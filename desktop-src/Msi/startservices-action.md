---
description: La acción StartServices inicia servicios del sistema. Esta acción consulta la tabla ServiceControl.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: Acción StartServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c150a8970c5852d9cfc53581290e792c00b628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677653"
---
# <a name="startservices-action"></a>Acción StartServices

La acción StartServices inicia servicios del sistema. Esta acción consulta la [tabla ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Las acciones de servicios se deben usar en la secuencia siguiente:

-   [StopServices](stopservices-action.md)
-   [DeleteServices](deleteservices-action.md)

Cualquiera de las siguientes acciones:

-   [InstallFiles](installfiles-action.md)
-   [RemoveFiles](removefiles-action.md)
-   [DuplicateFiles](duplicatefiles-action.md)
-   [MoveFiles](movefiles-action.md)
-   [PatchFiles](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [InstallServices](installservices-action.md)
-   StartServices

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Nombre para mostrar del servicio.      |
| \[2\] | Nombre del servicio.              |



 

## <a name="remarks"></a>Observaciones

Esta acción requiere que el usuario sea administrador o que tenga privilegios elevados con permiso para controlar los servicios o que la aplicación forme parte de una instalación administrada.

 

 



