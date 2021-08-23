---
title: Establecer Process-Wide seguridad mediante el Registro
description: Si desea establecer la seguridad de todo un proceso, una solución es establecer los niveles de seguridad que desea en el registro.
ms.assetid: 87f0a64f-f3ec-4ee2-8d65-4f82e8971f0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8ad3a549a78a10b15e965ba2e2a47b9e5e84f1e8790ccfbf90af622051714e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730915"
---
# <a name="setting-process-wide-security-through-the-registry"></a>Establecer Process-Wide seguridad mediante el Registro

Si desea establecer la seguridad de todo un proceso, una solución es establecer los niveles de seguridad que desea en el registro. Si la aplicación no puede llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o si prefiere no usar la seguridad mediante programación, esta podría ser una buena opción. Si decide establecer la seguridad de todo el proceso mediante el Registro, debe tener en cuenta que si llama a **CoInitializeSecurity** dentro del programa COM, usará los valores de **CoInitializeSecurity** y omitirá los valores del Registro.

Hay dos maneras de establecer la seguridad en el Registro para la aplicación:

-   Puede usar Dcomcnfg.exe, que proporciona una interfaz de usuario sencilla para modificar los valores de seguridad. Todos los servidores COM se pueden configurar mediante Dcomcnfg.exe. Para obtener más información, vea [Establecer Process-Wide seguridad mediante DCOMCNFG.](setting-processwide-security-using-dcomcnfg.md) Sin embargo, las aplicaciones cliente no suelen aparecer en Dcomcnfg.exe a menos que el cliente cree un GUID y lo escriba en el Registro.
-   Puede establecer valores de seguridad en la [clave AppID](appid-key.md) de la aplicación. En el resto de este tema se explica cómo establecer la seguridad en el Registro mediante la **clave AppID.**

Un AppID es un GUID que representa un proceso de servidor para una o varias clases. Cada clase está asociada exactamente a un AppID, y los AppID solo se pueden asignar a exe. Los archivos DLL no obtienen appID a menos que se ejecuten en un suplente y, a continuación, es el proceso suplente el que tiene el AppID. Si se cargan varios archivos DLL en un suplente, cada suplente solo tiene un AppID.

En algunos servidores COM, el código de registro genera un AppID y coloca las entradas en el Registro que asignan el AppID al nombre del ejecutable. Pero algunos servidores COM no proporcionan esta funcionalidad. Sin embargo, si el código de registro del servidor agrega una entrada para HKCR \\ CLSID{ServerCLSID} \\ [LocalServer32](localserver32.md) cuando se ejecuta dcomcnfg.exe, agregará automáticamente un AppID para el CLSID.

Para un cliente COM que no es un servidor, esta asignación no se crea porque el cliente nunca se registra. Por lo tanto, para establecer la seguridad mediante la clave **AppID,** el [](/windows/desktop/SysInfo/registry-functions) cliente debe crear las entradas del Registro necesarias, ya sea mediante programación mediante las funciones del Registro o mediante regedit.

Si decide establecer la seguridad de todo el proceso en el Registro en la clave **AppID,** tenga en cuenta que hay dos valores con nombre en la clave **AppID** que puede establecer sin tener permisos de administrador:

-   [AccessPermission](accesspermission.md)
-   [AuthenticationLevel](authenticationlevel.md)

Los **valores AuthenticationLevel** **y AccessPermission** se establecen de forma independiente y tienen valores predeterminados independientes. Si el **valor AuthenticationLevel** no está presente, [el valor LegacyAuthenticationLevel](legacyauthenticationlevel.md) se usa como valor predeterminado. De forma similar, si **el valor AccessPermission** no está presente, el valor [DefaultAccessPermission](defaultaccesspermission.md) se usa como valor predeterminado. Sin embargo, **los valores AuthenticationLevel** y **AccessPermission** están interrelacionados de las maneras siguientes:

-   Si **AuthenticationLevel** no es ninguno, los **valores AccessPermission** y **DefaultAccessPermission** se omiten para esa aplicación.
-   Si **AuthenticationLevel** no está presente y **LegacyAuthenticationLevel** no es ninguno, los valores **AccessPermission** y **DefaultAccessPermission** se omiten para esa aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de Process-Wide seguridad](setting-processwide-security.md)
</dt> </dl>

 

 