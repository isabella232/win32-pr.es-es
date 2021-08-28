---
title: Detección de si un equipo remoto admite WS-Management protocolo
description: Puede usar los métodos Session.Identify o IWSManSession.Identify para determinar si el equipo remoto tiene un servicio que admita el protocolo WS-Management usuario.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a7ebeb25f7f3af69a03c55499dd53a890e540c1a1ed677e7d48e5b11b82b1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643235"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a>Detección de si un equipo remoto admite WS-Management protocolo

Puede usar los métodos [**Session.Identify**](session-identify.md) o [**IWSManSession.Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) para determinar si el equipo remoto tiene un servicio que admita el protocolo WS-Management usuario.

Si un WS-Management de protocolo está configurado en el equipo remoto y está escuchando solicitudes, el servicio puede detectar una solicitud de identificación mediante el siguiente XML en el encabezado .


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



El WS-Management de protocolo que recibe la solicitud devuelve la información, incluida en la lista siguiente, en el cuerpo del mensaje:

-   La WS-Management del protocolo. Por ejemplo, "https://schemas.dmtf.org/wbem/wsman/1/wsman".
-   El proveedor del producto, por ejemplo, "Microsoft Corporation".
-   Versión del producto. Si la solicitud se envía con **WSManFlagUseNoAuthentication en** el *parámetro flags,* no se devuelve información de versión del producto. Si la solicitud se envía con la autenticación predeterminada en vigor o con otro modo de autenticación especificado, se puede devolver la información de la versión del producto.

La solicitud para detectar si el equipo remoto tiene configurado un servicio de protocolo WS-Management escucha y se puede realizar al principio de un script con otras operaciones. Esto comprobará que el equipo o los equipos de destino pueden responder a más solicitudes WS-Management protocolo. La comprobación también se puede realizar en un script independiente.

**Para detectar un servicio WS-Management protocolo**

1.  Cree un [**objeto WSMan.**](wsman.md)

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Determine si la solicitud debe enviarse autenticada o no autenticada y establezca el parámetro *flags* en consecuencia en la llamada a [**WSMan.CreateSession**](wsman-createsession.md).

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  Llame [**a Session.Identify.**](session-identify.md)

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a>Ejemplos

En el ejemplo de código vbscript siguiente se envía una solicitud de identificación no autenticada al equipo remoto denominado "Remote1" en el mismo dominio.


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



La siguiente respuesta muestra el XML devuelto por el equipo remoto. La WS-Management de protocolo (" ") y el proveedor de sistema operativo https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ("Microsoft Corporation") se especifican en el XML devuelto. Dado que el mensaje se envía sin autenticar, el servicio de administración remota no devuelve la versión del producto Windows.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



En el ejemplo de código de VBScript siguiente se envía una solicitud de identificación autenticada al equipo remoto.


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



Dado que la solicitud se envió con autenticación, se devuelve la información de versión.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Uso de Windows administración remota](using-windows-remote-management.md)
</dt> <dt>

[Windows Referencia de administración remota](windows-remote-management-reference.md)
</dt> </dl>

 

 




