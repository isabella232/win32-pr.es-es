---
description: La acción DeleteServices detiene un servicio y quita su registro del sistema. Esta acción consulta la tabla ServiceControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Acción DeleteServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd00b9d077239402817bdf40dc10ee1de9bdbff4b52998742434933c3e9dd8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379121"
---
# <a name="deleteservices-action"></a>Acción DeleteServices

La acción DeleteServices detiene un servicio y quita su registro del sistema. Esta acción consulta la [tabla ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Las acciones de servicios deben usarse en la secuencia siguiente:

1.  [StopServices](stopservices-action.md)
2.  DeleteServices
3.  Cualquiera de las siguientes acciones: [acciones InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles,](movefiles-action.md) [PatchFiles](patchfiles-action.md)y [RemoveDuplicateFiles.](removeduplicatefiles-action.md)
4.  [Acción InstallServices](installservices-action.md)
5.  [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Nombre para mostrar del servicio.      |
| \[2\] | Nombre del servicio.              |



 

## <a name="remarks"></a>Comentarios

Esta acción requiere que el usuario sea administrador o tenga privilegios elevados con permiso para eliminar servicios o que la aplicación sea parte de una instalación administrada.

 

 



