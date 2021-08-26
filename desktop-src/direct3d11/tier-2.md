---
title: Nivel 2
description: En esta sección se describe la compatibilidad con el nivel 2.
ms.assetid: 4A4AEF13-2F0F-482E-9262-256C257ED85A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f5a5b018e5e48e6b2a1b86771b925cb88cf070ecd2b1303d359640eac565bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027795"
---
# <a name="tier-2"></a>Nivel 2

En esta sección se describe la compatibilidad con el nivel 2.

-   Hardware en el nivel de característica 11.1 como mínimo.
-   Todas las características del nivel anterior (sin limitaciones específicas de nivel [1)](tier-1.md) más las adiciones en estos elementos siguientes:
-   Hay disponibles instrucciones de sombreador para fijar el LOD y los comentarios de estado asignados. Para más información, consulte [Exposición de recursos en mosaico HLSL.](hlsl-tiled-resources-exposure.md)
-   Las lecturas de iconos no asignados devuelven 0 en todos los componentes que no faltan del formato y el valor predeterminado para los componentes que faltan.
-   Las escrituras en iconos no asignados se detienen para ir a la memoria, pero pueden acabar en cachés que las lecturas posteriores en la misma dirección podrían o no recoger.
-   El filtrado de textura con una superficie que se encuentra entre los iconos **NULL** y los que no son NULL contribuye a 0 (con los valores predeterminados para los componentes de formato que faltan) para los elementos de textura de los iconos **NULL** en la operación de filtro general. Algunos hardware tempranos no cumplen este requisito y devuelve 0 (con los valores predeterminados para los componentes de formato que faltan) para el resultado del filtro completo si algún elemento de textura (con un peso distinto de cero) se encuentra en un icono **NULL.** No se permitirá que ningún otro hardware pierda el requisito de incluir todos los elementos de textura (ponderados distintos de cero) en la operación de filtro.
-   **Los** accesos de textura NULL hacen que la [**operación CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) en los comentarios de estado de una lectura de textura devuelva false. Esto es independientemente de cómo se pueda enmascarar la escritura del resultado de acceso de textura en el sombreador y cuántos componentes están en el formato de textura (la combinación de los cuales podría hacer que parezca que no es necesario tener acceso a la textura).
-   Restricciones de alineación para las formas de mosaico estándar: se garantiza que los mapas Mipmap que rellenan al menos un icono estándar en todas las dimensiones usen el mosaico estándar, y el resto se considera empaquetado como una unidad en N iconos (N **notificados** a la aplicación). La aplicación puede asignar los N iconos a ubicaciones arbitrariamente no unidas en un grupo de mosaicos, pero debe asignar todos o ninguno de los iconos empaquetados. El empaquetado de mip es un conjunto único de iconos empaquetados por segmento de matriz.
-   Se admite el filtrado de reducción mínimo/máximo. Para obtener información sobre el filtrado de reducción mínima/máxima, consulte Características de muestreo de [textura de recursos en mosaico.](tiled-resources-texture-sampling-features.md)
-   Los recursos en mosaico con mapas MIP menores que el tamaño de mosaico estándar en cualquier dimensión no pueden tener un tamaño de matriz mayor que 1.
-   Las limitaciones sobre cómo se puede acceder a los iconos cuando hay asignaciones duplicadas, descritas en Limitaciones de acceso a iconos con asignaciones [duplicadas,](tile-access-limitations-with-duplicate-mappings-.md)se siguen aplicando.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Niveles de características de recursos en mosaico](tiled-resources-features-tiers.md)
</dt> </dl>

 

 