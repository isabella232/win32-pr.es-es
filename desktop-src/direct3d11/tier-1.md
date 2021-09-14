---
title: Nivel 1
description: En esta sección se describe la compatibilidad con el nivel 1.
ms.assetid: 8E2907D2-EFCB-4F97-9B40-6835A65D3DE5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4111fa48dafa7f38a26d5ca09f95898eacef6f55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966899"
---
# <a name="tier-1"></a>Nivel 1

En esta sección se describe la compatibilidad con el nivel 1.

-   Hardware en el nivel de característica 11.0 como mínimo.
-   No hay compatibilidad con la resalte.
-   No se admite Texture1D ni Texture3D.
-   No se admite el suavizado de contorno múltiple (MSAA) de ejemplo 2, 8 o 16. Solo se requieren 4 veces, excepto los formatos 128 bpp.
-   No hay ningún patrón swzzle estándar (el diseño en mosaicos de 64 KB y el empaquetado de mip de cola es del proveedor de hardware).
-   Limitaciones de cómo se puede acceder a los iconos cuando hay asignaciones duplicadas, descritas en Limitaciones de acceso a [iconos con asignaciones duplicadas.](tile-access-limitations-with-duplicate-mappings-.md)

### <a name="limitations-affecting-tier-1-only"></a>Limitaciones que solo afectan al nivel 1

-   Los recursos en mosaico pueden **tener asignaciones NULL,** pero leerlos o escribirlos en ellos genera resultados indefinidos, incluido el dispositivo quitado. Las aplicaciones pueden evitarlo asignando una sola página ficticia a todas las áreas vacías. Tenga cuidado si escribe y representa en una página que está asignada a varias ubicaciones de destino de representación porque el orden de escrituras será indefinido.
-   Las instrucciones del sombreador para fijar el LOD y los comentarios de estado asignados no están disponibles. Para más información, consulte [Exposición de recursos en mosaico HLSL.](hlsl-tiled-resources-exposure.md)
-   Restricciones de alineación para las formas de mosaico estándar: solo se garantiza que las mips (a partir de la más fina) cuyas dimensiones sean múltiplo del tamaño de mosaico estándar admitan las formas de mosaico estándar y puedan tener mosaicos individuales asignados o no asignados arbitrariamente. El primer mapa mipmap de un recurso en mosaico que tenga cualquier dimensión que no sea un múltiplo de tamaño de mosaico estándar, junto con todos los mapas mip más general, puede tener una forma de mosaico no estándar, que se adapta a los mosaicos de N de 64 KB para este conjunto de mips a la vez (N notificados a la aplicación). Estos N iconos se consideran empaquetados como una unidad, que la aplicación debe asignar completamente o no asignar completamente en un momento dado, aunque las asignaciones de cada uno de los N iconos pueden estar en ubicaciones arbitrariamente no unidas en un grupo de mosaicos.
-   Los recursos en mosaico con cualquier asignación mipmap que no sea un múltiplo de tamaño de mosaico estándar en todas las dimensiones no pueden tener un tamaño de matriz mayor que 1.
-   Para cambiar entre hacer referencia [a](overviews-direct3d-11-resources-buffers.md) iconos de un grupo de mosaicos a través de un recurso de búfer [a](overviews-direct3d-11-resources-textures.md) hacer referencia a los mismos iconos a través de un recurso de textura, o viceversa, la llamada más reciente a [**UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) o [**CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) que define las asignaciones a esos iconos del grupo de mosaicos debe ser para la misma dimensión de recursos (búfer frente a textura) que la dimensión de recurso que se usará para acceder a los \* iconos. De lo contrario, el comportamiento no está definido, incluida la posibilidad de que se restablezca el dispositivo. Por ejemplo, llamar a **UpdateTileMappings** para definir asignaciones de mosaicos para un búfer y, a continuación, **ActualizarTileMappings** a los mismos iconos del grupo de mosaicos a través de un recurso [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y, a continuación, el acceso a los iconos a través del búfer no es válido. Las operaciones alternativas son volver a definir las asignaciones de mosaicos de un recurso al cambiar entre los iconos de búfer y textura (o viceversa) o simplemente no compartir nunca iconos en un grupo de mosaicos entre los recursos de búfer y los recursos de textura.
-   No se admite el filtrado de reducción mínimo/máximo. Para obtener información sobre el filtrado de reducción mínima/máxima, consulte Características de muestreo de [textura de recursos en mosaico.](tiled-resources-texture-sampling-features.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Niveles de características de recursos en mosaico](tiled-resources-features-tiers.md)
</dt> </dl>

 

 