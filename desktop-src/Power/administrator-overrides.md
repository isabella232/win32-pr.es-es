---
description: Invalidaciones de administrador
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Invalidaciones de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667234"
---
# <a name="administrator-overrides"></a>Invalidaciones de administrador

Windows tiene una sola lista de control de acceso (ACL) predeterminada en todos los objetos de directiva de energía. La ACL concede permisos de lectura, escritura y modificación a los miembros del grupo usuarios autenticados. A todos los demás usuarios se les concede el permiso de solo lectura. Las aplicaciones que llaman a funciones de la Directiva de energía pueden determinar si un usuario tiene permisos para una configuración de energía especificada mediante la función [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) .

La configuración de energía se puede invalidar mediante directiva de grupo. Las invalidaciones se pueden establecer mediante la Directiva de grupo de dominio o la Directiva de grupo local. [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) informará si una configuración de energía especificada tiene una invalidación de directiva de grupo.

La herramienta de línea de comandos **PowerCfg.exe** muestra un mensaje de error cuando no se puede completar un comando porque el usuario no tiene permisos para cambiar la configuración de energía o porque la configuración de energía tiene una invalidación de directiva de grupo.

La aplicación opciones de energía del panel de control no admite la configuración de permisos de acceso a directivas de energía. El cambio de permisos debe realizarse a través de **PowerCfg.exe**.

 

 



