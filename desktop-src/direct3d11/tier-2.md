---
title: Nivel 2
description: En esta sección se describe la compatibilidad de nivel 2.
ms.assetid: 4A4AEF13-2F0F-482E-9262-256C257ED85A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fa6e8ff3dba5780e3507bb2da5273e327a30e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904705"
---
# <a name="tier-2"></a>Nivel 2

En esta sección se describe la compatibilidad de nivel 2.

-   Hardware en el nivel de características 11,1 mínimo.
-   Todas las características del nivel anterior (sin limitaciones específicas de [nivel 1](tier-1.md) ) además de las adiciones en los siguientes elementos:
-   Hay disponibles instrucciones del sombreador para la compresión de LOD y comentarios de estado asignados. Para obtener más información, consulte la [exposición de los recursos en mosaico de HLSL](hlsl-tiled-resources-exposure.md).
-   Las lecturas de mosaicos no asignados devuelven 0 en todos los componentes que no faltan del formato y el valor predeterminado para los componentes que faltan.
-   Las escrituras en mosaicos no asignados se detienen de ir a la memoria, pero pueden acabar en las memorias caché que las lecturas posteriores de la misma dirección podrían o no retomarse.
-   El filtrado de texturas con una superficie que abarca los mosaicos **nulos** y los que no son **null** aporta 0 (con valores predeterminados para los componentes de formato que faltan) para textura en los mosaicos **nulos** en la operación de filtro global. Algunos equipos de hardware temprano no cumplen este requisito y devuelven 0 (con valores predeterminados para los componentes de formato que faltan) para el resultado del filtro completo si cualquier textura (con un peso distinto de cero) se encuentra en un icono **nulo** . No se permitirá que ningún otro hardware pierda el requisito de incluir todos los textura (distinto de cero ponderados) en la operación de filtro.
-   Los accesos de textura **nulos** provocan que la operación [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) en la información de estado de una textura leída devuelva false. Esto se debe a la manera en que el resultado de acceso de la textura podría aparecer enmascarado en el sombreador y el número de componentes que se encuentran en el formato de textura (la combinación de puede hacer que parezca que no es necesario tener acceso a la textura).
-   Restricciones de alineación para las formas de mosaico estándar: los mapas MIP que rellenan al menos un icono estándar en todas las dimensiones tienen la garantía de que usan el mosaico estándar, donde el resto se considera empaquetado como una **unidad** en N mosaicos (n se ha comunicado a la aplicación). La aplicación puede asignar los iconos N en ubicaciones contiguas de forma arbitraria en un grupo de mosaicos, pero debe asignar todos los iconos empaquetados o ninguno de ellos. El empaquetado de MIP es un conjunto único de mosaicos empaquetados por segmento de matriz.
-   Se admite el filtrado de reducción mínima/máxima. Para obtener información sobre el filtrado de reducción mínima/máxima, consulte [características de muestreo de textura de recursos en mosaico](tiled-resources-texture-sampling-features.md).
-   Los recursos en mosaico con cualquier mipmaps menor que el tamaño de mosaico estándar en cualquier dimensión no pueden tener un tamaño de matriz mayor que 1.
-   Se aplican limitaciones sobre cómo se puede tener acceso a los mosaicos cuando hay asignaciones duplicadas, que se describen en el [icono limitaciones de acceso con asignaciones duplicadas](tile-access-limitations-with-duplicate-mappings-.md), y continúan aplicándose.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Niveles de características de recursos en mosaico](tiled-resources-features-tiers.md)
</dt> </dl>

 

 