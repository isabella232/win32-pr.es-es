---
description: A partir de Windows Installer 3,0, los autores pueden agregar información de secuencia de revisiones a la base de datos del paquete de revisiones en la tabla MsiPatchSequence.
ms.assetid: 9cdcb25f-2c3d-411e-9aae-bdd52df38a97
title: Secuenciar revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9cbd9aead596abfaeb50d972915bf4d618440d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279482"
---
# <a name="sequencing-patches"></a>Secuenciar revisiones

A partir de Windows Installer 3,0, los autores pueden agregar información de secuencia de revisiones a la base de datos del paquete de revisiones en la tabla [MsiPatchSequence](msipatchsequence-table.md) . El instalador puede usar esta información para determinar qué revisiones son aplicables a un paquete de instalación, para determinar la mejor secuencia de aplicación de revisiones y para instalar revisiones en un orden constante independiente del orden en el que se proporcionan al sistema.

**Windows Installer 2,0:** No compatible. Windows Installer versiones anteriores a Windows Installer 3,0 instalan revisiones en el orden en que se proporcionan al sistema independientemente de si contienen una tabla [MsiPatchSequence](msipatchsequence-table.md) .

Se requiere lo siguiente para usar la funcionalidad de secuenciación de revisiones.

-   Los [paquetes de revisión](patch-packages.md) (archivos. msp) deben tener una tabla [MsiPatchSequence](msipatchsequence-table.md) que contenga información de secuenciación. El instalador instala las revisiones que no tienen una tabla MsiPatchSequence en el orden en que se proporcionan al sistema.
-   Las revisiones se instalan con Windows Installer 3,0 o posterior.

Windows Installer versión 3,0 tiene las siguientes funciones que las aplicaciones pueden utilizar para determinar la mejor secuencia de aplicación de revisiones.

-   La función [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) toma una lista de revisiones y determina en qué secuencia se pueden aplicar a un producto instalado. Esta función cuenta para cualquier revisión o producto que ya se haya instalado en el sistema.
-   La función [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) toma una lista de revisiones y determina en qué secuencia se pueden aplicar a un producto instalado. Esta función no tiene en cuenta las revisiones o los productos que ya se han instalado en el sistema.

Windows Installer versión 3,0 puede aplicar varias revisiones a un producto en una sola instalación de aplicación de revisiones. El grupo de revisiones puede contener revisiones que incluyen información de secuencia de revisión (una tabla [MsiPatchSequence](msipatchsequence-table.md) ) y revisiones que no lo hacen. El Windows Installer instala los paquetes de revisión sin esta tabla en el orden en que se proporcionan al sistema. El instalador tiene en cuenta los paquetes de revisión que carecen de una tabla MsiPatchSequence, pero que se han marcado como revisiones obsoletas o reemplazadas por el método descrito en la sección siguiente.

Cuando Windows Installer versión 3,0 instala varias revisiones, sigue estos pasos para determinar la secuencia en la que se aplican las revisiones individuales al producto:

1.  Las revisiones instaladas sin una tabla [MsiPatchSequence](msipatchsequence-table.md) se colocan en la secuencia en el orden en que se aplicaron al producto. La primera revisión que se aplicó se coloca en primer lugar en la secuencia.
2.  Las nuevas revisiones sin una [tabla MsiPatchSequence](msipatchsequence-table.md) se colocan en la secuencia. Estas revisiones se aplican mediante la instalación de aplicación de revisiones actual. Se colocan en el orden en que se proporcionan al sistema y se colocan después de todas las revisiones del paso 1.
3.  Las revisiones obsoletas se eliminan de la secuencia de revisiones.
    > [!Note]  
    > Un paquete de revisión puede especificar en la propiedad [**Resumen del número de revisión**](revision-number-summary.md) una lista explícita de las revisiones obsoletas que va a quitar la revisión. Esta lista está pensada para su uso por parte de Windows Installer versiones anteriores a la versión 3,0. Windows Installer versión 3,0 quita las revisiones marcadas como obsoletas de la secuencia, solo si las revisiones no tienen la [tabla MsiPatchSequence](msipatchsequence-table.md).

     

4.  El instalador recorre la secuencia de aplicación de revisiones y determina qué revisiones se aplican en la secuencia especificada. Cuando se aplican varias revisiones a un producto, cada revisión de la secuencia transforma también la base de datos de instalación del producto (archivo. msi). Una revisión es aplicable en una secuencia determinada solo si su transformación de base de datos es capaz de tomar el [código del producto](product-codes.md), la [**versión**](productversion.md), el [**idioma**](productlanguage.md)y el [**UpgradeCode**](upgradecode.md) que resulta de aplicar las transformaciones de todos los [paquetes de revisión](patch-packages.md) anteriores a la base de datos del producto. El instalador elimina cualquier revisión no aplicable de la secuencia.
5.  El instalador comienza a colocar revisiones que tienen información de secuenciación en la tabla [MsiPatchSequence](msipatchsequence-table.md) . Las revisiones de [actualización secundarias](minor-upgrades.md) que tienen la tabla MsiPatchSequence se colocan en la secuencia después de las revisiones que se secuenciaron en pasos anteriores y en el orden de las versiones de producto más bajas a las más altas después de actualizarse. A continuación, Windows Installer elimina las revisiones de actualización secundarias que no son aplicables en esta secuencia.
6.  Las revisiones de [actualización pequeñas](small-updates.md) destinadas a [actualizaciones secundarias](minor-upgrades.md) que tienen una tabla [MsiPatchSequence](msipatchsequence-table.md) se asignan a la versión más alta de la revisión de actualización secundaria de la secuencia.
7.  Todas las revisiones de [actualización pequeñas](small-updates.md) que permanecen sin asignar después de los pasos anteriores, y que tienen la tabla [MsiPatchSequence](msipatchsequence-table.md) , se colocan en la secuencia antes de la primera [actualización secundaria](minor-upgrades.md) que tiene la tabla MsiPatchSequence y después de la base de datos de instalación. msi y cualquier revisión sin la tabla MsiPatchSequence. A continuación, Windows Installer elimina todas las revisiones de actualización pequeñas que no son aplicables en esta secuencia.
8.  Windows Installer versión 3,0 elimina las revisiones reemplazadas de la secuencia. Cuando una revisión sustituye a las revisiones que se producen antes en la secuencia de revisión, la revisión contiene todas las correcciones de los parches anteriores. Las revisiones anteriores ya no son necesarias. El Windows Installer requiere la información de la tabla [MsiPatchSequence](msipatchsequence-table.md) para eliminar las revisiones reemplazadas.
    > [!Note]  
    > Se deben crear revisiones destinadas a sustituir un conjunto anterior de revisiones para sustituir a las revisiones anteriores de todas las familias de revisiones. Las revisiones de [actualización pequeñas](small-updates.md) solo pueden sustituir a las pequeñas. Las actualizaciones [secundarias](minor-upgrades.md) pueden suplantar las pequeñas actualizaciones y otras actualizaciones secundarias.

     

9.  Las revisiones de [actualización pequeñas](small-updates.md) que incluyen tablas [MsiPatchSequence](msipatchsequence-table.md) , se ordenan en las versiones del producto según la información de secuenciación de las tablas MsiPatchSequence. Esto determina la secuencia de revisión final.

Una revisión que ya no se debe usar se puede eliminar de la secuencia de revisión. Para obtener más información sobre cómo eliminar revisiones de la secuencia de revisión, consulte [eliminar revisiones](eliminating-patches.md).

Para obtener un ejemplo de cómo se puede usar la tabla [MsiPatchSequence](msipatchsequence-table.md) para aplicar revisiones en el orden en el que se crearon, vea el ejemplo de aplicación de [revisiones múltiples](multiple-patching-example.md).

 

 



