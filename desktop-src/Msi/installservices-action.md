---
description: La acción InstallServices registra un servicio para el sistema. Esta acción consulta la tabla ServiceInstall.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Acción InstallServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072035"
---
# <a name="installservices-action"></a>Acción InstallServices

La acción InstallServices registra un servicio para el sistema. Esta acción consulta la [tabla ServiceInstall](serviceinstall-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción de servicios debe usarse en la secuencia siguiente.

[StopServices](stopservices-action.md)

[DeleteServices](deleteservices-action.md)

Cualquiera de las siguientes acciones: [acciones InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles,](movefiles-action.md) [PatchFiles](patchfiles-action.md)y [RemoveDuplicateFiles.](removeduplicatefiles-action.md)

InstallServices

[StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Observaciones

Esta acción requiere que el usuario sea administrador o tenga privilegios elevados con permiso para instalar servicios o que la aplicación sea parte de una instalación administrada.

 

 



