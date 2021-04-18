---
description: La acción MsiConfigureServices configura un servicio para el sistema. Esta acción consulta las tablas MsiServiceConfig y MsiServiceConfigFailureActions.
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: Acción MsiConfigureServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f2321bcdfaeede8e80d7f4c341f5a099690952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653107"
---
# <a name="msiconfigureservices-action"></a>Acción MsiConfigureServices

La acción MsiConfigureServices configura un servicio para el sistema. Esta acción consulta las tablas [MsiServiceConfig](msiserviceconfig-table.md) y [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) .

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Esta acción está disponible a partir de Windows Installer 5,0.

> [!IMPORTANT]
>
> Los servicios de Windows proporcionan la capacidad de realizar automáticamente acciones predefinidas en respuesta a un error en un servicio. Para admitir la configuración mediante programación de estas **acciones de recuperación** cuando se produce un error en un servicio, se ha agregado [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) a MSI en la versión MSI 5,0. Sin embargo, esta funcionalidad no funciona según lo esperado.
>
> Para solucionar este problema, un desarrollador de aplicaciones debe utilizar la funcionalidad de **acción personalizada** en MSI para ejecutar **sc.exe** y establecer las **Opciones de recuperación** de manera adecuada.

 

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Esta acción estándar se debe usar en la secuencia siguiente.

[StopServices](stopservices-action.md)

[DeleteServices](deleteservices-action.md)

Cualquiera de las siguientes acciones: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)y [RemoveDuplicateFiles](removeduplicatefiles-action.md) .

[InstallServices](installservices-action.md)

MsiConfigureServices

[StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

Esta acción requiere que el usuario sea administrador o que tenga privilegios elevados con permisos para instalar servicios o que la aplicación forme parte de una instalación administrada.

 

 



