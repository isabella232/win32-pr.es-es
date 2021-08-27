---
title: Ejemplos de firmas raíz
description: En la sección siguiente se muestran las firmas raíz que varían en complejidad, de vacías a completamente llenas.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2332a6efb36b309c5dc74a8578a0be9d2f46298375c309872cae8718d5bc5950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529424"
---
# <a name="example-root-signatures"></a>Ejemplos de firmas raíz

En la sección siguiente se muestran las firmas raíz que varían en complejidad, de vacías a completamente llenas.

-   [Una firma raíz vacía](#an-empty-root-signature)
-   [Una constante](#one-constant)
-   [Agregar una vista raíz de búfer constante](#adding-a-root-constant-buffer-view)
-   [Tablas de descriptores de enlace](#binding-descriptor-tables)
-   [Una firma raíz más compleja](#a-more-complex-root-signature)
-   [Vistas de recursos del sombreador de streaming](#streaming-shader-resource-views)
-   [Temas relacionados](#related-topics)

## <a name="an-empty-root-signature"></a>Una firma raíz vacía

![una firma raíz vacía no tiene enlaces](images/root-tables-0.png)

Es poco probable que una firma raíz vacía sea útil, pero podría usarse en un paso de representación trivial con el uso solo del ensamblador de entrada y sombreadores de vértices y píxeles mínimos que no tienen acceso a ningún descriptor. También están disponibles las fases de combinación, destino de representación y galería de símbolos de profundidad, incluso con una firma raíz vacía.

## <a name="one-constant"></a>Una constante

![una constante raíz única](images/root-tables-constant.png)

La ranura de enlace de API es donde el argumento raíz de este parámetro se enlazará en el tiempo de registro de la lista de comandos. El número de ranuras de enlace de API es implícito, en función del orden de los parámetros de la firma raíz (la primera es siempre cero). La ranura de enlace HLSL es donde el sombreador verá que se muestra el parámetro raíz. El hardware no conoce el tipo ("uint" en el ejemplo anterior), pero es simplemente un comentario en la imagen; el hardware simplemente verá el DWORD único como contenido.

Para enlazar una constante en el tiempo de registro de la lista de comandos, se usaría un comando similar al siguiente:

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a>Agregar una vista raíz de búfer constante

![agrega una vista de búfer constante a la firma raíz](images/root-tables-cbv.png)

En este ejemplo se muestran dos constantes raíz y una vista raíz de búfer constante (CBV) que cuesta dos ranuras DWORD.

Para enlazar una vista de búfer constante, use un comando como el siguiente. Tenga en cuenta que el primer parámetro (2) es la ranura que se muestra en la imagen. Normalmente, se configurará una matriz de constantes y, a continuación, estará disponible para los sombreadores en b0 como CBV.

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a>Tablas de descriptores de enlace

![agrega tablas de descriptor a la firma raíz](images/root-tables-2.png)

En este ejemplo se muestra el uso de dos tablas de descriptores; uno que declara una tabla de cinco descriptores que estará disponible en tiempo de ejecución en un montón de descriptores UAV SRV de CBV y otro que declara una tabla de dos descriptores que se mostrarán en tiempo de ejecución en un montón de descriptores de \_ \_ sampler.

Para enlazar tablas de descriptores al grabar una lista de comandos.

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

Otra característica de la firma raíz es la constante raíz float4 que tiene cuatro DWORDS de tamaño. El siguiente comando enlaza solo las dos DWORDS centrales de las cuatro.

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a>Una firma raíz más compleja

![una firma raíz compleja con muchos elementos](images/root-tables-3.png)

En este ejemplo se muestra una firma raíz densa con la mayoría de los tipos de entradas. Dos de las tablas de descriptores (en las ranuras 3 y 6) incluyen matrices de tamaño sin enlazar. La carga aquí es que la aplicación solo toque descriptores válidos en un montón. Las matrices sin enlazar o muy grandes requieren el nivel de hardware 2+ de compatibilidad con el enlace de recursos.

Hay dos muestreadores estáticos (enlazados sin necesidad de ranuras de firma raíz).

En la ranura 9, UAV u4 y UAV u5 se declaran en el mismo desplazamiento de tabla de descriptores. Se usa un descriptor con alias, un descriptor en memoria se mostrará como u4 y u5 en los sombreadores HLSL. En este caso, el sombreador debe compilarse con la opción ALIAS MAY SHADER RESOURCES MAY de D3D10 o con la opción \_ \_ o en \_ \_ `/res_may_alias` FXC. Los descriptores con alias permiten enlazar un descriptor a varios puntos de enlace, sin tener que realizar ningún cambio en los sombreadores.

## <a name="streaming-shader-resource-views"></a>Vistas de recursos del sombreador de streaming

![vistas de recursos de sombreador de streaming en esta firma raíz](images/root-tables-4.png)

Esta firma raíz ilustra un escenario en el que todos los SRV se transmiten dentro y fuera de una matriz grande. En tiempo de ejecución, se puede establecer una tabla de descriptores una vez cuando se establece la firma raíz. A continuación, todas las lecturas de textura se realizan mediante la indexación en la matriz a través de constantes que se introducen a través de los primeros argumentos raíz. Solo se necesita un único montón de descriptores y solo se actualiza a medida que las texturas se transmiten dentro o fuera de las ranuras de descriptor libres.

Los desplazamientos del descriptor en el montón grande se identifican mediante sombreadores mediante las constantes de las vistas de búfer constante. Por ejemplo, si a un sombreador se le proporciona un identificador de material, puede indexar en la matriz grande mediante la constante para acceder al descriptor necesario (que hace referencia a la textura necesaria).

Este escenario requiere hardware con el nivel de enlace de recursos 2+.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Niveles de hardware de enlace de recursos](hardware-support.md)
</dt> <dt>

[Enlace de recursos en HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Firmas raíz](root-signatures.md)
</dt> </dl>

 

 




