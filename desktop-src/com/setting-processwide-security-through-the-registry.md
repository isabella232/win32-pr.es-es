---
title: Establecer la seguridad de Process-Wide a través del registro
description: Si desea establecer la seguridad para un proceso completo, una solución consiste en establecer los niveles de seguridad que desee en el registro.
ms.assetid: 87f0a64f-f3ec-4ee2-8d65-4f82e8971f0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d303f184229cb20aef1cbf71733956a3b6ce6618
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995664"
---
# <a name="setting-process-wide-security-through-the-registry"></a>Establecer la seguridad de Process-Wide a través del registro

Si desea establecer la seguridad para un proceso completo, una solución consiste en establecer los niveles de seguridad que desee en el registro. Si la aplicación no puede llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o si prefiere no usar la seguridad mediante programación, podría ser una buena opción. Si decide establecer la seguridad de todo el proceso mediante el registro, debe tener en cuenta que si llama a **CoInitializeSecurity** en el programa com, usará los valores de **CoInitializeSecurity** y omitirá los valores del registro.

Hay dos maneras de establecer la seguridad en el registro de la aplicación:

-   Puede usar Dcomcnfg.exe, que proporciona una interfaz de usuario simple para modificar los valores de seguridad. Todos los servidores COM se pueden configurar mediante Dcomcnfg.exe. Para obtener más información, vea [establecer la seguridad de Process-Wide mediante DCOMCNFG](setting-processwide-security-using-dcomcnfg.md). Sin embargo, las aplicaciones cliente no aparecen normalmente en Dcomcnfg.exe a menos que el cliente cree un GUID y lo escriba en el registro.
-   Puede establecer valores de seguridad en la clave [AppID](appid-key.md) de la aplicación. En el resto de este tema se explica cómo establecer la seguridad en el registro mediante la clave **AppID** .

Un AppID es un GUID que representa un proceso de servidor para una o más clases. Cada clase está asociada con exactamente un AppID y AppIDs solo se puede asignar a exe. Los archivos dll no obtienen AppIDs a menos que se ejecuten en un suplente y, a continuación, es el proceso suplente que tiene el AppID. Si se cargan varios archivos dll en un suplente, cada suplente tiene solo un AppID.

En algunos servidores COM, el código de registro genera un AppID y coloca entradas en el registro que asignan el AppID al nombre del archivo ejecutable. Sin embargo, algunos servidores COM no proporcionan esta funcionalidad. Sin embargo, si el código de registro del servidor agrega una entrada para \\ el CLSID HKCR {ServerCLSID} \\ [LocalServer32](localserver32.md) cuando se ejecuta dcomcnfg.exe, se agregará automáticamente un AppID para el CLSID.

Para un cliente COM que no es un servidor, esta asignación no se crea porque el cliente nunca se registra. Por consiguiente, para establecer la seguridad mediante la clave **AppID** , el cliente debe crear las entradas del registro necesarias, ya sea mediante programación con las [funciones del registro](/windows/desktop/SysInfo/registry-functions) o mediante regedit.

Si decide establecer la seguridad de todo el proceso en el registro con la clave **AppID** , tenga en cuenta que hay dos valores con nombre en la clave **AppID** que puede establecer sin tener permisos de administrador:

-   [AccessPermission](accesspermission.md)
-   [AuthenticationLevel](authenticationlevel.md)

Los valores **AuthenticationLevel** y **AccessPermission** se establecen de forma independiente y tienen valores predeterminados independientes. Si el valor de **AuthenticationLevel** no está presente, el valor de [LegacyAuthenticationLevel](legacyauthenticationlevel.md) se utiliza como valor predeterminado. Del mismo modo, si el valor de **AccessPermission** no está presente, el valor de [DefaultAccessPermission](defaultaccesspermission.md) se utiliza como valor predeterminado. Sin embargo, los valores de **AuthenticationLevel** y **AccessPermission** se interrelacionan de las siguientes maneras:

-   Si el valor de **AuthenticationLevel** es None, los valores **AccessPermission** y **DefaultAccessPermission** se omiten para esa aplicación.
-   Si **AuthenticationLevel** no está presente y **LegacyAuthenticationLevel** es None, los valores **AccessPermission** y **DefaultAccessPermission** se omiten para esa aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad de Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 