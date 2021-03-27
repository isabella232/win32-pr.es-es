---
title: Nivel 1
description: En esta sección se describe la compatibilidad de nivel 1.
ms.assetid: 8E2907D2-EFCB-4F97-9B40-6835A65D3DE5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4111fa48dafa7f38a26d5ca09f95898eacef6f55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793611"
---
# <a name="tier-1"></a>Nivel 1

En esta sección se describe la compatibilidad de nivel 1.

-   Hardware en el nivel de características 11,0 mínimo.
-   No se admiten tejidos.
-   No se admite Texture1D ni Texture3D.
-   No compatible con el suavizado de contorno de muestreo Multimuestra (MSAA) de 2, 8 o 16. Solo se requiere 4x, excepto los formatos 128 BPP.
-   Ningún patrón swizzle estándar (el diseño dentro de los mosaicos de 64 KB y el empaquetado de MIP de cola es el proveedor de hardware).
-   Limitaciones en el modo en que se puede obtener acceso a los mosaicos cuando hay asignaciones duplicadas, descritas en el [icono limitaciones de acceso con asignaciones duplicadas](tile-access-limitations-with-duplicate-mappings-.md).

### <a name="limitations-affecting-tier-1-only"></a>Limitaciones que solo afectan al nivel 1

-   Los recursos en mosaico pueden tener asignaciones **null** , pero leerlos o escribir en ellos produce resultados indefinidos, incluido el dispositivo quitado. Las aplicaciones pueden evitar esto asignando una sola página ficticia a todas las áreas vacías. Tenga cuidado si escribe y representa en una página que está asignada a varias ubicaciones de destino de representación porque el orden de las escrituras será undefined.
-   Las instrucciones del sombreador para la compresión de LOD y los comentarios de estado asignados no están disponibles. Para obtener más información, consulte la [exposición de los recursos en mosaico de HLSL](hlsl-tiled-resources-exposure.md).
-   Restricciones de alineación para las formas de mosaico estándar: solo se garantiza que MIPS (a partir del más fino) cuyas dimensiones son todas múltiplos del tamaño de mosaico estándar y que pueden tener mosaicos individuales asignados o desasignados arbitrariamente. El primer mipmap de un recurso en mosaico que tiene cualquier dimensión no es un múltiplo del tamaño de mosaico estándar, junto con todos los mapas de bits más generales, puede tener una forma de mosaico no estándar, ajustarse a los mosaicos de N KB para este conjunto de MIPS a la vez (N se ha comunicado a la aplicación). Estos N mosaicos se consideran empaquetados como una unidad, que debe ser totalmente asignada o totalmente Desasignada por la aplicación en un momento dado, aunque las asignaciones de cada uno de los iconos N pueden estar en ubicaciones geojuntas arbitrariamente en un grupo de mosaicos.
-   Los recursos en mosaico con cualquier mipmaps que no sea un múltiplo del tamaño de mosaico estándar en todas las dimensiones no pueden tener un tamaño de matriz mayor que 1.
-   Para cambiar entre los mosaicos de referencia de un grupo de mosaicos a través de un recurso de [búfer](overviews-direct3d-11-resources-buffers.md) para hacer referencia a los mismos mosaicos a través de un recurso de [textura](overviews-direct3d-11-resources-textures.md) , o viceversa, la llamada más reciente a [**UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) o [**CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) que define las asignaciones a esos mosaicos del grupo de mosaicos debe ser para la misma dimensión de recursos (búfer frente a textura \* ) que la dimensión de recursos que se utilizará De lo contrario, el comportamiento es indefinido, lo que incluye la posibilidad de restablecer el dispositivo. Por lo tanto, por ejemplo, al llamar a **UpdateTileMappings** para definir asignaciones de iconos para un búfer y, después, **UpdateTileMappings** a los mismos mosaicos en el grupo de mosaicos a través de un recurso de [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) , el acceso a los mosaicos a través del búfer no es válido. Las operaciones de solución alternativa consisten en volver a definir asignaciones de mosaicos para un recurso al cambiar entre el búfer y la textura (o viceversa) para compartir iconos o simplemente no compartir iconos en un grupo de mosaicos entre recursos de búfer y recursos de textura.
-   No se admite el filtrado de reducción mín./máx. Para obtener información sobre el filtrado de reducción mínima/máxima, consulte [características de muestreo de textura de recursos en mosaico](tiled-resources-texture-sampling-features.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Niveles de características de recursos en mosaico](tiled-resources-features-tiers.md)
</dt> </dl>

 

 