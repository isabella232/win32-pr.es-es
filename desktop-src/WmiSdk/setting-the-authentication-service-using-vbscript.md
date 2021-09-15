---
description: Al acceder a un servidor Windows Management Instrumentation (WMI) con un script, puede elegir entre los protocolos de autenticación NT LAN Manager (NTLM) o Kerberos.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Establecimiento del servicio de autenticación mediante VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465599"
---
# <a name="setting-the-authentication-service-using-vbscript"></a>Establecimiento del servicio de autenticación mediante VBScript

Al acceder a un servidor Windows Management Instrumentation (WMI) con un script, puede elegir entre los protocolos de autenticación NT LAN Manager (NTLM) o Kerberos. No es necesario especificar Kerberos excepto cuando se usa la delegación. Para obtener más información, vea [Connecting to a 3rd Computer-Delegation](connecting-to-a-3rd-computer-delegation.md).

Dado que las versiones del sistema operativo difieren en el servicio de autenticación que usan, se recomienda no especificar un valor para el campo de autoridad al conectarse a un sistema remoto. En su lugar, permita que el sistema operativo y la versión distribuida del Modelo de objetos componentes (DCOM) seleccione NTLM o Kerberos. Si se especifica un servicio de autenticación, la sintaxis requiere el nombre principal del servidor, que es el nombre del equipo de destino en lugar del controlador de dominio.

Puede usar el parámetro authority solo con conexiones a servidores WMI remotos. Se produce un error en el intento de conexión si intenta establecer niveles de autorización como parte de un moniker o con una llamada a [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) para una conexión local.

Realice el procedimiento siguiente para especificar el servicio de autenticación que desea usar en el parámetro *strAuthority* del método [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) o la conexión de cadena [de moniker.](constructing-a-moniker-string.md)

**Para especificar la autenticación NTLM o Kerberos con scripting API para WMI**

1.  Si el *parámetro strAuthority* comienza con la cadena "kerberos:", WMI asume que la cadena hace referencia a un nombre principal de Kerberos y se usa la autenticación Kerberos. Si el *parámetro strAuthority* comienza con la cadena "ntlmdomain:", WMI usa la autenticación NTLM en su lugar.
2.  Como alternativa, puede usar la parte de autoridad de un moniker para especificar el tipo de autenticación que se usa para conectarse a WMI. Para usar la autenticación Kerberos al usar un moniker, incluya la cadena "authority=kerberos:" seguida del nombre principal. Para usar la autenticación NTLM, incluya la cadena "authority=ntlmdomain:" seguida del nombre de dominio NTLM.

    En el ejemplo siguiente se muestra un moniker que solicita la autenticación Kerberos mediante la entidad de seguridad "mydomain \\ server".

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    En cambio, en el ejemplo siguiente se muestra un moniker que solicita la autenticación NTLM mediante el dominio "mydomain".

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



