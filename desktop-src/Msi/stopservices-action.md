---
description: La acción StopServices detiene los servicios del sistema. Esta acción consulta la tabla ServiceControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Acción StopServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee0082d1588c3a1486b51bd4f06869374e1f6babfa71d309d65512e1ff1b0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627385"
---
# <a name="stopservices-action"></a>Acción StopServices

La acción StopServices detiene los servicios del sistema. Esta acción consulta la [tabla ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Las acciones de servicios deben usarse en la secuencia siguiente:

-   StopServices
-   [DeleteServices](deleteservices-action.md)

Cualquiera de las siguientes acciones:

-   [InstallFiles](installfiles-action.md)
-   [RemoveFiles](removefiles-action.md)
-   [DuplicateFiles](duplicatefiles-action.md)
-   [MoveFiles](movefiles-action.md)
-   [PatchFiles](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [InstallServices](installservices-action.md)
-   [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Nombre para mostrar del servicio.      |
| \[2\] | Nombre del servicio.              |



 

## <a name="remarks"></a>Comentarios

Esta acción requiere que el usuario sea administrador o tenga privilegios elevados con permiso para controlar los servicios o que la aplicación sea parte de una instalación administrada.

 

 



