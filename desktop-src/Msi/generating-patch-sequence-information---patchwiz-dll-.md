---
description: La versión de PATCHWIZ.DLL publicada con Windows Installer&\# 160; 3.0 puede generar automáticamente información de secuencia de revisiones y agregar a la tabla MsiPatchSequence una nueva revisión.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Generando información de secuencia de revisión (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff82166f33266a58cd3ef299b2546b04a94ebb14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002262"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a>Generando información de secuencia de revisión (PATCHWIZ.DLL)

La versión de [PATCHWIZ.DLL](patchwiz-dll.md) publicada con Windows Installer 3,0 puede generar automáticamente información de secuencia de revisiones y agregar a la [tabla MsiPatchSequence](msipatchsequence-table.md) una nueva revisión.

Establezca la \_ propiedad secuencia \_ \_ de generación de datos deshabilitada en 1 (uno) en la [tabla de propiedades](properties-table-patchwiz-dll-.md) del archivo. PCP para evitar la generación automática de información sobre la secuenciación de revisiones. Si esta propiedad no está presente, la información se genera y se agrega automáticamente.

Cuando se utiliza el [PATCHWIZ.DLL](patchwiz-dll.md) liberado con Windows Installer 3,0 para generar automáticamente la información de secuenciación de revisiones, ocurre lo siguiente:

-   Se agrega una nueva fila a la [tabla MsiPatchSequence](msipatchsequence-table.md) para cada código de producto de una imagen de destino que aparece en la [tabla TargetImages](targetimages-table-patchwiz-dll-.md).
-   Los valores agregados a la columna PatchFamily en las nuevas filas corresponden a los códigos de producto de destino de las imágenes de destino que se enumeran en la [tabla TargetImages](targetimages-table-patchwiz-dll-.md).
-   Los valores agregados a las columnas de secuencia en las nuevas filas se generan con la versión de producto más alta de destino de la revisión y la hora UTC en que se genera la revisión. El número de secuencia es <Product Minor Version> . <Build Major Number> . <marca de tiempo 1>. <la marca de tiempo 2>.
    -   El primer campo es la versión del producto de la versión más reciente del producto que es el destino de la revisión.
    -   El segundo campo es el número principal de la compilación de la versión más reciente del producto que es el destino de la revisión.

    Los dos campos de marca de tiempo tienen en cuenta la marca de tiempo de 32 bits necesaria para contar los segundos en la hora universal coordinada (UTC).
    > [!Note]  
    > Las versiones del producto tienen el siguiente formato: <Product Major Version> . <Product Minor Version> .. <Build Major Number> <Build Minor Number> y un producto con un número de versión 2.1.0.0 es una versión superior a un producto con el número de versión 1.2.0.0

     

-   El atributo msidbPatchSequenceSupersedeEarlier se especifica en la columna de atributos de las nuevas filas que se generan para Service Packs (SP) o revisiones de actualización secundarias. El atributo msidbPatchSequenceSupersedeEarlier no se agrega a una revisión de actualización pequeña o QFE.
    > [!Note]  
    > Un Service Pack (SP) debe contener las correcciones de todas las QFE publicadas anteriormente. Sin embargo, si el autor de una revisión establece la propiedad de sustitución de datos de secuencia \_ \_ en 0 (cero) o 1 (uno) en el archivo. PCP, la columna atributos de todas las filas de la tabla MsiPatchSequence se establece en el valor que se especifica para la sustitución de datos de secuencia \_ \_ . Los autores de revisiones que requieren más control deben crear manualmente la columna de atributos.

     

Si incluye una [tabla PatchSequence](patchsequence-table--patchwiz-dll-.md) en el archivo. PCP, \_ \_ se omite la propiedad generación de datos de secuencia \_ deshabilitada y se puede Agregar la información proporcionada en la tabla PatchSequence a la [tabla MsiPatchSequence](msipatchsequence-table.md) de la revisión.

 

 



