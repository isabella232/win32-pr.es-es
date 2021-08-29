---
description: A partir Windows Installer 3.0, los autores pueden agregar información de secuenciación de revisiones a la base de datos del paquete de revisión en la tabla MsiPatchSequence.
ms.assetid: 9cdcb25f-2c3d-411e-9aae-bdd52df38a97
title: Secuenciación de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f61a72c8122f9f3679cf691f88bc3d9bc952732b9d638ca838f9992068b1c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040015"
---
# <a name="sequencing-patches"></a>Secuenciación de revisiones

A partir Windows Installer 3.0, los autores pueden agregar información de secuenciación de revisiones a la base de datos del paquete de revisión [en la tabla MsiPatchSequence.](msipatchsequence-table.md) El instalador puede usar esta información para determinar qué revisiones son aplicables a un paquete de instalación, para determinar la mejor secuencia de aplicación de revisiones e instalar revisiones en un orden constante independiente del orden en que se proporcionan al sistema.

**Windows Installer 2.0:** No se admite. Windows Las versiones del instalador anteriores Windows Installer 3.0 instalan revisiones en el orden en que se proporcionan al sistema independientemente de si contienen una [tabla MsiPatchSequence.](msipatchsequence-table.md)

Los siguientes elementos son necesarios para usar la funcionalidad de secuenciación de revisiones.

-   [Los paquetes](patch-packages.md) de revisión (archivos .msp) deben tener una [tabla MsiPatchSequence](msipatchsequence-table.md) que contenga información de secuenciación. El instalador instala revisiones que no tienen una tabla MsiPatchSequence en el orden en que se proporcionan al sistema.
-   Las revisiones se instalan mediante Windows Installer 3.0 o posterior.

Windows La versión 3.0 del instalador tiene las siguientes funciones que las aplicaciones pueden usar para determinar la mejor secuencia de aplicación de revisiones.

-   La [**función MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) toma una lista de revisiones y determina en qué secuencia se pueden aplicar a un producto instalado. Esta función tiene en cuenta las revisiones o productos que ya se han instalado en el sistema.
-   La [**función MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) toma una lista de revisiones y determina en qué secuencia se pueden aplicar a un producto instalado. Esta función no tiene en cuenta ninguna revisión o producto que ya se haya instalado en el sistema.

Windows La versión 3.0 del instalador puede aplicar varias revisiones a un producto en una sola instalación de aplicación de revisiones. El grupo de revisiones puede contener revisiones que incluyen información de secuencia de revisión (una [tabla MsiPatchSequence)](msipatchsequence-table.md) y revisiones que no lo hacen. El Windows instala los paquetes de revisión sin esta tabla en el orden en que se proporcionan al sistema. El instalador tiene en cuenta los paquetes de revisión que carecen de una tabla MsiPatchSequence, pero que se han marcado como revisiones obsoletas o reemplazadas por el método descrito en la sección siguiente.

Cuando Windows Installer versión 3.0 instala varias revisiones, sigue estos pasos para determinar la secuencia en la que se aplican revisiones individuales al producto:

1.  Las revisiones instaladas sin [una tabla MsiPatchSequence](msipatchsequence-table.md) se ponen en la secuencia en el orden en que se aplicaron al producto. La primera revisión que se aplicó se coloca en primer lugar en la secuencia.
2.  Las nuevas revisiones sin [una tabla MsiPatchSequence](msipatchsequence-table.md) se ponen en la secuencia. La instalación de revisiones actual aplica estas revisiones. Se colocan en el orden en que se proporcionan al sistema y se colocan después de todas las revisiones del paso 1.
3.  Las revisiones obsoletas se eliminan de la secuencia de revisiones.
    > [!Note]  
    > Un paquete de revisión puede especificar en la propiedad [**Resumen**](revision-number-summary.md) del número de revisión una lista explícita de revisiones obsoletas que va a quitar la revisión. Esta lista está pensada para su uso por Windows Installer anteriores a la versión 3.0. Windows La versión 3.0 del instalador quita de la secuencia las revisiones marcadas como obsoletas, solo si las revisiones no tienen la [tabla MsiPatchSequence](msipatchsequence-table.md).

     

4.  El instalador pasa por la secuencia de aplicación de revisiones y determina qué revisiones son aplicables en la secuencia determinada. Cuando se aplican varias revisiones a un producto, cada revisión de la secuencia también transforma la base de datos de instalación del producto (.msi archivo). Una revisión solo es aplicable en una secuencia determinada si su [](productlanguage.md)transformación de [](upgradecode.md) base de datos es capaz de tomar [](patch-packages.md) el código de producto [,](product-codes.md)la versión [**,**](productversion.md)el idioma y el código de actualización resultantes de aplicar las transformaciones de todos los paquetes de revisión anteriores a la base de datos del producto. El instalador elimina las revisiones que no se pueden aplicar de la secuencia.
5.  El instalador comienza a colocar revisiones que tienen información de secuenciación en [su tabla MsiPatchSequence.](msipatchsequence-table.md) [](minor-upgrades.md) Las revisiones de actualización secundarias que tienen la tabla MsiPatchSequence se colocan en la secuencia después de las revisiones que se secuenciaron en pasos anteriores y en el orden de sus versiones de producto de menor a mayor nivel después de actualizarse. Windows A continuación, el instalador elimina las revisiones de actualización secundarias que no se pueden aplicar en esta secuencia.
6.  [Las revisiones de](small-updates.md) actualización pequeñas destinadas a actualizaciones [secundarias](minor-upgrades.md) que tienen una tabla [MsiPatchSequence](msipatchsequence-table.md) se asignan a la versión más alta de la revisión de actualización secundaria en la secuencia.
7.  Todas [](small-updates.md) las revisiones de actualización pequeñas que permanecen sin firma después de los pasos anteriores, y que [](minor-upgrades.md) tienen la tabla [MsiPatchSequence,](msipatchsequence-table.md) se ponen en la secuencia antes de la primera actualización secundaria que tiene la tabla MsiPatchSequence y después de la base de datos de instalación de .msi y las revisiones sin la tabla MsiPatchSequence. Windows A continuación, el instalador elimina las revisiones de actualización pequeñas que no se pueden aplicar en esta secuencia.
8.  Windows La versión 3.0 del instalador elimina las revisiones reemplazadas de la secuencia. Cuando una revisión reemplaza las revisiones que se producen anteriormente en la secuencia de revisión, la revisión contiene todas las correcciones de las revisiones anteriores. Las revisiones anteriores ya no son necesarias. El Windows requiere la información de la tabla [MsiPatchSequence](msipatchsequence-table.md) para eliminar las revisiones reemplazadas.
    > [!Note]  
    > Las revisiones diseñadas para sustituir un conjunto anterior de revisiones deben crearse para reemplazar las revisiones anteriores en todas las familias de revisiones. [Las revisiones de](small-updates.md) actualizaciones pequeñas solo pueden sustituir a actualizaciones pequeñas. [Las actualizaciones secundarias](minor-upgrades.md) pueden sustituir a las actualizaciones pequeñas y a otras actualizaciones secundarias.

     

9.  [Las revisiones](small-updates.md) de actualización pequeñas que llevan tablas [MsiPatchSequence](msipatchsequence-table.md) se secuencian dentro de las versiones del producto según la información de secuenciación de sus tablas MsiPatchSequence. Esto determina la secuencia de aplicación de revisiones final.

Una revisión que ya no se debe usar se puede eliminar de la secuencia de aplicación de revisiones. Para obtener más información sobre cómo eliminar revisiones de la secuencia de aplicación de revisiones, vea [Eliminación de revisiones.](eliminating-patches.md)

Para obtener un ejemplo de cómo se puede usar la tabla [MsiPatchSequence](msipatchsequence-table.md) para aplicar revisiones en el orden en que se crearon, vea [el](multiple-patching-example.md)ejemplo de varias revisiones .

 

 



