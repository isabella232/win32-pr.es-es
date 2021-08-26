---
description: A partir de Windows Installer 3.0, se pueden aplicar varias revisiones a un producto en un orden constante, independientemente del orden en que se proporcionan las revisiones al sistema.
ms.assetid: 10af1857-d59f-490d-9b50-49619b1e892c
title: Instalación de varias revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dc6b65997bd6bcb2b9f4c8da5022adda9a38b0b93401dc507397421799d260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893855"
---
# <a name="installing-multiple-patches"></a>Instalación de varias revisiones

A partir de Windows Installer 3.0, se pueden aplicar varias revisiones a un producto en un orden constante, independientemente del orden en que se proporcionan las revisiones al sistema.

**Windows Installer 2.0:** No se admite. Windows Las versiones del instalador anteriores a la versión 3.0 siempre instalan revisiones en el orden en que se proporcionan al sistema.

**Windows Installer 3.0 y versiones posteriores:** El instalador puede usar la información proporcionada en la tabla [MsiPatchSequence](msipatchsequence-table.md) para determinar qué revisiones son aplicables al paquete del instalador de Windows y en qué orden se deben aplicar las revisiones. Las aplicaciones pueden usar [**las funciones MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) y [**MsiDeterminePatchSequence.**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)

La [**función MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) determina qué revisiones se aplican al paquete Windows Installer y en qué secuencia. La función puede tener en cuenta las revisiones reemplazadas o obsoletas. Esta función no tiene en cuenta los productos o revisiones instalados en el sistema que no se especifican en el conjunto.

La [**función MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) Sequence puede determinar la mejor secuencia de aplicación para las revisiones a un producto instalado especificado. Esta función tiene en cuenta las revisiones que ya se han aplicado al producto y las revisiones obsoletas y reemplazadas.

Cuando el paquete de revisión no tiene una tabla [MsiPatchSequence,](msipatchsequence-table.md) el instalador siempre aplica las revisiones en el orden en que se proporcionan al sistema.

Cuando el paquete de revisión contiene una mezcla de revisiones con información de secuencia en la tabla [MsiPatchSequence](msipatchsequence-table.md) y algunas revisiones sin esta información Windows, la versión 3.0 del instalador secuencia las revisiones en el orden descrito en la sección siguiente: [Secuenciar revisiones](sequencing-patches.md).

Un Windows installer no puede instalar más de 127 revisiones al instalar o actualizar una aplicación. Cuando se necesitan muchas actualizaciones, se deben combinar y las revisiones obsoletas anteriores deben eliminarse de la secuencia de aplicación de revisiones.

Una revisión que no se debe usar se puede eliminar de la secuencia de aplicación de revisiones. Esto evita que se aplique la revisión cuando se aplica la aplicación de destino. Esto es diferente de quitar una revisión que ya se ha aplicado a una aplicación. Para obtener más información sobre cómo eliminar revisiones de la secuencia de aplicación de revisiones, vea [Eliminación de revisiones.](eliminating-patches.md) Para obtener información sobre cómo quitar las revisiones aplicadas, vea [Quitar revisiones.](removing-patches.md)

Para obtener un ejemplo de cómo Windows instalador aplica varias revisiones cuando todas tienen tablas [MsiPatchSequence,](msipatchsequence-table.md) vea [ejemplo de varias revisiones](multiple-patching-example.md).

 

 



