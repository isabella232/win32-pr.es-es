---
description: La acción DeleteServices detiene un servicio y quita su registro del sistema. Esta acción consulta la tabla ServiceControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Acción DeleteServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5fc22bbb0c11cd546f1ffbb9f3ad98e06efae3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360868"
---
# <a name="deleteservices-action"></a>Acción DeleteServices

La acción DeleteServices detiene un servicio y quita su registro del sistema. Esta acción consulta la [tabla ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Las acciones de servicios se deben usar en la secuencia siguiente:

1.  [StopServices](stopservices-action.md)
2.  DeleteServices
3.  Cualquiera de las siguientes acciones: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)y [RemoveDuplicateFiles](removeduplicatefiles-action.md) .
4.  [Acción InstallServices](installservices-action.md)
5.  [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Nombre para mostrar del servicio.      |
| \[2\] | Nombre del servicio.              |



 

## <a name="remarks"></a>Observaciones

Esta acción requiere que el usuario sea administrador o que tenga privilegios elevados con permiso para eliminar servicios o que la aplicación forme parte de una instalación administrada.

 

 



