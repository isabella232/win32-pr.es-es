---
description: Al tener acceso a un servidor de Instrumental de administración de Windows (WMI) con un script, puede elegir entre los protocolos de autenticación NT LAN Manager (NTLM) o Kerberos.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Establecer el servicio de autenticación mediante VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717040"
---
# <a name="setting-the-authentication-service-using-vbscript"></a>Establecer el servicio de autenticación mediante VBScript

Al tener acceso a un servidor de Instrumental de administración de Windows (WMI) con un script, puede elegir entre los protocolos de autenticación NT LAN Manager (NTLM) o Kerberos. No es necesario especificar Kerberos excepto cuando se usa la delegación. Para obtener más información, vea [conectarse a un tercer equipo: Delegación](connecting-to-a-3rd-computer-delegation.md).

Dado que las versiones de sistema operativo difieren en el servicio de autenticación que usan, se recomienda no especificar un valor para el campo entidad al conectarse a un sistema remoto. En su lugar, permita que el sistema operativo y la versión distribuida del modelo de objetos componentes (DCOM) seleccionen NTLM o Kerberos. Si se especifica un servicio de autenticación, la sintaxis requiere el nombre de la entidad de seguridad del servidor, que es el nombre del equipo de destino en lugar del controlador de dominio.

Solo puede usar el parámetro Authority con conexiones a servidores WMI remotos. Se produce un error en el intento de conexión si intenta establecer los niveles de autorización como parte de un moniker o con una llamada a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) para una conexión local.

Realice el procedimiento siguiente para especificar el servicio de autenticación que desea usar en el parámetro *strAuthority* del método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) o la conexión de cadena de [moniker](constructing-a-moniker-string.md) .

**Para especificar la autenticación NTLM o Kerberos con la API de scripting para WMI**

1.  Si el parámetro *strAuthority* comienza con la cadena "Kerberos:", WMI supone que la cadena hace referencia a un nombre de entidad de seguridad de Kerberos y se utiliza la autenticación Kerberos. Si el parámetro *strAuthority* comienza con la cadena "ntlmdomain:", WMI utiliza la autenticación NTLM en su lugar.
2.  Como alternativa, puede usar la parte de autoridad de un moniker para especificar el tipo de autenticación que se utiliza para conectarse a WMI. Para usar la autenticación Kerberos al utilizar un moniker, incluya la cadena "Authority = Kerberos:" seguida del nombre de la entidad de seguridad. Para usar la autenticación NTLM, incluya la cadena "Authority = ntlmdomain:" seguida del nombre de dominio NTLM.

    En el ejemplo siguiente se muestra un moniker que solicita la autenticación Kerberos mediante la entidad "midominio \\ Server".

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    En cambio, en el ejemplo siguiente se muestra un moniker que solicita la autenticación NTLM mediante el dominio "midominio".

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



