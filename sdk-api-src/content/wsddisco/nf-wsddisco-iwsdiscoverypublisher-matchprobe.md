---
UID: NF:wsddisco.IWSDiscoveryPublisher.MatchProbe
title: IWSDiscoveryPublisher::MatchProbe (wsddisco.h)
description: Determines whether a Probe message matches the specified host and sends a WS-Discovery ProbeMatches message if the match is made.helpviewer_keywords: ["IWSDiscoveryPublisher interface","MatchProbe method","IWSDiscoveryPublisher.MatchProbe","IWSDiscoveryPublisher::MatchProbe","MatchProbe","MatchProbe method","MatchProbe method","IWSDiscoveryPublisher interface","ncd.iwsdiscoverypublisher_matchprobe_method","wsddisco/IWSDiscoveryPublisher::MatchProbe"]
old-location: ncd\iwsdiscoverypublisher_matchprobe_method.htm
tech.root: WsdApi
ms.assetid: 657f50ad-128f-4ccb-b89a-ed88f5d9b381
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisher interface,MatchProbe method, IWSDiscoveryPublisher.MatchProbe, IWSDiscoveryPublisher::MatchProbe, MatchProbe, MatchProbe method, MatchProbe method,IWSDiscoveryPublisher interface, ncd.iwsdiscoverypublisher_matchprobe_method, wsddisco/IWSDiscoveryPublisher::MatchProbe
f1_keywords:
- wsddisco/IWSDiscoveryPublisher.MatchProbe
dev_langs:
- c++
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wsdapi.dll
api_name:
- IWSDiscoveryPublisher.MatchProbe
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDiscoveryPublisher::MatchProbe


## -description


Determines whether a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/probe-message">Probe</a> message matches the specified host and sends a WS-Discovery <a href="https://docs.microsoft.com/windows/desktop/WsdApi/probematches-message">ProbeMatches</a> message if the match is made.


## -parameters




### -param pProbeMessage [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_message">WSD_SOAP_MESSAGE</a> structure that represents the Probe message passed to the notification sink's <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublishernotify-probehandler">ProbeHandler</a>.


### -param pMessageParameters [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a> object that represents the transmission parameters passed in to the notification sink's <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublishernotify-probehandler">ProbeHandler</a>.


### -param pszId [in]

The logical or physical address of the device, which is used as the device endpoint address. A logical address is of the form <code>urn:uuid:{guid}</code>. A physical address can be a URI prefixed by http or https, or simply a URI prefixed by <code>uri</code>. Whenever possible, use a logical address.


### -param ullMetadataVersion [in]

The current metadata version.

<div class="alert"><b>Note</b>  For compatibility with the <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery specification</a>, this value must be less than or equal to UINT_MAX (4294967295).</div>
<div> </div>

### -param ullInstanceId [in]

Identifier for the current instance of the device being published. This identifier must be incremented whenever the service is restarted.  For more information about instance identifiers, see Appendix I of the <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery specification</a>.

<div class="alert"><b>Note</b>  For compatibility with the <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery specification</a>, this value must be less than or equal to UINT_MAX (4294967295).</div>
<div> </div>

### -param ullMessageNumber [in]

Counter within the scope of the instance identifier for the current message. The message number must be incremented for each message.

<div class="alert"><b>Note</b>  For compatibility with the <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery specification</a>, this value must be less than or equal to UINT_MAX (4294967295).</div>
<div> </div>

### -param pszSessionId [in, optional]

Unique identifier within the scope of the instance identifier for the current session. This parameter corresponds to the sequence identifier in the AppSequence block in the Probe message. For more information about sequence identifiers, see Appendix I of the <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery specification</a>.

This parameter may be <b>NULL</b>.


### -param pTypesList [in, optional]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_name_list">WSD_NAME_LIST</a> structure that represents the list of types supported by the publishing host. May be <b>NULL</b>. 

If <i>pTypesList</i> is specified, <b>MatchProbe</b> will use WS-Discovery matching logic to verify that the types in the list match the types specified in <i>pProbeMessage</i>.


### -param pScopesList [in, optional]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_uri_list">WSD_URI_LIST</a> structure that represents the list of matching scopes supported by the publishing host. The list contains  hash values in string form. May be <b>NULL</b>.

If <i>pScopesList</i> is specified, <b>MatchProbe</b> will use WS-Discovery matching logic to verify that the scopes in the list match the scopes specified in <i>pProbeMessage</i>.


### -param pXAddrsList [in, optional]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_uri_list">WSD_URI_LIST</a> structure that represents the list of transport addresses supported by the publishing host. Each transport address string contains an address and port number which can be used for connection by a remote host. May be <b>NULL</b>.


## -returns



Possible return values include, but are not limited to, the following:

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the following conditions is true:

<ul>
<li><i>pszId</i> is <b>NULL</b>.</li>
<li>The length in characters of <i>pszId</i> exceeds WSD_MAX_TEXT_LENGTH (8192). </li>
<li>The length in characters of <i>pszSessionId</i> exceeds WSD_MAX_TEXT_LENGTH (8192). </li>
<li><i>pProbeMessage</i> is <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The publisher has not been started. Attaching a notification sink starts the publisher. To attach a sink, call <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-registernotificationsink">RegisterNotificationSink</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



<b>MatchProbe</b> should be called only when the discovery publisher has issued a <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublishernotify-probehandler">ProbeHandler</a> callback. <i>pProbeMessage</i> and <i>pMessageParameters</i> are passed directly from the callback into <b>MatchProbe</b>. The <b>ProbeHandler</b> also passes information required by the publisher to determine if the supplied Probe message matches and, if so, to issue a ProbeMatches response if appropriate.

<b>MatchProbe</b> sends ProbeMatches messages on all bound adapters and automatically issues message retransmissions when required by WS-Discovery.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a>
 

 

