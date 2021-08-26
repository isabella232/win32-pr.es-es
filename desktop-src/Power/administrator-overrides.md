---
description: Invalidaciones de administrador
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Invalidaciones de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af73f6d6fe3fe7d4edb8272c4d39c385a84973e4a3263c448505f5235adec855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033025"
---
# <a name="administrator-overrides"></a>Invalidaciones de administrador

Windows tiene una única lista de control de acceso (ACL) predeterminada en todos los objetos de directiva de energía. La ACL concede permisos de lectura, escritura y cambio a los miembros del grupo Usuarios autenticados. A todos los demás usuarios se les concede permiso de solo lectura. Las aplicaciones que llaman a funciones de directiva de energía pueden determinar si un usuario tiene permisos para una configuración de energía especificada mediante la [**función PowerSettingAccessCheck.**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck)

La configuración de energía se puede invalidar mediante directiva de grupo. Las invalidaciones se pueden establecer a través de la directiva de grupo de dominio o la directiva de grupo local. [**PowerSettingAccessCheck informa si**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) una configuración de energía especificada tiene una invalidación de directiva de grupo.

La herramienta de línea de **comandosPowerCfg.exe** muestra un mensaje de error cuando no se puede completar un comando porque el usuario no tenía permisos para cambiar la configuración de energía o porque la configuración de energía tiene una invalidación de directiva de grupo.

La Opciones de energía en Panel de control no proporciona compatibilidad para configurar los permisos de acceso de la directiva de energía. El cambio de permisos debe realizarse a **travésPowerCfg.exe**.

 

 



