---
title: Establecer Process-Wide seguridad mediante el Registro
description: Si desea establecer la seguridad para todo un proceso, una solución es establecer los niveles de seguridad que desea en el Registro.
ms.assetid: 87f0a64f-f3ec-4ee2-8d65-4f82e8971f0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d303f184229cb20aef1cbf71733956a3b6ce6618
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369627"
---
# <a name="setting-process-wide-security-through-the-registry"></a>Establecer Process-Wide seguridad mediante el Registro

Si desea establecer la seguridad para todo un proceso, una solución es establecer los niveles de seguridad que desea en el Registro. Si la aplicación no puede llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o si prefiere no usar la seguridad mediante programación, esta podría ser una buena opción. Si decide establecer la seguridad de todo el proceso mediante el Registro, debe tener en cuenta que si llama a **CoInitializeSecurity** dentro del programa COM, usará los valores de **CoInitializeSecurity** y omitirá los valores del Registro.

Hay dos maneras de establecer la seguridad en el Registro para la aplicación:

-   Puede usar Dcomcnfg.exe, que proporciona una interfaz de usuario sencilla para modificar los valores de seguridad. Todos los servidores COM se pueden configurar mediante Dcomcnfg.exe. Para obtener más información, vea [Setting Process-Wide Security Using DCOMCNFG](setting-processwide-security-using-dcomcnfg.md). Sin embargo, las aplicaciones cliente normalmente no aparecen en Dcomcnfg.exe a menos que el cliente cree un GUID y lo escriba en el Registro.
-   Puede establecer valores de seguridad en la clave [AppID](appid-key.md) de la aplicación. En el resto de este tema se explica cómo establecer la seguridad en el Registro mediante la **clave AppID.**

Un AppID es un GUID que representa un proceso de servidor para una o varias clases. Cada clase está asociada exactamente a un AppID y los AppID solo se pueden asignar a los EXE. Los archivos DLL no obtienen appID a menos que se ejecuten en un suplente y, a continuación, es el proceso suplente el que tiene el AppID. Si se cargan varios archivos DLL en un suplente, cada suplente solo tiene un AppID.

Para algunos servidores COM, el código de registro genera un AppID y coloca entradas en el Registro que asignan el AppID al nombre del ejecutable. Pero algunos servidores COM no proporcionan esta funcionalidad. Sin embargo, si el código de registro del servidor agrega una entrada para HKCR \\ CLSID{ServerCLSID} \\ [LocalServer32](localserver32.md) cuando se ejecuta dcomcnfg.exe, agregará automáticamente un AppID para el CLSID.

Para un cliente COM que no es un servidor, esta asignación no se crea porque el cliente nunca se registra. Por lo tanto, para establecer la seguridad mediante la clave **AppID,** el [](/windows/desktop/SysInfo/registry-functions) cliente debe crear las entradas del Registro necesarias, ya sea mediante programación mediante las funciones del Registro o mediante regedit.

Si decide establecer la seguridad de todo el proceso en el Registro en la clave **AppID,** tenga en cuenta que hay dos valores con nombre en la clave **AppID** que puede establecer sin tener permisos de administrador:

-   [AccessPermission](accesspermission.md)
-   [AuthenticationLevel](authenticationlevel.md)

Los **valores AuthenticationLevel** **y AccessPermission** se establecen de forma independiente y tienen valores predeterminados independientes. Si el **valor AuthenticationLevel** no está presente, el [valor LegacyAuthenticationLevel](legacyauthenticationlevel.md) se usa como valor predeterminado. De forma similar, si **el valor AccessPermission** no está presente, se usa el valor [DefaultAccessPermission](defaultaccesspermission.md) como valor predeterminado. Sin embargo, **los valores AuthenticationLevel** y **AccessPermission** están interrelacionados de las maneras siguientes:

-   Si **AuthenticationLevel** no es ninguno, los **valores AccessPermission** y **DefaultAccessPermission** se omiten para esa aplicación.
-   Si **AuthenticationLevel** no está presente y **LegacyAuthenticationLevel** no es ninguno, los valores **AccessPermission** y **DefaultAccessPermission** se omiten para esa aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de Process-Wide seguridad](setting-processwide-security.md)
</dt> </dl>

 

 