// Get Data
const accounts = await entities.crm_account.find({
    select: ["id", "name", "country", "updatedAt", "updatedBy", "type", "accountid"],
    order: { name: "ASC" },
});

const countries = await entities.crm_country.find({
    select: ["country", "name", "flagurl"],
});

const types = await entities.crm_type.find({
    select: ["type", "name"]
});

// Build Data
accounts.forEach(function (account) {

    const country = countries.find(countries => countries.country === account.country);
    const type = types.find(types => types.type === account.type);

    if (country) {
        account.countryText = country.name;
        account.countryFlagUrl = country.flagurl;
    }

    if (type) account.typeText = type.name;

});

// Send Data to Client
result.data = accounts;
complete();