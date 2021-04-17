---
description: La confirmación de acciones personalizadas se ejecuta cuando se completa correctamente el script de instalación.
ms.assetid: ad766585-e8ac-44b6-9717-7979f803886c
title: Confirmar acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174af16a84f71ff90a1fc35c76054ee503449b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666831"
---
# <a name="commit-custom-actions"></a>Confirmar acciones personalizadas

La confirmación de acciones personalizadas se ejecuta cuando se completa correctamente el script de instalación. Si la [acción InstallFinalize](installfinalize-action.md) es correcta, el instalador ejecutará las acciones personalizadas commit existentes. El único parámetro de modo que establece el instalador en este caso es MSIRUNMODE \_ commit. Consulte [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) para obtener una descripción de los parámetros de modo de ejecución.

Se puede especificar una acción personalizada commit agregando una marca de opción al campo Type de la [tabla CustomAction](customaction-table.md). Consulte [acción personalizada In-Script opciones de ejecución](custom-action-in-script-execution-options.md) para la marca de opción que designa una acción personalizada commit.

Una acción personalizada commit es el complemento de una [acción de reversión personalizada](rollback-custom-actions.md) y se puede usar con las acciones personalizadas de reversión para invertir acciones personalizadas que realizan cambios directamente en el sistema.

Tenga en cuenta que es posible que una acción personalizada de reversión no pueda quitar todos los cambios realizados por las acciones de confirmación personalizadas. Aunque el instalador escribe las acciones personalizadas de reversión y confirmación en el script de reversión, la confirmación de acciones personalizadas solo se ejecuta después de que el instalador haya procesado correctamente el script de instalación. La confirmación de acciones personalizadas son las primeras acciones que se ejecutan en el script de reversión. Si se produce un error en una acción personalizada commit, el instalador inicia la reversión, pero solo puede revertir las operaciones ya escritas en el script de reversión. Esto significa que, dependiendo de la acción personalizada commit, es posible que una operación de reversión no pueda deshacer los cambios realizados por la acción. Puede omitir los errores en confirmar acciones personalizadas mediante la creación de la acción personalizada para omitir los códigos de retorno.

Las acciones personalizadas de reversión y confirmación no se ejecutan cuando la reversión está deshabilitada. Si un autor de paquetes requiere estos tipos de acciones personalizadas para una instalación adecuada, deben usar la propiedad [**RollbackDisabled**](rollbackdisabled.md) en una condición que impida que la instalación continúe cuando la reversión está deshabilitada.

 

 



