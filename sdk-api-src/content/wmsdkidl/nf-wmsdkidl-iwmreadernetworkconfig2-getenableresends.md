---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetEnableResends
title: IWMReaderNetworkConfig2::GetEnableResends (wmsdkidl.h)
description: The GetEnableResends method ascertains whether resending is enabled.helpviewer_keywords: ["GetEnableResends","GetEnableResends method [windows Media Format]","GetEnableResends method [windows Media Format]","IWMReaderNetworkConfig2 interface","IWMReaderNetworkConfig2 interface [windows Media Format]","GetEnableResends method","IWMReaderNetworkConfig2.GetEnableResends","IWMReaderNetworkConfig2::GetEnableResends","IWMReaderNetworkConfig2GetEnableResends","wmformat.iwmreadernetworkconfig2_getenableresends","wmsdkidl/IWMReaderNetworkConfig2::GetEnableResends"]
old-location: wmformat\iwmreadernetworkconfig2_getenableresends.htm
tech.root: wmformat
ms.assetid: d39d42c3-7d00-4fb6-8979-2b65d00ac636
ms.date: 12/05/2018
ms.keywords: GetEnableResends, GetEnableResends method [windows Media Format], GetEnableResends method [windows Media Format],IWMReaderNetworkConfig2 interface, IWMReaderNetworkConfig2 interface [windows Media Format],GetEnableResends method, IWMReaderNetworkConfig2.GetEnableResends, IWMReaderNetworkConfig2::GetEnableResends, IWMReaderNetworkConfig2GetEnableResends, wmformat.iwmreadernetworkconfig2_getenableresends, wmsdkidl/IWMReaderNetworkConfig2::GetEnableResends
f1_keywords:
- wmsdkidl/IWMReaderNetworkConfig2.GetEnableResends
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
- IWMReaderNetworkConfig2.GetEnableResends
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderNetworkConfig2::GetEnableResends


## -description



The <b>GetEnableResends</b> method ascertains whether resending is enabled.




## -parameters




### -param pfEnableResends [out]

Pointer to a Boolean value that is set to True if resending is enabled.


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
NULL pointer argument.

</td>
</tr>
</table>
 




## -remarks



This feature is available only for content streamed from a server running Windows Media Services using either MMSU or RTSPU protocol.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2">IWMReaderNetworkConfig2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenableresends">IWMReaderNetworkConfig2::SetEnableResends</a>
 

 

