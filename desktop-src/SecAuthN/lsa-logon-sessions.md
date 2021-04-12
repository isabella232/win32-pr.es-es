---
description: Una sesión de inicio de sesión es una sesión informática que comienza cuando una autenticación de usuario se realiza correctamente y termina cuando el usuario cierra la sesión del sistema.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: Sesiones de inicio de sesión LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32a4912218b68c25c5c23334f7b34ef875fa318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278135"
---
# <a name="lsa-logon-sessions"></a>Sesiones de inicio de sesión LSA

Una [*sesión de inicio*](../secgloss/l-gly.md) de sesión es una sesión informática que comienza cuando una autenticación de usuario se realiza correctamente y termina cuando el usuario cierra la sesión del sistema.

Cuando un usuario se autentica correctamente, el paquete de autenticación crea una sesión de inicio de sesión y devuelve información a la [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) que se usa para crear un [*token*](../secgloss/t-gly.md) para el nuevo usuario. Este token incluye, entre otras cosas, un [*identificador local único*](../secgloss/l-gly.md) (LUID) para la sesión de inicio de sesión, denominado [*identificador de inicio de sesión*](../secgloss/l-gly.md).

Cuando se crea un token, se incrementa el [*recuento de referencias*](../secgloss/r-gly.md) de la sesión de inicio de sesión. El recuento de referencias también se incrementa siempre que se crean copias del token para la creación de procesos, la suplantación u otros usos. A medida que se completan los usos de los tokens y se eliminan las copias del token, se reduce el recuento de referencias de la sesión de inicio de sesión. Cuando el recuento de referencias llega a cero, se elimina la sesión de inicio de sesión.

> [!Note]  
> Si la autenticación no se realiza correctamente, el [*paquete de autenticación*](../secgloss/a-gly.md) no debe crear una sesión de inicio de sesión. Si el paquete de autenticación debe crear una sesión de inicio de sesión antes de realizar una determinación final sobre la validez del usuario y si se produce un error en la autenticación, el paquete de autenticación debe eliminar la sesión.

 

 

 
