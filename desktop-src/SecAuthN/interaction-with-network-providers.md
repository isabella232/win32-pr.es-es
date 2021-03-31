---
description: Explica las interacciones entre Winlogon y los proveedores de red.
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: Interacción con proveedores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d3eeadb7a9f4d8137e1d9b1ef7ff2430910cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912474"
---
# <a name="interaction-with-network-providers"></a>Interacción con proveedores de red

Puede configurar un sistema para que admita cero o más proveedores de red. Cada uno de estos proveedores de red puede especificar que requiere un procesamiento de autenticación interactiva especial. Esta funcionalidad permite que las redes instaladas recopilen información de identificación y autenticación específica de cada red, pero les permite recopilarla durante el inicio de sesión normal y en el paraguas seguro del [*contexto*](../secgloss/c-gly.md) y el escritorio de [*Winlogon*](../secgloss/w-gly.md) .

Winlogon llama a los proveedores de red en varios casos. Después de un inicio de sesión correcto, Winlogon llama a los proveedores de red para que puedan recopilar [*las credenciales*](../secgloss/c-gly.md) y autenticar al usuario para su red. Winlogon también llama a los proveedores de red cuando los usuarios cambian sus contraseñas. Esto permite a cada usuario mantener una única contraseña para su uso en todas las redes.

La estructura de [**\_ información de \_ notificación \_ de WLX MPR**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) se usa para proporcionar información de identificación y autenticación en las funciones de Gina relevantes. Esta estructura incluye los siguientes miembros.



| Miembro             | Descripción                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **pszUserName**    | Nombre de cuenta del usuario que ha iniciado sesión.                                                                                                                                                      |
| **pszDomain**      | El nombre de dominio del usuario que ha iniciado sesión. No todos los modelos de autenticación tienen un concepto de dominio (o su equivalente), por lo que este miembro puede ser **null**.                                              |
| **pszPassword**    | Cuando el usuario dio una contraseña de texto no cifrado durante la autenticación, al proporcionarla aquí se permite a otros proveedores de red usar la misma contraseña (para lograr un inicio de sesión único) sin preguntar al usuario.    |
| **pszOldPassword** | Después de un cambio de contraseña, que proporciona la contraseña original aquí y la nueva contraseña en el miembro **pszPassword** , permite a los proveedores de red actualizar sus contraseñas sin preguntar al usuario. |



 

[*Gina*](../secgloss/g-gly.md) no tiene que proporcionar esta información a los proveedores de red. Si se pasa un puntero **nulo** en lugar de un puntero de estructura válido, los proveedores de red pedirán al usuario información.

 

 
