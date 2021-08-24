---
description: El Windows procesa acciones personalizadas como un subproceso independiente de la instalación principal.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Acciones personalizadas sincrónicas y asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ffa9de75d81cfe0c824bab0580f0e6565567a187f768d99687169b47543a41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893615"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a>Acciones personalizadas sincrónicas y asincrónicas

El Windows procesa acciones personalizadas como un subproceso independiente de la instalación principal. Durante la ejecución sincrónica de una acción personalizada, el instalador espera a que se complete el subproceso de la acción personalizada antes de continuar con la instalación principal. Durante la ejecución asincrónica, el instalador ejecuta la acción personalizada simultáneamente a medida que continúa la instalación actual. Por lo tanto, los autores de acciones personalizadas deben tener en cuenta los subprocesos asincrónicos que pueden realizar cambios en la base de datos de instalación entre llamadas de función.

En concreto, las llamadas a [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) y [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) deben evitarse en acciones personalizadas asincrónicas. En su lugar, [**use MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) para obtener una ruta de acceso de destino. Las operaciones masivas de base de datos, como las operaciones de importación, exportación y transformación, deben evitarse en cualquier tipo de acción personalizada.

Las marcas de opción se pueden establecer en el campo Tipo de la [tabla CustomAction](customaction-table.md) para especificar que los subprocesos de acción principal y personalizado se ejecuten de forma sincrónica o asincrónica. Vea [Opciones de procesamiento de devolución de acciones personalizadas.](custom-action-return-processing-options.md)

El instalador solo puede ejecutar acciones personalizadas [de reversión y](rollback-custom-actions.md) acciones de [instalación](concurrent-installations.md) simultánea como acciones personalizadas sincrónicas.

 

 



