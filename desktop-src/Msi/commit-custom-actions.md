---
description: Confirmar Acciones personalizadas se ejecutan una vez completado correctamente el script de instalación.
ms.assetid: ad766585-e8ac-44b6-9717-7979f803886c
title: Confirmar acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4226a126468df400e23c8eb59885b6e5a66c96d740c0c0e0959320697da293d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380319"
---
# <a name="commit-custom-actions"></a>Confirmar acciones personalizadas

Confirmar Acciones personalizadas se ejecutan una vez completado correctamente el script de instalación. Si la [acción InstallFinalize se](installfinalize-action.md) realiza correctamente, el instalador ejecutará las acciones commit custom existentes. El único parámetro de modo que establece el instalador en este caso es MSIRUNMODE \_ COMMIT. Consulte [**MsiGetMode para**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) obtener una descripción de los parámetros del modo de ejecución.

Se puede especificar una acción personalizada de confirmación agregando una marca de opción al campo Tipo de la [tabla CustomAction](customaction-table.md). Consulte [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md) (Opciones de ejecución de acciones personalizadas) para obtener la marca de opción que designa una acción personalizada de confirmación.

Una acción personalizada de confirmación es el complemento [de](rollback-custom-actions.md) una acción personalizada de reversión y se puede usar con acciones personalizadas de reversión para invertir acciones personalizadas que realicen cambios directamente en el sistema.

Tenga en cuenta que es posible que una acción personalizada de reversión no pueda quitar todos los cambios realizados mediante acciones personalizadas de confirmación. Aunque el instalador escribe acciones personalizadas de reversión y confirmación en el script de reversión, las acciones personalizadas de confirmación solo se ejecutan después de que el instalador haya procesado correctamente el script de instalación. Las acciones personalizadas de confirmación son las primeras que se ejecutan en el script de reversión. Si se produce un error en una acción personalizada de confirmación, el instalador inicia la reversión, pero solo puede revertir las operaciones ya escritas en el script de reversión. Esto significa que, en función de la acción personalizada de confirmación, es posible que una reversión no pueda deshacer los cambios realizados por la acción. Puede omitir los errores en las acciones personalizadas de confirmación mediante la creación de la acción personalizada para omitir los códigos de retorno.

Las acciones personalizadas de reversión y confirmación no se ejecutan cuando la reversión está deshabilitada. Si un autor del paquete requiere estos tipos de acciones personalizadas para una instalación adecuada, debe usar la propiedad [**RollbackDisabled**](rollbackdisabled.md) en una condición que impida que la instalación continúe cuando se deshabilite la reversión.

 

 



