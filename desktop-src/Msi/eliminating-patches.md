---
description: Una revisión que ya no se debe usar se puede eliminar de la secuencia de revisión.
ms.assetid: b1d499d9-4fd3-4996-84a1-c32acefbb98f
title: Eliminar revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a705ce5919ffd36e6fc860403e11db56c6df1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652533"
---
# <a name="eliminating-patches"></a>Eliminar revisiones

Una revisión que ya no se debe usar se puede eliminar de la secuencia de revisión. Esto evita que se aplique la revisión cuando se aplica la revisión a la aplicación de destino. Esto es diferente a quitar una revisión que ya se ha aplicado a una aplicación. Para obtener información acerca de cómo quitar revisiones aplicadas, consulte [quitar revisiones](removing-patches.md).

* * Windows Installer 3,0 y versiones posteriores: * *

Las revisiones que tienen la tabla [MsiPatchSequence](msipatchsequence-table.md) pueden usar esta tabla para eliminar revisiones de la secuencia de revisión. Una revisión puede eliminar las revisiones que preceden en la secuencia de revisión y reemplazar la información de esas revisiones por su propia información. Tanto la revisión que especifica las revisiones que se van a eliminar como las revisiones que se eliminan deben tener una tabla MsiPatchSequence que contiene información.

Si las revisiones eliminadas y la revisión de sustitución no tienen tablas de [MsiPatchSequence](msipatchsequence-table.md) , el paquete de revisión puede especificar una lista de revisiones que se eliminarán de la secuencia de revisión en su propiedad de [**Resumen de número de revisión**](revision-number-summary.md) . Windows Installer 3,0 omite esta lista si las revisiones eliminadas o reemplazadas tienen una tabla MsiPatchSequence.

Cuando el paquete de revisión contiene revisiones con información de secuencia en la tabla [MsiPatchSequence](msipatchsequence-table.md) y algunas revisiones sin esta información, Windows Installer 3,0 secuencia las revisiones en el orden descrito en la sección siguiente: [secuenciación de revisiones](sequencing-patches.md).

Por ejemplo, Patch1, Patch2 y Patch3 pueden ser tres revisiones que no tienen la tabla [MsiPatchSequence](msipatchsequence-table.md) . Patch2 puede ser una revisión que solo es aplicable si ya se ha aplicado Patch1 a la aplicación. Patch3 puede ser una revisión posterior que tiene toda la información de Patch1 y también elimina Patch1 de la secuencia de revisión. Esto significa que, cuando se aplica Patch3, patch 2 también pasa a ser inaplicable, ya que requiere Patch1. Cualquier información de Patch2 independiente no se entrega a la aplicación.

**Windows Installer 2,0:** No compatible. El único método disponible es especificar la lista de revisiones que se van a eliminar de la secuencia de revisión en la propiedad [**Resumen del número de revisión**](revision-number-summary.md) .

> [!Note]  
> Los autores de revisiones deben usar las funciones [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) y [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) para determinar la secuencia de revisiones que se aplican realmente al producto, ya que la eliminación de algunas revisiones puede dejar inaplicables otras revisiones.

 

 

 



