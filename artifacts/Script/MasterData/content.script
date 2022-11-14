// Get Data
const country = await entities.crm_country.find({ select: ["country", "name"] });
const type = await entities.crm_type.find({ select: ["type", "name"] });
const currency = await entities.crm_currency.find({ select: ["currency", "name"] });
const industry = await entities.crm_industry.find({ select: ["industry", "name"] });
const stage = await entities.crm_stage.find({ select: ["stage", "name"] });

// Adding empty rows
country.splice(0, 0, {});
type.splice(0, 0, {});
currency.splice(0, 0, {});
industry.splice(0, 0, {});
stage.splice(0, 0, {});

// Send Data to Client
result.data = {
    country: country,
    type: type,
    currency: currency,
    industry: industry,
    stage: stage,
};

complete();
