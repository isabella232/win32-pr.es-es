---
title: Predicación
description: Predication es una característica que permite que la GPU en lugar de la CPU determine que no se debe dibujar, copiar ni enviar un objeto.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072926"
---
# <a name="predication"></a>Predicación

Predication es una característica que permite que la GPU en lugar de la CPU determine que no dibujar, copiar ni enviar un objeto.

-   [Información general](#overview)
-   [SetPredication](#setpredication)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

El uso típico de la predicado es con oclusión; Si se dibuja un cuadro de límite y se oculta, obviamente no hay ningún punto en dibujar el propio objeto. En esta situación, el dibujo del objeto se puede "predicar", lo que permite su eliminación de la representación real por parte de la GPU.

Al principio, esto podría parecer redudant más allá de la prueba de profundidad estándar más un paso de profundidad temprana. Sin embargo, el predicado puede quitar la sobrecarga del propio estado del comando draw, además de la rasterización. Aunque un paso de profundidad temprano quita píxeles innecesarios, todavía puede ejecutar sombreadores de vértice, casco, dominio y geometría, e invocar el ensamblador de entrada de función fija, el tesselador y el rasterizador. Al dibujar un cuadro de límite simple o un volumen de límite similar, que es más fácil de procesar y rasterizar que el modelo real, se evita la rasterización y &mdash; &mdash; el procesamiento innecesarios.

A diferencia de Direct3D 11, la predicado se desacopla de las consultas y se expande en Direct3D 12 para permitir que una aplicación predica objetos en función de cualquier razonamiento que el desarrollador de la aplicación pueda decidir (no solo la oclusión).

## <a name="setpredication"></a>SetPredication

La predicado se puede establecer en función del valor de 64 bits dentro de un búfer (consulte [**D3D12 \_ PREDICATION \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).

Cuando la GPU ejecuta un [**comando SetPredication,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) ajusta el valor en el búfer. Los cambios futuros en los datos del búfer no afectan retroactivamente al estado de predicado.

Si el parámetro de entrada Buffer es NULL, el predicado se deshabilita.

Las sugerencias de predicado no están presentes en la API de Direct3D 12; y se permite la predicación en listas de comandos directas, de proceso y de copia. El búfer de origen puede estar en cualquier tipo de montón (predeterminado, carga, readback, personalizado).

El entorno de ejecución principal validará lo siguiente:

-   *AlignedBufferOffset* es un múltiplo de 8 bytes
-   El recurso es un búfer
-   La operación es un miembro válido de la enumeración
-   [**No se puede llamar a SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) desde una agrupación
-   El tipo de lista de comandos admite predicado
-   El desplazamiento no supera el tamaño del búfer

La capa de depuración emitirá un error si el búfer de origen no está en el D3D12_RESOURCE_STATE_PREDICATION [**(que**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) es el mismo que [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)y simplemente un alias).

El conjunto de operaciones que se pueden predicar son:

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

[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) no se predica a sí mismo. En su lugar, se predican las operaciones individuales de la lista anterior que se encuentran en el lado de la agrupación.

Los métodos ID3D12GraphicsCommandList [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) y [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) no se predican.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contadores y consultas](counters-and-queries.md)
</dt> <dt>

[Medición del rendimiento](performance-measurement.md)
</dt> <dt>

[Paso a paso de consultas de predicado](predication-queries.md)
</dt> </dl>

 

 




