---
description: Un administrador de credenciales es similar a un proveedor de red en que proporciona puntos de entrada a los que llama el enrutador de varios proveedores (MPR). De hecho, algunos proveedores de red también son administradores de credenciales.
ms.assetid: a1105754-a57f-4a0d-9797-bec22b99900c
title: Administrador de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20165a5e6145de0a2c042c38923c41d793bd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082878"
---
# <a name="credential-manager"></a>Administrador de credenciales

Un administrador de credenciales es similar a un proveedor de red en que proporciona puntos de entrada a los que llama el [*enrutador de varios proveedores*](/windows/desktop/SecGloss/m-gly) (MPR). De hecho, algunos proveedores de red también son administradores de credenciales.

Si implementa las funciones de administración de credenciales en el mismo archivo DLL que las funciones de proveedor de red dependen de los requisitos de la aplicación. Los administradores de credenciales reciben notificaciones cuando cambia la información de autenticación. Por ejemplo, se notifica a los administradores de credenciales cuando un usuario inicia sesión o cambia la contraseña de la cuenta. Cuando un proceso de inicio de sesión, como [*Winlogon*](/windows/desktop/SecGloss/w-gly), está en proceso de iniciar sesión o cambiar la contraseña de una cuenta, llama a la función de redes Windows (WNet) adecuada de mpr. A continuación, el MPR llama al punto de entrada adecuado para cada administrador de credenciales. Siempre se llamará a estas funciones de administración de credenciales en el contexto del sistema, LocalSystem, en lugar del contexto del usuario. Para obtener más información acerca de las funciones de WNet, consulte [redes de Windows](/windows/desktop/WNet/windows-networking-wnet-). Para obtener más información sobre la interfaz que los administradores de credenciales deben implementar, vea [**API de administración de credenciales**](credential-management-api.md).

 

 
