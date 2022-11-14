var options = {
    data: modeloPageDetail.oData
};

apiSave(options).then(function (res) {
    modeloPageDetail.setData(res);
    sap.m.MessageToast.show("Account saved successfully");
    apiList();
});