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
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a>Detección de si un equipo remoto admite WS-Management protocolo

Puede usar la [**sesión. Identify**](session-identify.md) o [**IWSManSession. Identifique**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) los métodos para determinar si el equipo remoto tiene un servicio que admite el protocolo de WS-Management.

Si un servicio de protocolo WS-Management está configurado en el equipo remoto y está escuchando solicitudes, el servicio puede detectar una solicitud de identificación mediante el siguiente XML en el encabezado.


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



El servicio de protocolo WS-Management que recibe la solicitud devuelve la información contenida en la lista siguiente, en el cuerpo del mensaje:

-   La versión del protocolo WS-Management. Por ejemplo, "https://schemas.dmtf.org/wbem/wsman/1/wsman".
-   El proveedor del producto, por ejemplo, "Microsoft Corporation".
-   Versión del producto. Si la solicitud se envía con **WSManFlagUseNoAuthentication** en el parámetro *Flags* , no se devuelve información de versión del producto. Si la solicitud se envía con la autenticación predeterminada activa o con otro modo de autenticación especificado, se puede devolver la información de versión del producto.

La solicitud para detectar si el equipo remoto tiene un servicio de protocolo configurado y de escucha WS-Management se puede realizar al principio de un script con otras operaciones. Esto comprobará que el equipo o equipos de destino pueden responder a otras solicitudes de protocolo WS-Management. La comprobación también puede realizarse en un script independiente.

**Para detectar un servicio de protocolo de WS-Management**

1.  Cree un objeto [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Determine si la solicitud se debe enviar autenticada o no autenticada y establezca el parámetro *Flags* en consecuencia en la llamada a [**WSMan. createSession**](wsman-createsession.md).

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  Sesión de llamada [**. Identifique**](session-identify.md).

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código de VBScript envía una solicitud de identificación no autenticada al equipo remoto denominado "Remote1" en el mismo dominio.


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



La siguiente respuesta muestra el XML devuelto por el equipo remoto. La versión del protocolo WS-Management (" https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ") y el proveedor del sistema operativo ("Microsoft Corporation") se especifican en el XML devuelto. Dado que el mensaje se envía sin autenticar, el servicio Administración remota de Windows no devuelve la versión del producto.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



El siguiente ejemplo de código de VBScript envía una solicitud de identificación autenticada al equipo remoto.


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

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> <dt>

[Referencia de Administración remota de Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 




