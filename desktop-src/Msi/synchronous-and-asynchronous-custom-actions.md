---
description: El Windows Installer procesa las acciones personalizadas como un subproceso independiente de la instalación principal.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Acciones personalizadas sincrónicas y asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067c5b40840269f3a0393faee8fe670f5e522c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677528"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a>Acciones personalizadas sincrónicas y asincrónicas

El Windows Installer procesa las acciones personalizadas como un subproceso independiente de la instalación principal. Durante la ejecución sincrónica de una acción personalizada, el instalador espera a que el subproceso de la acción personalizada se complete antes de continuar con la instalación principal. Durante la ejecución asincrónica, el instalador ejecuta la acción personalizada simultáneamente a medida que continúa la instalación actual. Por lo tanto, los autores de acciones personalizadas deben tener en cuenta todos los subprocesos asincrónicos que puedan estar realizando cambios en la base de datos de instalación entre las llamadas de función.

En concreto, las llamadas a [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) y [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) deben evitarse en acciones personalizadas asincrónicas. En su lugar, use [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) para obtener una ruta de acceso de destino. Las operaciones de base de datos masivas como las operaciones de importación, exportación y transformación deben evitarse en cualquier tipo de acción personalizada.

Las marcas de opciones se pueden establecer en el campo Type de la [tabla CustomAction](customaction-table.md) para especificar que los subprocesos de acción principal y personalizada se ejecuten de forma sincrónica o asincrónica. Vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).

El instalador solo puede ejecutar acciones [personalizadas de reversión](rollback-custom-actions.md) y acciones de [instalación simultáneas](concurrent-installations.md) como acciones personalizadas sincrónicas.

 

 



