---
title: Predication
description: Predication es una característica que permite que la GPU en lugar de la CPU determine no dibujar, copiar o enviar un objeto.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2020
ms.locfileid: "104549157"
---
# <a name="predication"></a>Predication

Predication es una característica que permite que la GPU en lugar de la CPU determine no dibujar, copiar o enviar un objeto.

-   [Información general](#overview)
-   [SetPredication](#setpredication)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

El uso típico de predication es con oclusión; Si se dibuja un cuadro de límite y es ocluidos, obviamente no hay ningún punto en el dibujo del propio objeto. En esta situación, se puede "predicar" el dibujo del objeto, lo que permite su eliminación de la representación real por parte de la GPU.

En primer lugar, esto podría parecer redudant y por encima de la prueba de profundidad estándar más un paso de profundidad temprana. Sin embargo, predication puede quitar la sobrecarga del estado del comando Draw en sí, además de la rasterización. Aunque una fase de profundidad temprana quita los píxeles innecesarios, todavía puede ejecutar sombreadores de vértices, de casco, de dominio y de geometría, e invocar el ensamblador de entrada de función fija, tesselator y rasterizador. Al dibujar un rectángulo de selección simple o un volumen de límite similar &mdash; que sea más fácil de procesar y Rasterizar que el modelo real &mdash; , se evita la rasterización y el procesamiento innecesarios.

A diferencia de Direct3D 11, predication está desacoplado de las consultas y se expande en Direct3D 12 para permitir que una aplicación Predicate objetos en función de la razón por la que el desarrollador de la aplicación puede decidir (no solo oclusión).

## <a name="setpredication"></a>SetPredication

Predication se puede establecer en función del valor de 64 bits dentro de un búfer (consulte [**D3D12 \_ Predication \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).

Cuando la GPU ejecuta un comando [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) , ajusta el valor en el búfer. Los cambios futuros en los datos del búfer no afectan al estado predication.

Si el búfer de parámetros de entrada es NULL, predication está deshabilitado.

Las sugerencias de Predication no están presentes en la API de Direct3D 12. y predication se permiten en las listas de comandos Direct, Compute y Copy. El búfer de origen puede estar en cualquier tipo de montón (valor predeterminado, cargar, readback, personalizado).

El entorno de tiempo de ejecución principal validará lo siguiente:

-   *AlignedBufferOffset* es un múltiplo de 8 bytes
-   El recurso es un búfer
-   La operación es un miembro válido de la enumeración
-   No se puede llamar a [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) desde una agrupación
-   El tipo de lista de comandos admite predication
-   El desplazamiento no supera el tamaño del búfer

La capa de depuración emitirá un error si el búfer de origen no está en el [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (que es igual que [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)y simplemente un alias).

El conjunto de operaciones que se pueden predicar es:

-   [**DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [**ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [**ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) no está predicado a sí mismo. En su lugar, se predican las operaciones individuales de la lista anterior que se encuentran en el lado de la agrupación.

No se predican los métodos ID3D12GraphicsCommandList [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) y [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contadores y consultas](counters-and-queries.md)
</dt> <dt>

[Medición del rendimiento](performance-measurement.md)
</dt> <dt>

[Tutoriales de consultas de Predication](predication-queries.md)
</dt> </dl>

 

 




