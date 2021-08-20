---
description: Hay dos maneras de crear la base de Windows de instalación del instalador de forma que solo se llame a una acción cuando se desinstale el paquete.
ms.assetid: 67b205bb-11d8-454f-b5d5-93330219f6cc
title: Acciones de a acondicionador que se ejecutarán durante la eliminación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fa9596dd6868b105f87c795ad70b6edc5ebac96381ffcc2b8b951947c87568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144328"
---
# <a name="conditioning-actions-to-run-during-removal"></a>Acciones de a acondicionador que se ejecutarán durante la eliminación

Hay dos maneras de crear la base de datos de instalación de modo que solo se llame a una acción cuando se desinstale el paquete:

-   Si la acción se secuencia después de la acción [InstallValidate](installvalidate-action.md) en la tabla [InstallExecuteSequence](installexecutesequence-table.md), el autor del paquete puede especificar una condición de REMOVE="ALL" para la acción en la columna Condición . Tenga en cuenta [**que no se**](remove.md) garantiza que la propiedad REMOVE se establezca en ALL durante una desinstalación antes de que el instalador ejecute la acción InstallValidate. Tenga en cuenta que las comillas alrededor del valor ALL son necesarias en este caso.
-   Si la acción se secuencia después de la acción [CostFinalize](costfinalize-action.md) y cualquier acción que pueda cambiar el estado de la característica, como la acción [MigrateFeatureStates](migratefeaturestates-action.md), la acción puede estar condiciónda en el estado de una característica o componente determinados. Vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md) Use esta opción para llamar a una acción durante la eliminación de una determinada característica o componente, que puede producirse fuera de la eliminación completa de la aplicación.

Tenga en cuenta [**que la**](installed.md) propiedad Instalado se puede usar en expresiones condicionales para determinar si un producto está instalado por equipo o para el usuario actual. Para determinar si el producto está instalado para otro usuario, compruebe la [**propiedad ProductState.**](productstate.md)

Tenga en cuenta que la acción [RemoveExistingProducts](removeexistingproducts-action.md)puede quitar las versiones anteriores de un producto durante una actualización. En [este caso,](upgrade-table.md) la tabla Upgrade también [**puede establecer la**](remove.md) propiedad REMOVE en ALL. Para determinar si una actualización quita un producto, compruebe la [**propiedad UPGRADINGPRODUCTCODE.**](upgradingproductcode.md) El instalador solo establece esta propiedad cuando RemoveExistingProducts quita el producto. El instalador no establece la propiedad durante una desinstalación normal, como la eliminación con Agregar o quitar programas.

 

 



