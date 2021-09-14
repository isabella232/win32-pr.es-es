---
description: Una revisión que ya no se debe usar se puede eliminar de la secuencia de aplicación de revisiones.
ms.assetid: b1d499d9-4fd3-4996-84a1-c32acefbb98f
title: Eliminación de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a705ce5919ffd36e6fc860403e11db56c6df1592
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158499"
---
# <a name="eliminating-patches"></a>Eliminación de revisiones

Una revisión que ya no se debe usar se puede eliminar de la secuencia de aplicación de revisiones. Esto evita que se aplique la revisión cuando se aplica la aplicación de destino. Esto es diferente de quitar una revisión que ya se ha aplicado a una aplicación. Para obtener información sobre cómo quitar revisiones aplicadas, vea [Quitar revisiones.](removing-patches.md)

**Windows Installer 3.0 y versiones posteriores: **

Las revisiones que tienen [la tabla MsiPatchSequence](msipatchsequence-table.md) pueden usar esta tabla para eliminar las revisiones de la secuencia de aplicación de revisiones. Una revisión puede eliminar las revisiones anteriores a ella en la secuencia de aplicación de revisiones y reemplazar la información de esas revisiones por su propia información. Tanto la revisión que especifica las revisiones que se deben eliminar como las revisiones que se eliminan deben tener una tabla MsiPatchSequence que contenga información.

Si las revisiones eliminadas y la revisión de reemplazo no tienen tablas [MsiPatchSequence,](msipatchsequence-table.md) el paquete de revisión puede especificar una lista de revisiones que se eliminarán de la secuencia de aplicación de revisiones en su propiedad Resumen del número de revisión. [](revision-number-summary.md) Windows El instalador 3.0 omite esta lista si las revisiones eliminadas o de reemplazo tienen una tabla MsiPatchSequence.

Cuando el paquete de revisión contiene revisiones con información de secuencia en la tabla [MsiPatchSequence](msipatchsequence-table.md) y algunas revisiones sin esta información, el instalador de Windows 3.0 secuencia las revisiones en el orden descrito en la sección siguiente: [Secuenciación](sequencing-patches.md)de revisiones .

Por ejemplo, Patch1, Patch2 y Patch3 pueden ser tres revisiones que no tienen la [tabla MsiPatchSequence.](msipatchsequence-table.md) Patch2 puede ser una revisión que solo es aplicable si Patch1 ya se ha aplicado a la aplicación. Patch3 puede ser una revisión posterior que tenga toda la información de Patch1 y también elimine Patch1 de la secuencia de aplicación de revisiones. Esto significa que cuando se aplica Patch3, la revisión 2 también se vuelve inaplicable, ya que requiere Patch1. Cualquier información de Patch2 por sí sola no se entrega a la aplicación.

**Windows Installer 2.0:** No se admite. El único método disponible es especificar la lista de revisiones que se eliminarán de la secuencia de aplicación de revisiones en la propiedad [**Resumen del**](revision-number-summary.md) número de revisión.

> [!Note]  
> Los autores de revisiones deben usar las funciones [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) y [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) para determinar la secuencia de revisiones que realmente se aplican al producto porque la eliminación de algunas revisiones puede hacer que otras revisiones no se puedan aplicar.

 

 

 



