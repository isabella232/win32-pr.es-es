---
title: Firmas raíz de ejemplo
description: En la siguiente sección se muestran firmas raíz que varían en complejidad de vacío a completo.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d09d355cc1c96d77670c5536400f0b3f93c097
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104010"
---
# <a name="example-root-signatures"></a>Firmas raíz de ejemplo

En la siguiente sección se muestran firmas raíz que varían en complejidad de vacío a completo.

-   [Una firma raíz vacía](#an-empty-root-signature)
-   [Una constante](#one-constant)
-   [Agregar una vista de búfer de constantes raíz](#adding-a-root-constant-buffer-view)
-   [Enlazar Tablas de descriptores](#binding-descriptor-tables)
-   [Una firma raíz más compleja](#a-more-complex-root-signature)
-   [Vistas de recursos del sombreador de streaming](#streaming-shader-resource-views)
-   [Temas relacionados](#related-topics)

## <a name="an-empty-root-signature"></a>Una firma raíz vacía

![una firma raíz vacía no tiene enlaces](images/root-tables-0.png)

Una firma raíz vacía no es probable que sea útil, pero se puede usar en un paso de representación trivial con el uso solo del ensamblador de entrada, y los sombreadores de vértices y píxeles mínimos que no tienen acceso a ningún descriptor. También están disponibles la fase de mezcla, el destino de representación y las fases de estarcido de profundidad, incluso con una firma raíz vacía.

## <a name="one-constant"></a>Una constante

![una constante raíz única](images/root-tables-constant.png)

La ranura de enlace de la API es donde el argumento raíz para este parámetro se enlazará en la hora del registro de la lista de comandos. El número de ranuras de enlace de API es implícito, según el orden de los parámetros en la signatura raíz (el primero es siempre cero). La ranura de enlace HLSL es donde el sombreador verá el parámetro raíz que se muestra. El tipo ("uint" en el ejemplo anterior) no es conocido por el hardware, pero solo es un Comentario de la imagen, el hardware simplemente verá el único valor DWORD como contenido.

Para enlazar una constante en el momento del registro de la lista de comandos, se utilizaría un comando similar al siguiente:

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a>Agregar una vista de búfer de constantes raíz

![agrega una vista de búfer de constantes a la firma raíz.](images/root-tables-cbv.png)

En este ejemplo se muestran dos constantes raíz y una vista de búfer de constantes raíz (CBV) que cuesta dos ranuras DWORD.

Para enlazar una vista de búfer de constantes, use un comando como el siguiente. Tenga en cuenta que el primer parámetro (2) es la ranura que se muestra en la imagen. Normalmente, se configurará una matriz de constantes y, a continuación, estará disponible para los sombreadores en B0 como CBV.

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a>Enlazar Tablas de descriptores

![agrega tablas de descriptores a la firma raíz](images/root-tables-2.png)

En este ejemplo se muestra el uso de dos tablas de descriptores; una que declara una tabla de cinco descriptores que estará disponible en tiempo de ejecución en un \_ montón de \_ descriptor de CBV SRV UAV y otro que declare una tabla de dos descriptores que se mostrarán en tiempo de ejecución en un montón de descriptores de muestra.

Para enlazar las tablas de descriptor al grabar una lista de comandos.

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

Otra característica de la firma raíz es la constante raíz FLOAT4 que tiene un tamaño de cuatro DWORD. El comando siguiente enlaza solo los dos DWORDs centrales de los cuatro.

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a>Una firma raíz más compleja

![una firma raíz compleja con muchos elementos](images/root-tables-3.png)

En este ejemplo se muestra una firma raíz densa con la mayoría de los tipos de entradas. Dos de las tablas de descriptor (en las ranuras 3 y 6) incluyen matrices de tamaño sin enlazar. La carga aquí está en la aplicación para que solo se toquen los descriptores válidos en un montón. Las matrices sin enlazar o de gran tamaño requieren el nivel de hardware 2 y la compatibilidad con enlaces de recursos.

Hay dos muestras estáticas (enlazadas sin necesidad de espacios de firma raíz).

En la ranura 9, UAV U4 y UAV U5 se declaran en el mismo desplazamiento de la tabla de descriptores. Este es el uso de un descriptor con alias, un descriptor en la memoria se mostrará como U4 y U5 en los sombreadores de HLSL. En este caso, el sombreador se debe compilar con la \_ \_ opción de alias D3D10 de los recursos del sombreador \_ \_ y la `/res_may_alias` opción o en FXC. Los descriptores con alias permiten enlazar un descriptor a varios puntos de enlace, sin tener que realizar ningún cambio en los sombreadores.

## <a name="streaming-shader-resource-views"></a>Vistas de recursos del sombreador de streaming

![vistas de recursos del sombreador de streaming en esta firma raíz](images/root-tables-4.png)

Esta firma raíz muestra un escenario en el que todos los SRVs se transmiten dentro y fuera de una matriz grande. En tiempo de ejecución, se puede establecer una tabla de descriptor una vez cuando se establece la firma raíz. Después, todas las lecturas de textura se realizan mediante la indexación en la matriz a través de constantes que se introducen a través de los primeros argumentos raíz. Solo se necesita un montón de descriptor y solo se actualiza a medida que las texturas se transmiten dentro o fuera de las ranuras descriptoras libres.

Los desplazamientos del descriptor en el montón grande se identifican mediante sombreadores que usan las constantes en las vistas de búfer de constantes. Por ejemplo, si un sombreador recibe un identificador de material, puede indizar en la matriz de gran tamaño mediante la constante para tener acceso al descriptor necesario (que hace referencia a la textura necesaria).

Este escenario requiere hardware con enlace de recursos Tier2 +.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Niveles de hardware de enlace de recursos](hardware-support.md)
</dt> <dt>

[Enlace de recursos en HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Firmas raíz](root-signatures.md)
</dt> </dl>

 

 




