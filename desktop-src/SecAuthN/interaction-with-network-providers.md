---
description: Explica las interacciones entre Winlogon y los proveedores de red.
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: Interacción con proveedores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d3eeadb7a9f4d8137e1d9b1ef7ff2430910cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071278"
---
# <a name="interaction-with-network-providers"></a>Interacción con proveedores de red

Puede configurar un sistema para que admita cero o más proveedores de red. Cada uno de estos proveedores de red puede especificar que requiere un procesamiento de autenticación interactivo especial. Esta funcionalidad permite a las redes instaladas recopilar información de identificación y autenticación específica de cada red, pero les permite recopilarla durante el inicio de sesión normal y bajo el paraguas seguro del contexto y el escritorio de [*Winlogon.*](../secgloss/w-gly.md) [](../secgloss/c-gly.md)

Winlogon llama a proveedores de red en una serie de circunstancias. Después de un inicio de sesión correcto, Winlogon llama a los proveedores de red para que puedan recopilar [*credenciales*](../secgloss/c-gly.md) y autenticar al usuario para su red. Winlogon también llama a los proveedores de red cuando los usuarios cambian sus contraseñas. Esto permite a cada usuario mantener una sola contraseña para su uso en todas las redes.

La [**estructura DE INFORMACIÓN DE NOTIFICACIÓN DE \_ MPR \_ DE \_ WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) se usa para proporcionar información de identificación y autenticación en las funciones GINA pertinentes. Esta estructura incluye los siguientes miembros.



| Miembro             | Descripción                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **pszUserName**    | Nombre de cuenta del usuario que inició sesión.                                                                                                                                                      |
| **pszDomain**      | Nombre de dominio del usuario que inició sesión. No todos los modelos de autenticación tienen un concepto de dominio (o su equivalente), por lo que este miembro puede ser **NULL.**                                              |
| **pszPassword**    | Cuando el usuario ha dado una contraseña de texto no cifrado durante la autenticación, proporcionarla aquí permite a otros proveedores de red usar la misma contraseña (para lograr un inicio de sesión único) sin preguntar al usuario.    |
| **pszOldPassword** | Después de un cambio de contraseña, proporcionar la contraseña original aquí y la nueva contraseña en el miembro **pszPassword** permite a los proveedores de red actualizar sus contraseñas sin preguntar al usuario. |



 

Una [*GINA*](../secgloss/g-gly.md) no tiene que proporcionar esta información a los proveedores de red. Si se **pasa un** puntero NULL en lugar de un puntero de estructura válido, los proveedores de red solicitarán información al usuario.

 

 
