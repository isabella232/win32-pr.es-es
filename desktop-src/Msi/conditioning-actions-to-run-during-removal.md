---
description: Hay dos maneras de crear la base de datos de instalación de Windows Installer de forma que solo se llame a una acción cuando se desinstale el paquete.
ms.assetid: 67b205bb-11d8-454f-b5d5-93330219f6cc
title: Acciones de acondicionamiento que se ejecutan durante la eliminación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0e84f21b42f569744af9b8a7a46bb1e3df7a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544886"
---
# <a name="conditioning-actions-to-run-during-removal"></a>Acciones de acondicionamiento que se ejecutan durante la eliminación

Hay dos maneras de crear la base de datos de instalación de forma que solo se llame a una acción cuando se desinstale el paquete:

-   Si la acción se secuencia después de la [acción InstallValidate](installvalidate-action.md) en la [tabla InstallExecuteSequence](installexecutesequence-table.md), el autor del paquete puede especificar una condición de Remove = "All" para la acción en la columna condition. Tenga en cuenta que no se garantiza que la propiedad [**Remove**](remove.md) se establezca en All durante la desinstalación antes de que el instalador ejecute la acción InstallValidate. Tenga en cuenta que en este caso se requieren marcas de comillas alrededor del valor.
-   Si la acción se secuencia después de la [acción CostFinalize](costfinalize-action.md) y cualquier acción que pudiera cambiar el estado de la característica, como la [acción MigrateFeatureStates](migratefeaturestates-action.md), la acción puede estar condicionada en el estado de una característica o componente determinado. Consulte [Sintaxis de la instrucción condicional](conditional-statement-syntax.md). Use esta opción para llamar a una acción durante la eliminación de una característica o componente determinado, que puede producirse fuera de la eliminación completa de la aplicación.

Tenga en cuenta que la propiedad [**installed**](installed.md) se puede usar en expresiones condicionales para determinar si un producto está instalado por equipo o para el usuario actual. Para determinar si el producto está instalado para un usuario diferente, Compruebe la propiedad [**ProductState**](productstate.md) .

Tenga en cuenta que las versiones anteriores de un producto pueden quitarse durante una actualización mediante la [acción RemoveExistingProducts](removeexistingproducts-action.md). En este caso, la [tabla de actualización](upgrade-table.md) también puede establecer la propiedad [**Remove**](remove.md) en ALL. Para determinar si una actualización está quitando un producto, Compruebe la propiedad [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) . El instalador solo establece esta propiedad cuando RemoveExistingProducts quita el producto. El instalador no establece la propiedad durante una desinstalación normal, como la eliminación con agregar o quitar programas.

 

 



