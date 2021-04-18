---
description: A partir de Windows Installer 3,0, se pueden aplicar varias revisiones a un producto en un orden constante, independientemente del orden en el que se proporcionen las revisiones al sistema.
ms.assetid: 10af1857-d59f-490d-9b50-49619b1e892c
title: Instalar varias revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4edb8d085ede6aee81690bf67bd9c5e19780ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687136"
---
# <a name="installing-multiple-patches"></a>Instalar varias revisiones

A partir de Windows Installer 3,0, se pueden aplicar varias revisiones a un producto en un orden constante, independientemente del orden en el que se proporcionen las revisiones al sistema.

**Windows Installer 2,0:** No compatible. Windows Installer versiones anteriores a la versión 3,0 siempre instalan las revisiones en el orden en que se proporcionan al sistema.

**Windows Installer 3,0 y versiones posteriores:** El instalador puede usar la información proporcionada en la tabla [MsiPatchSequence](msipatchsequence-table.md) para determinar qué revisiones son aplicables al paquete de Windows Installer y en qué orden deben aplicarse las revisiones. Las aplicaciones pueden usar las funciones [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) y [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) .

La función [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) determina qué revisiones se aplican al paquete de Windows Installer y en qué secuencia. La función puede tener en cuenta las revisiones reemplazadas u obsoletas. Esta función no tiene en cuenta los productos o revisiones que están instalados en el sistema y que no se especifican en el conjunto.

La función de secuencia [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) puede determinar la mejor secuencia de aplicación para las revisiones en un producto instalado especificado. Esta función cuenta las revisiones que ya se han aplicado al producto y las cuentas para las revisiones obsoletas y reemplazadas.

Cuando el paquete de revisión no tiene una tabla de [MsiPatchSequence](msipatchsequence-table.md) , el instalador siempre aplica las revisiones en el orden en el que se proporcionan al sistema.

Cuando el paquete de revisión contiene una mezcla de revisiones con información de secuencia en la tabla [MsiPatchSequence](msipatchsequence-table.md) y algunas revisiones sin esta información, la versión 3,0 de Windows Installer secuencia las revisiones en el orden descrito en la sección siguiente: [secuenciación de revisiones](sequencing-patches.md).

Un paquete Windows Installer no puede instalar más de 127 revisiones al instalar o actualizar una aplicación. Cuando se necesitan muchas actualizaciones, se deben combinar y las revisiones obsoletas anteriores deben eliminarse de la secuencia de revisión.

Una revisión que no se debe utilizar se puede eliminar de la secuencia de revisión. Esto evita que se aplique la revisión cuando se aplica la revisión a la aplicación de destino. Esto es diferente a quitar una revisión que ya se ha aplicado a una aplicación. Para obtener más información acerca de cómo eliminar revisiones de la secuencia de revisión, consulte [eliminar revisiones](eliminating-patches.md). Para obtener información acerca de cómo quitar revisiones aplicadas, consulte [quitar revisiones](removing-patches.md).

Para ver un ejemplo de cómo Windows Installer aplica varias revisiones cuando todas tienen tablas [MsiPatchSequence](msipatchsequence-table.md) , consulte el ejemplo de aplicación de [revisiones múltiples](multiple-patching-example.md).

 

 



