---
description: Un mapa de valores es una matriz vinculada a una propiedad con los calificadores Value y ValueMap.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: Valores de ValueMap y calificadores de valor
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df85342df9543e4d62b04482785ec31bb5bd3982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706745"
---
# <a name="valuemap-and-value-qualifiers"></a>Valores de ValueMap y calificadores de valor

Un mapa de valores es una matriz vinculada a una propiedad con los calificadores **Value** y **ValueMap** .

La propiedad actúa como un índice en la matriz y contiene un valor que representa uno de los valores de la matriz. Con el código MOF, puede tener los siguientes tipos de asignaciones de valores:

-   Asignación de matriz a un entero.

    Puede definir una matriz con el calificador de **valor** y vincular la matriz directamente a una propiedad de entero, tal como se muestra en el ejemplo siguiente:

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    En este ejemplo, el valor de la propiedad **status** es un índice de la matriz de cadenas definida por **Value**. La propiedad solo puede tomar valores que correspondan a las posiciones ordinales de la matriz de **valores** menos 1. Por ejemplo, establecer el **Estado** en "1" se asigna al valor "error". La propiedad de índice solo puede aceptar valores que correspondan a posiciones de la matriz de **valores** . Por ejemplo, si la matriz tiene 10 entradas, la propiedad de índice puede tener la historia 0 a 9, no 30 o 177.

-   Asignación de matriz a otra matriz asignada a un entero.

    Si desea crear un índice que no use un sistema ordinal de recuento, use el calificador **ValueMap** . El calificador **ValueMap** configura otra matriz que contiene un sistema de numeración de índices arbitrario, tal como se muestra en el ejemplo siguiente:

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    Aunque debe colocar los valores de **ValueMap** entre comillas, WMI tiene en cuenta los valores enteros. Por lo tanto, en este ejemplo, puede establecer la propiedad **status** en un entero en **ValueMap** set: 1, 3, 99 o 0. WMI asigna cada entero de una posición ordinal de la matriz de cadenas **ValueMap** a la posición correspondiente en la matriz de **valores** . Por ejemplo, establecer el **Estado** en 0 se asigna a "Unknown".

-   Asignación de matriz a otra matriz asignada a una cadena.

    Si no desea utilizar un entero para indizar la matriz, en su lugar puede usar una cadena que contenga uno de los valores posibles de la matriz. Para ello, debe definir una matriz de **valores** y **ValueMap** que contengan cadenas, como se muestra en el ejemplo siguiente:

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    Con una propiedad de cadena, los valores reales permitidos de la propiedad son las entradas de la matriz **ValueMap** . Por ejemplo, puede establecer el **Estado** en "correcto" o "desconocido".

Depende de la aplicación aprovechar las asignaciones de una manera útil. Depende del proveedor aplicar un intervalo de valores válido.

## <a name="remarks"></a>Observaciones

A **la hora** de decidir si usar los / calificadores de **valor**  / de **BitValues** o de mapa de bits, determine si alguno de los valores que se indican podría producirse al mismo tiempo. Si pueden existir varios valores simultáneos, debe usar el **mapa de bits** / **BitValues**. Si todos los valores son mutuamente excluyentes, debe usar los  / calificadores de **valor** de ValueMap.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mapa de bits y BitValues](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



