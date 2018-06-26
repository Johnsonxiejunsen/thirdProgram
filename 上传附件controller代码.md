# thirdProgram
show my code
/**
     * 获取上传附件信息
     * @param params
     */
    @RequestMapping(value = "/delFileInfo", method = RequestMethod.GET)
    @FuncOper(operName = "删除上传附件信息", operCode = "DEL_FILEINFO", funCode = "ADMINORGAN_PRESERVE")
    public void delFileInfo(@RequestParam(required = false) Map<String, String> params) {
        JSONObject param = (JSONObject) JSONObject.toJSON(params);
        iFileStorage.deleteFile(String.valueOf(param.get("filedId")));
    }
