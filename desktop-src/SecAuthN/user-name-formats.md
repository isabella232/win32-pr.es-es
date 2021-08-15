---
description: Cuando una aplicación usa el API de Administración credenciales para solicitar credenciales, se espera que el usuario escriba información que se pueda validar, ya sea por el sistema operativo o por la aplicación.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Formatos de nombre de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c2d4a31904e1cdc6c08da596e2db24054389387ef90142001e7f0e6e520567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915550"
---
# <a name="user-name-formats"></a>Formatos de nombre de usuario

Cuando una aplicación usa el API de Administración credenciales para solicitar credenciales, se espera que el usuario escriba información que se pueda validar, ya sea por el sistema operativo o por la aplicación. El usuario puede especificar información de credenciales de dominio en uno de los siguientes formatos:

-   [Nombre principal del usuario](#user-principal-name)
-   [Nombre de inicio de sesión de nivel inferior](#down-level-logon-name)

## <a name="user-principal-name"></a>Nombre principal del usuario

[*El formato de nombre principal*](../secgloss/u-gly.md) de usuario (UPN) se usa para especificar un nombre de estilo de Internet, como <b>UserName@Example.Microsoft.com</b> . En la tabla siguiente se resumen las partes de un UPN.



| Parte                                                        | Ejemplo                                |
|-------------------------------------------------------------|----------------------------------------|
| Nombre de la cuenta de usuario. También se conoce como nombre de inicio de sesión.<br/> | *UserName*<br/>                  |
| Separador. Literal de carácter, at sign (@).<br/> | @<br/>                           |
| Sufijo UPN. También se conoce como nombre de dominio.<br/>       | *Example.Microsoft.com* <br/> |



 

Un UPN se puede definir implícita o explícitamente. Un UPN implícito tiene el formato <b>UserName@DNSDomainName.com</b> . Un UPN implícito siempre está asociado a la cuenta del usuario, incluso si no se define un UPN explícito. Un UPN explícito tiene el formato , donde el administrador define explícitamente las cadenas de nombre <i><b>Name@Suffix</b></i> y sufijo.

## <a name="down-level-logon-name"></a>Down-Level de inicio de sesión

El formato de nombre de inicio de sesión de nivel inferior se usa para especificar un dominio y una cuenta de usuario en ese dominio, por ejemplo, <i><b>DOMAIN \\ UserName</b></i>. En la tabla siguiente se resumen las partes de un nombre de inicio de sesión de nivel inferior.



| Parte                                                           | Ejemplo               |
|----------------------------------------------------------------|-----------------------|
| Nombre de dominio NetBIOS.<br/>                                | *DOMAIN*<br/>   |
| Separador. Literal de carácter, la barra diagonal inversa ( \\ ).<br/> | **\\**<br/>     |
| Nombre de la cuenta de usuario. También se conoce como nombre de inicio de sesión.<br/>    | *UserName*<br/> |



 

 

 
