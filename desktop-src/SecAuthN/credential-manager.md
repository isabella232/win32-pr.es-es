---
description: Un administrador de credenciales es similar a un proveedor de red, ya que proporciona puntos de entrada a los que llama el enrutador de varios proveedores (MPR). De hecho, algunos proveedores de red también son administradores de credenciales.
ms.assetid: a1105754-a57f-4a0d-9797-bec22b99900c
title: Administrador de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20165a5e6145de0a2c042c38923c41d793bd641d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160996"
---
# <a name="credential-manager"></a>Administrador de credenciales

Un administrador de credenciales es similar a un proveedor de red, ya que proporciona puntos de entrada a los que llama el enrutador [*de varios*](/windows/desktop/SecGloss/m-gly) proveedores (MPR). De hecho, algunos proveedores de red también son administradores de credenciales.

Si implementa las funciones de administración de credenciales en el mismo archivo DLL que las funciones del proveedor de red depende de los requisitos de la aplicación. Los administradores de credenciales reciben notificaciones cuando cambia la información de autenticación. Por ejemplo, se notifica a los administradores de credenciales cuando un usuario inicia sesión o cambia una contraseña de cuenta. Cuando un proceso de inicio de sesión, como [*Winlogon,*](/windows/desktop/SecGloss/w-gly)está en proceso de iniciar sesión o de cambiar la contraseña de una cuenta, llama a la función mpr Windows networking (WNet) adecuada. A continuación, MPR llama al punto de entrada adecuado para cada administrador de credenciales. Estas funciones de administración de credenciales siempre se llamarán en el contexto del sistema, LocalSystem, en lugar del contexto de usuario. Para obtener más información sobre las funciones de WNet, [vea Windows Networking](/windows/desktop/WNet/windows-networking-wnet-). Para obtener más información sobre la interfaz que deben implementar los administradores de credenciales, vea [**Credential API de Administración**](credential-management-api.md).

 

 
