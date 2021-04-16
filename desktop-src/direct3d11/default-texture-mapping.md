---
title: Asignación de textura predeterminada
description: El uso de la asignación de texturas predeterminada reduce la copia y el uso de memoria mientras se comparten datos de imagen entre la GPU y la CPU.
ms.assetid: 77AF4BFA-09B5-4181-9408-002764F2A923
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f203c7590c3673d30315250b2b4ce2663e48c9c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418710"
---
# <a name="default-texture-mapping"></a>Asignación de textura predeterminada

El uso de la asignación de texturas predeterminada reduce la copia y el uso de memoria mientras se comparten datos de imagen entre la GPU y la CPU. Sin embargo, solo se debe usar en situaciones específicas. El diseño de swizzle estándar evita copiar o permutación datos en varios diseños.

-   [Información general](#overview)
-   [API D3D 11.3](#d3d113-apis)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

La asignación de texturas predeterminadas no debe ser la primera opción para los desarrolladores. Los desarrolladores deben codificar en primer lugar con la GPU discreta (es decir, no tienen acceso a la CPU para la mayoría de las texturas y se cargan con [**CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)). Sin embargo, en ciertos casos, la CPU y la GPU pueden interactuar con tanta frecuencia en los mismos datos, que la asignación de texturas predeterminadas resulta útil para ahorrar energía o para acelerar un diseño determinado en arquitecturas o adaptadores concretos. Las aplicaciones deben detectar estos casos y optimizar las copias innecesarias.

En D3D 11.3, las texturas creadas con \_ el diseño de textura D3D11 \_ \_ sin definir (un miembro de la enumeración de [**\_ \_ diseño de textura D3D11**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) ) y ningún acceso de CPU son las más eficaces para la representación y el muestreo de GPU frecuentes. Cuando se realiza una prueba de rendimiento, esas texturas se deben comparar con el \_ diseño de textura D3D11 sin \_ \_ definir con el acceso a la CPU y con el D3D11 \_ \_ \_ de distribución de textura de 64 k \_ \_ SWIZZLE estándar con acceso de CPU y la \_ \_ \_ fila de diseño de textura D3D11 \_ principal para la compatibilidad entre adaptadores.

El uso de D3D11 \_ Texture \_ layout \_ undefined with CPU Access habilita los métodos [**WriteToSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource), Map (lo que impide el acceso a [](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)la aplicación al puntero) y se anula la [**asignación**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) , pero puede sacrificar la eficacia del acceso a la GPU. El uso \_ de D3D11 Texture \_ layout \_ 64k \_ estándar \_ SWIZZLE con acceso de CPU habilita **WriteToSubresource**, **ReadFromSubresource**, **map** (que devuelve un puntero válido a la aplicación) y se puede desasignar. También puede sacrificar la eficacia del acceso a GPU más que el diseño de textura de D3D11 \_ \_ \_ sin definir con el acceso a la CPU.

En general, las aplicaciones deben crear la mayoría de las texturas como accesible solo para GPU y con el \_ diseño de textura D3D11 sin \_ \_ definir.

Antes de la característica de asignación de texturas predeterminadas, solo había un diseño normalizado para los datos multidimensionales: "lineal", también conocido como "principal de filas". Las aplicaciones deben evitar las \_ texturas dinámicas de uso y almacenamiento provisional \_ cuando está disponible la opción asignar valores predeterminados. Las \_ texturas dinámicas de uso y almacenamiento provisional \_ usan el diseño lineal.

D3D 11.3 (y D3D12) introduce un diseño estándar de datos multidimensionales. Esto se hace para permitir que varias unidades de procesamiento operen en los mismos datos sin copiar los datos ni permutación los datos entre varios diseños. Un diseño normalizado permite mejorar la eficacia a través de los efectos de la red y permite que los algoritmos realicen cortes cortos suponiendo un patrón determinado.

No obstante, tenga en cuenta que esta swizzle estándar es una característica de hardware y puede que no sea compatible con todas las GPU.

## <a name="d3d113-apis"></a>API D3D 11.3

A diferencia de D3D12, D3D 11.3 no admite la asignación de texturas de forma predeterminada, por lo que debe consultar los datos de la [**\_ característica D3D11 \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2). También será necesario consultar los swizzle estándar con una llamada a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) y comprobando el `StandardSwizzle64KBSupported` campo de **D3D11 de \_ datos de características \_ \_ D3D11 \_ OPTIONS2**.

Las siguientes API hacen referencia a la asignación de textura:

Enumeraciones

-   [**D3D11 \_ \_Diseño de textura**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) : controla el patrón swizzle de las texturas predeterminadas y habilita la compatibilidad con asignaciones en las texturas predeterminadas.
-   [**D3D11 \_ CARACTERÍSTICA**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) : hace referencia a [**D3D11 \_ \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2).
-   [**D3D11 \_ \_ \_ Marca de copia de mosaicos**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : contiene marcas para copiar los recursos en mosaico de swizzled en los búferes lineales y desde ellos.

Estructuras

-   [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1) : describe una textura 2D. Tenga en cuenta la estructura de la \_ \_ aplicación auxiliar CD3D11 TEXTURE2D DESC1.
-   [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1) : describe una textura 3D. Tenga en cuenta la estructura de la \_ \_ aplicación auxiliar CD3D11 TEXTURE3D DESC1.

Métodos

-   [**ID3D11Device3:: CreateTexture2D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture2d1) : crea una matriz de texturas 2D.
-   [**ID3D11Device3:: CreateTexture3D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture3d1) : crea una sola textura 3D.
-   [**ID3D11Device3:: WriteToSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource) : copia datos en una \_ textura predeterminada de uso de D3D11 \_ que se asignó mediante [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
-   [**ID3D11Device3:: ReadFromSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource) : copia datos de una \_ textura predeterminada del uso de D3D11 \_ que se asignó mediante [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
-   [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) : obtiene un puntero a los datos contenidos en un subrecurso y deniega el acceso de la GPU a ese subrecurso.
-   [**ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) desasignar: invalida el puntero a un recurso y vuelve a habilitar el acceso de la GPU a ese recurso.
-   [**ID3D11Texture2D1:: GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture2d1-getdesc1) : obtiene las propiedades de un recurso de textura 2D.
-   [**ID3D11Texture3D1:: GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture3d1-getdesc1) : obtiene las propiedades de un recurso de textura 3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 




