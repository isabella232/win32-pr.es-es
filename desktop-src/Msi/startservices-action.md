---
description: La acción StartServices inicia los servicios del sistema. Esta acción consulta la tabla ServiceControl.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: Acción StartServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ff7b927eb4bc157530cebe9767ef7a434d92f0b72f9e6c799b02a2969f5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627535"
---
# <a name="startservices-action"></a>Acción StartServices

La acción StartServices inicia los servicios del sistema. Esta acción consulta la [tabla ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Las acciones de servicios deben usarse en la secuencia siguiente:

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



 

## <a name="remarks"></a>Comentarios

Esta acción requiere que el usuario sea administrador o tenga privilegios elevados con permiso para controlar los servicios o que la aplicación sea parte de una instalación administrada.

 

 



