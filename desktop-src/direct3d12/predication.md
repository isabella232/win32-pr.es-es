---
title: Predicación
description: Predicación es una característica que permite a la GPU en lugar de a la CPU determinar que no dibuje, copie ni envíe un objeto.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422d0f2fc5f69ca0e633be4e93af4448a02efc42fbc89592125c45909710c462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118806685"
---
# <a name="predication"></a>Predicación

Predicación es una característica que permite a la GPU en lugar de a la CPU determinar que no dibuje, copie ni envíe un objeto.

-   [Información general](#overview)
-   [SetPredication](#setpredication)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

El uso típico de predicado es con oclusión; si se dibuja un cuadro de límite y se oculta, obviamente no hay ningún punto en dibujar el propio objeto. En esta situación, el dibujo del objeto se puede "predicar", lo que permite su eliminación de la representación real por la GPU.

Al principio, esto podría parecer redudant sobre y por encima de la prueba de profundidad estándar más un paso de profundidad temprana. Pero el predicado puede quitar la sobrecarga del propio estado del comando draw, además de la rasterización. Aunque un paso de profundidad temprano quita píxeles innecesarios, todavía puede ejecutar sombreadores de vértice, casco, dominio y geometría, e invocar el ensamblador de entrada de función fija, el teator y el rasterizador. Al dibujar un cuadro de límite simple o un volumen de límite similar, que es más fácil de procesar y rasterizar que el modelo real, se evita la rasterización y el procesamiento &mdash; &mdash; innecesarios.

A diferencia de Direct3D 11, la predicado se desacopla de las consultas y se expande en Direct3D 12 para permitir que una aplicación predica objetos en función de cualquier razonamiento que el desarrollador de la aplicación pueda decidir (no solo la oclusión).

## <a name="setpredication"></a>SetPredication

La predicado se puede establecer en función del valor de 64 bits dentro de un búfer (consulte [**D3D12 \_ PREDICATION \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).

Cuando la GPU ejecuta un [**comando SetPredication,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) ajusta el valor en el búfer. Los cambios futuros en los datos del búfer no afectan de forma retroactiva al estado de predicado.

Si el parámetro de entrada Buffer es NULL, el predicado se deshabilita.

Las sugerencias de predicado no están presentes en la API de Direct3D 12; y se permite la predicación en listas de comandos directas, de proceso y de copia. El búfer de origen puede estar en cualquier tipo de montón (predeterminado, carga, reversión, personalizado).

El entorno de ejecución principal validará lo siguiente:

-   *AlignedBufferOffset* es un múltiplo de 8 bytes
-   El recurso es un búfer
-   La operación es un miembro válido de la enumeración
-   [**No se puede llamar a SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) desde una agrupación
-   El tipo de lista de comandos admite predicados
-   El desplazamiento no supera el tamaño del búfer.

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

 

 




