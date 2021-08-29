---
description: La acción MsiConfigureServices configura un servicio para el sistema. Esta acción consulta las tablas MsiServiceConfig y MsiServiceConfigFailureActions.
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: Acción MsiConfigureServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f77bcb37514cc0e90cd9b3e4f65f184104a60a575f159e45391582cfed01c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945070"
---
# <a name="msiconfigureservices-action"></a>Acción MsiConfigureServices

La acción MsiConfigureServices configura un servicio para el sistema. Esta acción consulta las [tablas MsiServiceConfig](msiserviceconfig-table.md) y [MsiServiceConfigFailureActions.](msiserviceconfigfailureactions-table.md)

**[Windows instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Esta acción está disponible a partir de Windows Installer 5.0.

> [!IMPORTANT]
>
> Windows Los servicios proporcionan la capacidad de realizar automáticamente acciones predefinidas en respuesta a un error en un servicio. Para admitir la configuración  mediante programación de estas acciones de recuperación cuando se produce un error en un servicio, [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) se agregó a MSI en la versión MSI 5.0. Sin embargo, esta funcionalidad no funciona según lo previsto.
>
> Para solucionar este problema, un desarrollador de aplicaciones debe  usar la funcionalidad **Acción** personalizada de MSI para ejecutarsc.exey establecer las opciones de **recuperación** correctamente.

 

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Esta acción estándar debe usarse en la secuencia siguiente.

[StopServices](stopservices-action.md)

[DeleteServices](deleteservices-action.md)

Cualquiera de las siguientes acciones: [acciones InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles,](duplicatefiles-action.md) [MoveFiles,](movefiles-action.md) [PatchFiles](patchfiles-action.md)y [RemoveDuplicateFiles.](removeduplicatefiles-action.md)

[InstallServices](installservices-action.md)

MsiConfigureServices

[StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Comentarios

Esta acción requiere que el usuario sea administrador o tenga privilegios elevados con permiso para instalar servicios o que la aplicación sea parte de una instalación administrada.

 

 



