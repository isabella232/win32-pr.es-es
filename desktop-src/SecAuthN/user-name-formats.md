---
description: Cuando una aplicación usa la API de administración de credenciales para solicitar credenciales, se espera que el usuario escriba información que se pueda validar, ya sea por parte del sistema operativo o de la aplicación.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Formatos de nombre de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652905"
---
# <a name="user-name-formats"></a>Formatos de nombre de usuario

Cuando una aplicación usa la API de administración de credenciales para solicitar credenciales, se espera que el usuario escriba información que se pueda validar, ya sea por parte del sistema operativo o de la aplicación. El usuario puede especificar la información de las credenciales de dominio en uno de los siguientes formatos:

-   [Nombre principal del usuario](#user-principal-name)
-   [Nombre de inicio de sesión de nivel inferior](#down-level-logon-name)

## <a name="user-principal-name"></a>Nombre principal del usuario

[*El formato de nombre principal de usuario*](../secgloss/u-gly.md) (UPN) se usa para especificar un nombre de estilo de Internet, como <b>UserName@Example.Microsoft.com</b> . En la tabla siguiente se resumen las partes de un UPN.



| Parte                                                        | Ejemplo                                |
|-------------------------------------------------------------|----------------------------------------|
| Nombre de la cuenta de usuario. También se conoce como nombre de inicio de sesión.<br/> | *UserName*<br/>                  |
| Separador. Un literal de carácter, el signo de arroba (@).<br/> | @<br/>                           |
| Sufijo UPN. También se conoce como nombre de dominio.<br/>       | *Example.Microsoft.com* <br/> |



 

Un UPN puede definirse implícita o explícitamente. Un UPN implícito tiene el formato <b>UserName@DNSDomainName.com</b> . Un UPN implícito siempre está asociado a la cuenta del usuario, incluso si no se ha definido un UPN explícito. Un UPN explícito tiene el formato <i><b>Name@Suffix</b></i> , donde el administrador define explícitamente las cadenas de nombre y sufijo.

## <a name="down-level-logon-name"></a>Nombre de inicio de sesión Down-Level

El formato de nombre de inicio de sesión de nivel inferior se usa para especificar un dominio y una cuenta de usuario en ese dominio, por ejemplo, <i><b>dominio \\ nombreDeUsuario</b></i>. En la tabla siguiente se resumen las partes de un nombre de inicio de sesión de nivel inferior.



| Parte                                                           | Ejemplo               |
|----------------------------------------------------------------|-----------------------|
| Nombre de dominio NetBIOS.<br/>                                | *DOMAIN*<br/>   |
| Separador. Un literal de carácter, la barra diagonal inversa ( \\ ).<br/> | **\\**<br/>     |
| Nombre de la cuenta de usuario. También se conoce como nombre de inicio de sesión.<br/>    | *UserName*<br/> |



 

 

 
