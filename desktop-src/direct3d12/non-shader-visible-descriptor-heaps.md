---
title: Montones de descriptores no visibles por el sombreador
description: Los sombreadores no pueden hacer referencia a algunos montones de descriptores a través de tablas de descriptores, pero existen para ayudar a la aplicación a almacenamiento provisional de los descriptores antes de grabar una lista de comandos o porque no se requiere ningún montón visible del sombreador.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51d30c7a99250ee0842b79d76ccebb6150bcf9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072937"
---
# <a name="non-shader-visible-descriptor-heaps"></a>Montones de descriptores no visibles por el sombreador

Los sombreadores no pueden hacer referencia a algunos montones de descriptores a través de tablas de descriptores, pero existen para ayudar a la aplicación a almacenamiento provisional de los descriptores antes de grabar una lista de comandos o porque no se requiere ningún montón visible del sombreador.

-   [Vistas no visibles](#non-visible-views)
-   [Resumen](#summary)
-   [Temas relacionados](#related-topics)

## <a name="non-visible-views"></a>Vistas no visibles

Todos los montones de descriptores, incluidos los montones de descriptores accesibles del sombreador descritos anteriormente, se pueden manipular mediante la CPU o las listas de comandos en función del grupo de memoria y las propiedades de acceso a la CPU que seleccione la aplicación para un montón de descriptores.

En el caso de los [montones de descriptores visibles del](shader-visible-descriptor-heaps.md)sombreador, la razón obvia para denegar el acceso del sombreador a estos montones de descriptores es mientras se están montados. A continuación, estos montones se hacen visibles para el sombreador y se accede a ellos a través de tablas de descriptores en la ejecución de la lista de comandos. Sin embargo, no hay ningún requisito para la fase de los montones visibles del sombreador, ya que se pueden rellenar directamente.

Otros descriptores se enlazan a la canalización haciendo que su contenido se grabe directamente en la lista de comandos. Estos descriptores solo sirven para traducir los parámetros de vista en el tiempo de registro de la lista de comandos. Estos montones siempre son visibles sin sombreador y contienen lo siguiente.

-   Representar vistas de destino (RTV)
-   Vistas de galería de símbolos de profundidad (DSV)

Las vistas de búfer de índice (IBV), las vistas de búfer de vértice (VBV) y las vistas de salida de flujo (SOV) se pasan directamente a los métodos de API, no tienen tipos de montón específicos.

Después de grabar en la lista de comandos (con una llamada como [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), por ejemplo), la memoria usada para contener los descriptores de esta llamada está disponible inmediatamente para volver a usarse después de la llamada.

Incluso las tablas de descriptores tienen opciones en las que una aplicación puede permitir que la implementación elija registrar el contenido de la tabla en la grabación de la lista de comandos (en lugar de desreferenciar el puntero de tabla en la ejecución).

## <a name="summary"></a>Resumen



|                   | Sombreador visible, solo escritura de CPU                                   | No visible el sombreador, lectura y escritura de CPU                                       |
|-------------------|------------------------------------|----------------------------------------|
| **CBV, SRV, UAV** | sí                                | sí                                    |
| **SAMPLER**       | sí                                | sí                                    |
| **RTV**           | No                                 | sí                                    |
| **DSV**           | No                                 | sí                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> </dl>

 

 




