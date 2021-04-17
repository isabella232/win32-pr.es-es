---
title: Detección de si un equipo remoto admite WS-Management protocolo
description: Puede usar la sesión. Identify o IWSManSession. Identifique los métodos para determinar si el equipo remoto tiene un servicio que admite el protocolo de WS-Management.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82284b38b2a101c767766d44eb975ff7e1dadc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704659"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a><span data-ttu-id="c6778-103">Detección de si un equipo remoto admite WS-Management protocolo</span><span class="sxs-lookup"><span data-stu-id="c6778-103">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>

<span data-ttu-id="c6778-104">Puede usar la [**sesión. Identify**](session-identify.md) o [**IWSManSession. Identifique**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) los métodos para determinar si el equipo remoto tiene un servicio que admite el protocolo de WS-Management.</span><span class="sxs-lookup"><span data-stu-id="c6778-104">You can use the [**Session.Identify**](session-identify.md) or [**IWSManSession.Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) methods to determine if the remote computer has a service that supports the WS-Management protocol.</span></span>

<span data-ttu-id="c6778-105">Si un servicio de protocolo WS-Management está configurado en el equipo remoto y está escuchando solicitudes, el servicio puede detectar una solicitud de identificación mediante el siguiente XML en el encabezado.</span><span class="sxs-lookup"><span data-stu-id="c6778-105">If a WS-Management protocol service is configured on the remote computer and is listening for requests, the service can detect an Identify request by the following XML in the header.</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



<span data-ttu-id="c6778-106">El servicio de protocolo WS-Management que recibe la solicitud devuelve la información contenida en la lista siguiente, en el cuerpo del mensaje:</span><span class="sxs-lookup"><span data-stu-id="c6778-106">The WS-Management protocol service that receives the request returns the information, contained in the following list, in the body of the message:</span></span>

-   <span data-ttu-id="c6778-107">La versión del protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="c6778-107">The WS-Management protocol version.</span></span> <span data-ttu-id="c6778-108">Por ejemplo, "https://schemas.dmtf.org/wbem/wsman/1/wsman".</span><span class="sxs-lookup"><span data-stu-id="c6778-108">For example, "https://schemas.dmtf.org/wbem/wsman/1/wsman".</span></span>
-   <span data-ttu-id="c6778-109">El proveedor del producto, por ejemplo, "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="c6778-109">The product vendor, for example, "Microsoft Corporation".</span></span>
-   <span data-ttu-id="c6778-110">Versión del producto.</span><span class="sxs-lookup"><span data-stu-id="c6778-110">The product version.</span></span> <span data-ttu-id="c6778-111">Si la solicitud se envía con **WSManFlagUseNoAuthentication** en el parámetro *Flags* , no se devuelve información de versión del producto.</span><span class="sxs-lookup"><span data-stu-id="c6778-111">If the request is sent with **WSManFlagUseNoAuthentication** in the *flags* parameter, then no product version information is returned.</span></span> <span data-ttu-id="c6778-112">Si la solicitud se envía con la autenticación predeterminada activa o con otro modo de autenticación especificado, se puede devolver la información de versión del producto.</span><span class="sxs-lookup"><span data-stu-id="c6778-112">If the request is sent with either the default authentication in effect or with another authentication mode specified, then the product version information can be returned.</span></span>

<span data-ttu-id="c6778-113">La solicitud para detectar si el equipo remoto tiene un servicio de protocolo configurado y de escucha WS-Management se puede realizar al principio de un script con otras operaciones.</span><span class="sxs-lookup"><span data-stu-id="c6778-113">The request to detect whether the remote computer has a configured and listening WS-Management protocol service can be performed at the beginning of a script with other operations.</span></span> <span data-ttu-id="c6778-114">Esto comprobará que el equipo o equipos de destino pueden responder a otras solicitudes de protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="c6778-114">This will verify that the target computer or computers can respond to further WS-Management protocol requests.</span></span> <span data-ttu-id="c6778-115">La comprobación también puede realizarse en un script independiente.</span><span class="sxs-lookup"><span data-stu-id="c6778-115">The verification also can be done in a separate script.</span></span>

<span data-ttu-id="c6778-116">**Para detectar un servicio de protocolo de WS-Management**</span><span class="sxs-lookup"><span data-stu-id="c6778-116">**To detect a WS-Management protocol service**</span></span>

1.  <span data-ttu-id="c6778-117">Cree un objeto [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="c6778-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="c6778-118">Determine si la solicitud se debe enviar autenticada o no autenticada y establezca el parámetro *Flags* en consecuencia en la llamada a [**WSMan. createSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="c6778-118">Determine whether the request should be sent authenticated or unauthenticated and set the *flags* parameter accordingly in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  <span data-ttu-id="c6778-119">Sesión de llamada [**. Identifique**](session-identify.md).</span><span class="sxs-lookup"><span data-stu-id="c6778-119">Call [**Session.Identify**](session-identify.md).</span></span>

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a><span data-ttu-id="c6778-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c6778-120">Examples</span></span>

<span data-ttu-id="c6778-121">El siguiente ejemplo de código de VBScript envía una solicitud de identificación no autenticada al equipo remoto denominado "Remote1" en el mismo dominio.</span><span class="sxs-lookup"><span data-stu-id="c6778-121">The following VBScript code example sends an unauthenticated Identify request to the remote computer named "Remote1" in the same domain.</span></span>


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



<span data-ttu-id="c6778-122">La siguiente respuesta muestra el XML devuelto por el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="c6778-122">The following response shows the XML returned by the remote computer.</span></span> <span data-ttu-id="c6778-123">La versión del protocolo WS-Management (" https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ") y el proveedor del sistema operativo ("Microsoft Corporation") se especifican en el XML devuelto.</span><span class="sxs-lookup"><span data-stu-id="c6778-123">The WS-Management protocol version ("https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd") and the operating system vendor ("Microsoft Corporation") are specified in the returned XML.</span></span> <span data-ttu-id="c6778-124">Dado que el mensaje se envía sin autenticar, el servicio Administración remota de Windows no devuelve la versión del producto.</span><span class="sxs-lookup"><span data-stu-id="c6778-124">Because the message is sent unauthenticated, the product version is not returned by the Windows Remote Management service.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



<span data-ttu-id="c6778-125">El siguiente ejemplo de código de VBScript envía una solicitud de identificación autenticada al equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="c6778-125">The following VBScript code example sends an authenticated Identify request to the remote computer.</span></span>


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



<span data-ttu-id="c6778-126">Dado que la solicitud se envió con autenticación, se devuelve la información de versión.</span><span class="sxs-lookup"><span data-stu-id="c6778-126">Because the request was sent with authentication, the version information is returned.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a><span data-ttu-id="c6778-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6778-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6778-128">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="c6778-128">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="c6778-129">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="c6778-129">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="c6778-130">Referencia de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="c6778-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




