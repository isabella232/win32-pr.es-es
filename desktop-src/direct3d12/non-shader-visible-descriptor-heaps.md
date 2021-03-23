---
title: Montones de descriptor visibles sin sombreador
description: Los sombreadores no pueden hacer referencia a algunos montones de descriptor a través de tablas de descriptores, pero existen para ayudar a la aplicación a ensayar los descriptores antes de grabar una lista de comandos o porque no se requiere ningún montón visible del sombreador.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894640cde142f1241b088518ba7140ffb9405152
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104549097"
---
# <a name="non-shader-visible-descriptor-heaps"></a>Montones de descriptor visibles sin sombreador

Los sombreadores no pueden hacer referencia a algunos montones de descriptor a través de tablas de descriptores, pero existen para ayudar a la aplicación a ensayar los descriptores antes de grabar una lista de comandos o porque no se requiere ningún montón visible del sombreador.

-   [Vistas no visibles](#non-visible-views)
-   [Resumen](#summary)
-   [Temas relacionados](#related-topics)

## <a name="non-visible-views"></a>Vistas no visibles

Todos los montones de descriptor, incluidos los montones de descriptor accesible del sombreador descritos anteriormente, se pueden manipular mediante las listas de comandos y de CPU en función de las propiedades del bloque de memoria y el acceso a la CPU que la aplicación selecciona para un montón de descriptores.

En el caso de los [montones de descriptor visibles del sombreador](shader-visible-descriptor-heaps.md), el motivo obvio para denegar el acceso del sombreador a estos montones descriptores es mientras se almacenan provisionalmente. Después, estos montones se hacen visibles para el sombreador y se obtiene acceso a ellos a través de las tablas de descriptor en la ejecución de la lista de comandos. Sin embargo, no hay ningún requisito para almacenar en fases los montones visibles del sombreador, sino que se pueden rellenar directamente.

Otros descriptores se enlazan a la canalización haciendo que su contenido se grabe directamente en la lista de comandos. Estos descriptores solo sirven para traducir los parámetros de la vista en la hora del registro de la lista de comandos. Estos montones siempre son visibles sin sombreador y contienen lo siguiente.

-   Vistas de destino de representación (RTVs)
-   Vistas de estarcido de profundidad (DSV)

Las vistas de búfer de índice (IBVs), las vistas de búfer de vértices (VBVs) y las vistas de salida de secuencias (SOVs) se pasan directamente a los métodos de la API, no tienen tipos de montón concretos.

Después de grabar en la lista de comandos (con una llamada como [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), por ejemplo) la memoria usada para contener los descriptores de esta llamada está disponible inmediatamente para su reutilización después de la llamada.

Incluso las tablas de descriptores tienen opciones donde una aplicación puede permitir que la implementación elija registrar el contenido de la tabla en la grabación de la lista de comandos (en lugar de desreferenciar el puntero de tabla en ejecución).

## <a name="summary"></a>Resumen



|                   |                                    |                                        |
|-------------------|------------------------------------|----------------------------------------|
|                   | **sombreador visible, solo escritura de CPU** | **sin sombreador visible, lectura de CPU/escritura** |
| **CBV, SRV, UAV** | sí                                | sí                                    |
| **MUESTRAS**       | sí                                | sí                                    |
| **RTV**           | no                                 | sí                                    |
| **VISTA**           | no                                 | sí                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> </dl>

 

 




