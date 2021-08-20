---
description: La versión de PATCHWIZ.DLL publicada con Windows Installer&160;3.0 puede generar automáticamente información de secuenciación de revisiones y agregar a la tabla \# MsiPatchSequence una nueva revisión.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Generar información de secuencia de revisión (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03094d9df26f4565db5b3a31c9a27c58a0bb45dac8aac93b2fefce34104d58c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947026"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a>Generar información de secuencia de revisión (PATCHWIZ.DLL)

La versión de [PATCHWIZ.DLL](patchwiz-dll.md) publicada con Windows Installer 3.0 puede generar automáticamente información de secuenciación de revisiones y agregar a la tabla [MsiPatchSequence](msipatchsequence-table.md) una nueva revisión.

Establezca la propiedad SEQUENCE DATA GENERATION DISABLED en \_ 1 (uno) en la Tabla de propiedades del archivo .csv para evitar la generación automática de información de \_ \_ secuenciación de revisiones. [](properties-table-patchwiz-dll-.md) Si esta propiedad no está presente, la información se genera y agrega automáticamente.

Cuando el [PATCHWIZ.DLL](patchwiz-dll.md) publicado con Windows Installer 3.0 se usa para generar automáticamente la información de secuenciación de revisiones, se produce lo siguiente:

-   Se agrega una nueva fila a la tabla [MsiPatchSequence para](msipatchsequence-table.md) cada código de producto de una imagen de destino que se muestra en [la tabla TargetImages](targetimages-table-patchwiz-dll-.md).
-   Los valores agregados a la columna PatchFamily de las nuevas filas corresponden a los códigos de producto de destino de las imágenes de destino que se enumeran en la [tabla TargetImages](targetimages-table-patchwiz-dll-.md).
-   Los valores agregados a las columnas Sequence de las nuevas filas se generan con la versión de producto más alta destinada por la revisión y la hora UTC cuando se genera la revisión. El número de secuencia es <Product Minor Version> <Build Major Number> . <marca de tiempo 1>.<marca de tiempo 2>.
    -   El primer campo es la versión del producto de la versión más alta del producto a la que se dirigirá la revisión.
    -   El segundo campo es el número principal de compilación de la versión más alta del producto a la que se dirigirá la revisión.

    Los dos campos de marca de tiempo tienen en cuenta la marca de tiempo de 32 bits necesaria para contar los segundos en hora universal coordinada (UTC).
    > [!Note]  
    > Las versiones del producto tienen el formato siguiente: . . . . y un producto con el número de versión 2.1.0.0 es una versión superior a la de un producto con el número de versión <Product Major Version> <Product Minor Version> <Build Major Number> <Build Minor Number> 1.2.0.0

     

-   El atributo msidbPatchSequenceSupersedeEarlier se especifica en la columna Atributo de las nuevas filas que se generan para Service Pack (SP) o revisiones de actualización secundarias. El atributo msidbPatchSequenceSupersedeEarlier no se agrega a una revisión de actualización pequeña o QFE.
    > [!Note]  
    > Un Service Pack (SP) debe contener las correcciones de todos los ASE que se publicaron antes. Sin embargo, si un autor de revisión establece la propiedad SEQUENCE DATA SUPERSEDENCE en 0 (cero) o 1 (uno) en el archivo .csv, la columna Attributes de todas las filas de la tabla \_ MsiPatchSequence se establece en el valor especificado para \_ SEQUENCE \_ DATA \_ SUPERSEDENCE. Los autores de revisiones que requieren más control deben crear la columna Atributos manualmente.

     

Si incluye una [tabla PatchSequence](patchsequence-table--patchwiz-dll-.md) en el archivo .csv, se omite la propiedad SEQUENCE DATA GENERATION DISABLED y se puede agregar la información proporcionada en la tabla PatchSequence a la tabla \_ \_ \_ [MsiPatchSequence](msipatchsequence-table.md) de la revisión.

 

 



