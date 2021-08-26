---
title: Compresión de bloques de textura en Direct3D 11
description: La compatibilidad con la compresión de bloques (BC) para texturas se ha ampliado en Direct3D 11 para incluir los algoritmos BC6H y BC7.
ms.assetid: E0735D4E-9C0F-45DC-854A-C27EB8367D86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52c2c764c0f9dca4021dcb14187db67e697cd7155701294a9c6214b4543d00b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027805"
---
# <a name="texture-block-compression-in-direct3d-11"></a>Compresión de bloques de textura en Direct3D 11

La compatibilidad con la compresión de bloques (BC) para texturas se ha ampliado en Direct3D 11 para incluir los algoritmos BC6H y BC7. BC6H admite datos de origen de color de rango altamente dinámicos y BC7 proporciona una compresión de calidad superior a la media con menos artefactos para los datos de origen RGB estándar.

Para obtener información más específica sobre la compatibilidad con algoritmos de compresión de bloques antes de Direct3D 11, incluida la compatibilidad con los formatos BC1 a BC5, vea Compresión de [bloques (Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)

**Nota sobre los formatos de archivo:** Los formatos de compresión de textura BC6H y BC7 usan el formato de archivo DDS para almacenar los datos de textura comprimidos. Para obtener más información, consulte la [Guía de programación para DDS](/windows/desktop/direct3ddds/dx-graphics-dds-pguide) para obtener más información.

## <a name="block-compression-formats-supported-in-direct3d-11"></a>Formatos de compresión de bloques admitidos en Direct3D 11



| Datos de origen                                  | Resolución mínima de compresión de datos necesaria                              | Formato recomendado | Nivel mínimo de características admitidas |
|----------------------------------------------|---------------------------------------------------------------------------|--------------------|---------------------------------|
| Color de tres canales con canal alfa       | Tres canales de color (5 bits:6 bits:5 bits), con 0 o 1 bit de alfa  | BC1                | Direct3D 9.1                    |
| Color de tres canales con canal alfa       | Tres canales de color (5 bits:6 bits:5 bits), con 4 bits de alfa         | BC2                | Direct3D 9.1                    |
| Color de tres canales con canal alfa       | Tres canales de color (5 bits:6 bits:5 bits) con 8 bits de alfa          | BC3                | Direct3D 9.1                    |
| Color de un canal                            | Un canal de color (8 bits)                                                | BC4                | Direct3D 10                     |
| Color de dos canales                            | Dos canales de color (8 bits:8 bits)                                        | BC5                | Direct3D 10                     |
| Color de rango dinámico alto (HDR) de tres canales | Tres canales de color (16 bits:16 bits:16 bits) en punto flotante "medio"\* | BC6H               | Direct3D 11                     |
| Color de tres canales, canal alfa opcional  | Tres canales de color (de 4 a 7 bits por canal) con de 0 a 8 bits de alfa  | BC7                | Direct3D 11                     |



 

\*El punto flotante "Half" es un valor de 16 bits que consta de un bit de signo opcional, un exponente sesgado de 5 bits y una mantisa de 10 o 11 bits.

## <a name="bc1-bc2-and-b3-formats"></a>Formatos BC1, BC2 y B3

Los formatos BC1, BC2 y BC3 son equivalentes a los formatos de compresión de textura DXTn de Direct3D 9 y son los mismos que los formatos correspondientes de Direct3D 10 BC1, BC2 y BC3. Todos los niveles de características requieren compatibilidad con estos tres formatos (D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1, D3D \_ FEATURE LEVEL \_ \_ 9 \_ 2, \_ D3D FEATURE LEVEL \_ \_ 9 \_ 3, D3D \_ FEATURE LEVEL \_ \_ 10 \_ 0, D3D \_ FEATURE LEVEL \_ \_ 10 1 y \_ D3D \_ FEATURE LEVEL \_ \_ 11 \_ 0).



| Formato de compresión de bloques | Formato DXGI                                                                           | Formato equivalente de Direct3D 9                               | Bytes por bloque de 4 x 4 píxeles |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------|---------------------------|
| BC1                      | DXGI \_ FORMAT \_ BC1 \_ UNORM, DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB, DXGI \_ FORMAT \_ BC1 \_ TYPELESS | D3DFMT \_ DXT1, FourCC="DXT1"                                | 8                         |
| BC2                      | DXGI \_ FORMAT \_ BC2 \_ UNORM, DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB, DXGI \_ FORMAT \_ BC2 \_ TYPELESS | D3DFMT \_ DXT2 \* , FourCC="DXT2", D3DFMT \_ DXT3, FourCC="DXT3" | 16                        |
| BC3                      | DXGI \_ FORMAT \_ BC3 \_ UNORM, DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB, DXGI \_ FORMAT \_ BC3 \_ TYPELESS | D3DFMT \_ DXT4 \* , FourCC="DXT4", D3DFMT \_ DXT5, FourCC="DXT5" | 16                        |



 

\*Estos esquemas de compresión (DXT2 y DXT4) no distinguen entre los formatos alfa multiplicados previamente de Direct3D 9 y los formatos alfa estándar. Los sombreadores programables deben controlar esta distinción en el momento de la representación.

## <a name="bc4-and-bc5-formats"></a>Formatos BC4 y BC5



| Formato de compresión de bloques | Formato DXGI                                                                     | Formato equivalente de Direct3D 9 | Bytes por bloque de 4 x 4 píxeles |
|--------------------------|---------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC4                      | DXGI \_ FORMAT \_ BC4 \_ UNORM, DXGI \_ FORMAT \_ BC4 \_ SNORM, DXGI \_ FORMAT \_ BC4 \_ TYPELESS | FourCC="ATI1"                | 8                         |
| BC5                      | DXGI \_ FORMAT \_ BC5 \_ UNORM, DXGI \_ FORMAT \_ BC5 \_ SNORM, DXGI \_ FORMAT \_ BC5 \_ TYPELESS | FourCC="ATI2"                | 16                        |



 

## <a name="bc6h-format"></a>Formato BC6H

Para obtener información más detallada sobre este formato, consulte la [documentación de FORMATO BC6H.](bc6h-format.md)



| Formato de compresión de bloques | Formato DXGI                                                                      | Formato equivalente de Direct3D 9 | Bytes por bloque de 4 x 4 píxeles |
|--------------------------|----------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC6H                     | DXGI \_ FORMAT \_ BC6H \_ UF16, DXGI \_ FORMAT \_ BC6H \_ SF16, DXGI \_ FORMAT \_ BC6H \_ TYPELESS | N/D                          | 16                        |



 

El formato BC6H puede seleccionar diferentes modos de codificación para cada bloque de 4 x 4 píxeles. Hay disponibles un total de 14 modos de codificación diferentes, cada uno con unas diferencias ligeramente diferentes en la calidad visual resultante de la textura mostrada. La elección de modos permite la rápida decodización por parte del hardware con el nivel de calidad seleccionado o adaptado según el contenido de origen, pero también aumenta considerablemente la complejidad del espacio de búsqueda.

## <a name="bc7-format"></a>Formato BC7

Para obtener información más detallada sobre este formato, consulte la [documentación sobre el formato BC7.](bc7-format.md)



| Formato de compresión de bloques | Formato DXGI                                                                           | Formato equivalente de Direct3D 9 | Bytes por bloque de 4 x 4 píxeles |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC7                      | DXGI \_ FORMAT \_ BC7 \_ UNORM, DXGI \_ FORMAT \_ BC7 \_ UNORM \_ SRGB, DXGI \_ FORMAT \_ BC7 \_ TYPELESS | N/D                          | 16                        |



 

El formato BC7 puede seleccionar diferentes modos de codificación para cada bloque de 4 x 4 píxeles. Hay disponibles un total de 8 modos de codificación diferentes, cada uno con unas diferencias ligeramente diferentes en la calidad visual resultante de la textura mostrada. La elección de modos permite la rápidacodización por parte del hardware con el nivel de calidad seleccionado o adaptado según el contenido de origen, pero también aumenta considerablemente la complejidad del espacio de búsqueda.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                 | Descripción                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Formato BC6H](bc6h-format.md)<br/>                             | El formato BC6H es un formato de compresión de textura diseñado para admitir espacios de color de alto rango dinámico (HDR) en los datos de origen.<br/> |
| [Formato BC7](bc7-format.md)<br/>                               | El formato BC7 es un formato de compresión de textura que se usa para la compresión de alta calidad de datos RGB y RGBA.<br/>                    |
| [Referencia del modo de formato BC7](bc7-format-mode-reference.md)<br/> | Esta documentación contiene una lista de los 8 modos de bloque y las asignaciones de bits para los bloques de formato de compresión de textura BC7.<br/>    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compresión de bloques (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

