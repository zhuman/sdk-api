---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetProxyExceptionList
title: IWMReaderNetworkConfig::SetProxyExceptionList (wmsdkidl.h)
description: The SetProxyExceptionList method specifies the proxy exception list.helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","SetProxyExceptionList method","IWMReaderNetworkConfig.SetProxyExceptionList","IWMReaderNetworkConfig::SetProxyExceptionList","IWMReaderNetworkConfigSetProxyExceptionList","SetProxyExceptionList","SetProxyExceptionList method [windows Media Format]","SetProxyExceptionList method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_setproxyexceptionlist","wmsdkidl/IWMReaderNetworkConfig::SetProxyExceptionList"]
old-location: wmformat\iwmreadernetworkconfig_setproxyexceptionlist.htm
tech.root: wmformat
ms.assetid: 1f6c6bb6-3a42-44da-ab80-e72a19b8d272
ms.date: 12/05/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetProxyExceptionList method, IWMReaderNetworkConfig.SetProxyExceptionList, IWMReaderNetworkConfig::SetProxyExceptionList, IWMReaderNetworkConfigSetProxyExceptionList, SetProxyExceptionList, SetProxyExceptionList method [windows Media Format], SetProxyExceptionList method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setproxyexceptionlist, wmsdkidl/IWMReaderNetworkConfig::SetProxyExceptionList
f1_keywords:
- wmsdkidl/IWMReaderNetworkConfig.SetProxyExceptionList
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmvcore.lib
- Wmvcore.dll
- WMStubDRM.lib
- WMStubDRM.dll
api_name:
- IWMReaderNetworkConfig.SetProxyExceptionList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderNetworkConfig::SetProxyExceptionList


## -description



The <b>SetProxyExceptionList</b> method specifies the proxy exception list.




## -parameters




### -param pwszProtocol [in]

Pointer to a wide-character null-terminated string containing the protocol.


### -param pwszExceptionList [in]

Pointer to a wide-character null-terminated string containing the exception list. The list must be a comma-separated list of hosts. Exception lists are limited to 1024 wide characters.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
NULL or invalid argument passed in.

</td>
</tr>
</table>
 




## -remarks



The exception list is a list of computers, domains, or addresses that bypass the proxy host name when the host in the target URL matches an entry in the list.

Wildcard characters can be used in the list entries (using the * character). For example "*.com" would match all hosts in the "com" domain while "67.*" would match all hosts in the 67 class A subnet. The exception list is used only when the proxy setting is WMT_PROXY_SETTING_MANUAL. If the proxy setting is WMT_PROXY_SETTING_BROWSER, then the exception list configured in the browser is used instead.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getproxyexceptionlist">IWMReaderNetworkConfig::GetProxyExceptionList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxysettings">IWMReaderNetworkConfig::SetProxySettings</a>
 

 

