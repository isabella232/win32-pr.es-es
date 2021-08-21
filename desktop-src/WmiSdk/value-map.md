---
description: Un mapa de valores es una matriz vinculada a una propiedad con los calificadores Value y ValueMap.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: Calificadores ValueMap y Value
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 34b95b540a99dfaecefcbe0b87e817fd0c44c58606921046476b3411cdd256e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107384"
---
# <a name="valuemap-and-value-qualifiers"></a>Calificadores ValueMap y Value

Un mapa de valores es una matriz vinculada a una propiedad con los calificadores **Value** **y ValueMap.**

La propiedad actúa como índice en la matriz, con un valor que representa uno de los valores de la matriz. Con el código MOF, puede tener los siguientes tipos de asignaciones de valores:

-   Asignación de matriz a un entero.

    Puede definir una matriz con el calificador **Value** y vincular la matriz directamente a una propiedad de entero, como se muestra en el ejemplo siguiente:

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    En este ejemplo, el **valor de la propiedad Status** es un índice en la matriz de cadenas definida por **Value**. La propiedad solo puede tomar valores que se correspondan con las posiciones ordinales de la **matriz Value** menos 1. Por ejemplo, si **establece Estado** en "1", se asigna al valor "Error". La propiedad index solo puede tomar valores que se correspondan con las posiciones de la **matriz Value.** Por ejemplo, si la matriz tiene 10 entradas, la propiedad de índice puede tener entre 0 y 9, no 30 ni 177.

-   Asignación de matriz a otra asignación de matriz a un entero.

    Si desea crear un índice que no use un sistema ordinal de recuento, use el **calificador ValueMap.** El **calificador ValueMap** configura otra matriz que contiene un sistema arbitrario de numeración de índices, como se muestra en el ejemplo siguiente:

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    Aunque debe colocar los valores de **ValueMap** entre comillas, WMI tiene en cuenta los valores enteros. Por lo tanto, en este ejemplo puede establecer la propiedad **Status** en un entero en el conjunto **ValueMap:** 1, 3, 99 o 0. WMI asigna cada entero de una posición ordinal de la matriz de **cadenas ValueMap** a una posición correspondiente en la **matriz Value.** Por ejemplo, si **establece Estado** en 0, se asigna a "Desconocido".

-   Asignación de matriz a otra asignación de matriz a una cadena.

    Si no desea usar un entero para indexar la matriz, en su lugar puede usar una cadena para contener uno de los valores posibles de la matriz. Para ello, debe definir una matriz **Value** **y ValueMap** que contengan cadenas, como se muestra en el ejemplo siguiente:

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    Con una propiedad de cadena, los valores permitidos reales de la propiedad son las entradas de la **matriz ValueMap.** Por ejemplo, puede establecer Estado **en** "Aceptar" o "Desconocido".

La aplicación debe aprovechar las asignaciones de una manera útil. Es el proveedor el que debe aplicar un intervalo legal de valores.

## <a name="remarks"></a>Comentarios

Para decidir si se deben usar los calificadores **ValueMap** Value o /   / **BitMap BitValues,** determine si alguno de los valores que se indican podría producirse simultáneamente. Si pueden existir varios valores simultáneos, debe usar **BitMap** / **BitValues**. Si todos los valores son mutuamente excluyentes, debe usar los calificadores **ValueMap** / **Value.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[BitMap y BitValues](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



