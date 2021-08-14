---
title: Asignación de textura predeterminada
description: El uso de la asignación de texturas predeterminada reduce el uso de la copia y la memoria al compartir datos de imagen entre la GPU y la CPU.
ms.assetid: 77AF4BFA-09B5-4181-9408-002764F2A923
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edc81fc1bf59a974f9bd901fc96d43afc16019edce68fbaabfbf3259c0d4a3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752295"
---
# <a name="default-texture-mapping"></a>Asignación de textura predeterminada

El uso de la asignación de texturas predeterminada reduce el uso de la copia y la memoria al compartir datos de imagen entre la GPU y la CPU. Sin embargo, solo se debe usar en situaciones específicas. El diseño swzzle estándar evita copiar o deslizar datos en varios diseños.

-   [Información general](#overview)
-   [API D3D11.3](#d3d113-apis)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

La asignación de texturas predeterminadas no debe ser la primera opción para los desarrolladores. Los desarrolladores deben codificar primero de forma discreta y fácil de usar con GPU (es decir, no tener acceso a la CPU para la mayoría de las texturas y cargar con [**CopySubresourceRegion1).**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) Pero, en determinados casos, la CPU y la GPU pueden interactuar con tanta frecuencia en los mismos datos, que la asignación de texturas predeterminadas resulta útil para ahorrar energía o para acelerar un diseño determinado en determinados adaptadores o arquitecturas. Las aplicaciones deben detectar estos casos y optimizar las copias innecesarias.

En D3D11.3, las texturas creadas con D3D11 TEXTURE LAYOUT UNDEFINED (un miembro de la \_ \_ \_ [**enumeración \_ TEXTURE LAYOUT \_ de D3D11)**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) y ningún acceso de CPU son las más eficaces para la representación y el muestreo frecuentes de GPU. Al realizar pruebas de rendimiento, esas texturas deben compararse con D3D11 TEXTURE LAYOUT UNDEFINED con acceso \_ \_ a \_ CPU, D3D11 TEXTURE LAYOUT 64K STANDARD SW ROWLE con acceso a CPU y \_ \_ \_ \_ \_ D3D11 \_ TEXTURE LAYOUT ROW MAJOR \_ \_ \_ para compatibilidad entre adaptadores.

El uso de D3D11 TEXTURE LAYOUT UNDEFINED con acceso de CPU habilita los métodos \_ \_ \_ [**WriteToSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource), [**ReadFromSubresource,**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource) [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) (que excluye el acceso de la aplicación al puntero) y [**Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); pero puede sacrificar la eficacia del acceso a GPU. El uso de D3D11 \_ TEXTURE \_ LAYOUT 64K STANDARD SWZZLE con acceso de CPU habilita \_ \_ \_ **WriteToSubresource,** **ReadFromSubresource,** **Map** (que devuelve un puntero válido a la aplicación) y Unmap . También puede sacrificar la eficacia del acceso de GPU a más de D3D11 \_ TEXTURE \_ LAYOUT \_ UNDEFINED con acceso de CPU.

En general, las aplicaciones deben crear la mayoría de las texturas como accesibles solo para GPU y con DISEÑO DE TEXTURA D3D11 \_ \_ SIN \_ DEFINIR.

Antes de la característica de texturas predeterminadas de asignación, solo había un diseño estandarizado para datos multidimensionales: "lineal", también conocido como "fila principal". Las aplicaciones deben evitar las \_ texturas USAGE STAGING y USAGE \_ DYNAMIC cuando el valor predeterminado del mapa está disponible. Las \_ texturas USAGE STAGING y USAGE \_ DYNAMIC usan el diseño lineal.

D3D11.3 (y D3D12) presentan un diseño de datos multidimensional estándar. Esto se hace para permitir que varias unidades de procesamiento funcionen en los mismos datos sin copiar los datos ni deslizar los datos entre varios diseños. Un diseño estandarizado permite aumentar la eficacia a través de los efectos de red y permite que los algoritmos realicen cortas reducciones suponiendo un patrón determinado.

Tenga en cuenta que este swzzle estándar es una característica de hardware y es posible que no sea compatible con todas las GPU.

## <a name="d3d113-apis"></a>API D3D11.3

A diferencia de D3D12, D3D11.3 no admite la asignación de texturas de forma predeterminada, por lo que debe consultar [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2). También será necesario consultar swzzle estándar con una llamada a [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) y comprobar el campo de `StandardSwizzle64KBSupported` **D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**.

Las siguientes API hacen referencia a la asignación de texturas:

Enumeraciones

-   [**D3D11 \_ TEXTURE \_ LAYOUT**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) : controla el patrón swzzle de las texturas predeterminadas y habilita la compatibilidad con mapas en texturas predeterminadas.
-   [**D3D11 \_ FEATURE:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) hace [**referencia a D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2).
-   [**D3D11 \_ TILE \_ COPY \_ FLAG:**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) contiene marcas para copiar recursos en mosaico desdobados hacia y desde búferes lineales.

Estructuras

-   [**D3D11 \_ TEXTURE2D \_ DESC1:**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1) describe una textura 2D. Observe la estructura auxiliar CD3D11 \_ TEXTURE2D \_ DESC1.
-   [**D3D11 \_ TEXTURE3D \_ DESC1:**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1) describe una textura 3D. Observe la estructura auxiliar CD3D11 \_ TEXTURE3D \_ DESC1.

Métodos

-   [**ID3D11Device3::CreateTexture2D1:**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture2d1) crea una matriz de texturas 2D.
-   [**ID3D11Device3::CreateTexture3D1:**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture3d1) crea una sola textura 3D.
-   [**ID3D11Device3::WriteToSubresource:**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource) copia los datos en una textura USAGE DEFAULT de D3D11 que se \_ \_ asignó mediante [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
-   [**ID3D11Device3::ReadFromSubresource:**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource) copia datos de una textura USAGE DEFAULT de D3D11 que se \_ \_ asignó mediante [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
-   [**ID3D11DeviceContext::Map:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) obtiene un puntero a los datos contenidos en un subrecurso y deniega el acceso de GPU a ese subrecurso.
-   [**ID3D11DeviceContext::Unmap:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) invalida el puntero a un recurso y vuelve a inicializar el acceso de la GPU a ese recurso.
-   [**ID3D11Texture2D1::GetDesc1:**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture2d1-getdesc1) obtiene las propiedades de un recurso de textura 2D.
-   [**ID3D11Texture3D1::GetDesc1:**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture3d1-getdesc1) obtiene las propiedades de un recurso de textura 3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de Direct3D 11.3](direct3d-11-3-features.md)
</dt> </dl>

 

 




