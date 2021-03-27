---
title: Compresión de bloque de textura en Direct3D 11
description: La compatibilidad con la compresión de bloques (BC) para las texturas se ha ampliado en Direct3D 11 para incluir los algoritmos BC6H y BC7.
ms.assetid: E0735D4E-9C0F-45DC-854A-C27EB8367D86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f80a22c97c8a706a3825abfb4ac2b5133c1a9beb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149317"
---
# <a name="texture-block-compression-in-direct3d-11"></a>Compresión de bloque de textura en Direct3D 11

La compatibilidad con la compresión de bloques (BC) para las texturas se ha ampliado en Direct3D 11 para incluir los algoritmos BC6H y BC7. BC6H es compatible con los datos de origen de color de alto nivel dinámico y BC7 proporciona una compresión de calidad mejor que la media con menos artefactos para los datos de origen RGB estándar.

Para obtener información más específica acerca de la compatibilidad con algoritmos de compresión de bloque antes de Direct3D 11, incluida la compatibilidad con los formatos de BC1 a BC5, vea [compresión de bloques (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression).

**Nota sobre los formatos de archivo:** Los formatos de compresión de textura BC6H y BC7 usan el formato de archivo DDS para almacenar los datos de textura comprimidos. Para obtener más información, consulte la [Guía de programación para DDS](/windows/desktop/direct3ddds/dx-graphics-dds-pguide) .

## <a name="block-compression-formats-supported-in-direct3d-11"></a>Formatos de compresión de bloque admitidos en Direct3D 11



| Datos de origen                                  | Resolución de compresión de datos mínima requerida                              | Formato recomendado | Nivel mínimo de características admitidas |
|----------------------------------------------|---------------------------------------------------------------------------|--------------------|---------------------------------|
| Color de tres canales con canal alfa       | Tres canales de color (5 bits: 6 bits: 5 bits), con 0 o 1 bit (s) de alfa  | BC1                | Direct3D 9,1                    |
| Color de tres canales con canal alfa       | Tres canales de color (5 bits: 6 bits: 5 bits), con 4 bits de alfa         | BC2                | Direct3D 9,1                    |
| Color de tres canales con canal alfa       | Tres canales de color (5 bits: 6 bits: 5 bits) con 8 bits de alfa          | BC3                | Direct3D 9,1                    |
| Color de un canal                            | Un canal de color (8 bits)                                                | LAS texturas BC4                | Direct3D 10                     |
| Color de dos canales                            | Dos canales de color (8 bits: 8 bits)                                        | BC5                | Direct3D 10                     |
| Color de intervalo dinámico alto (HDR) de tres canales | Tres canales de color (16 bits: 16 bits: 16 bits) en el punto flotante "medio"\* | BC6H               | Direct3D 11                     |
| Color de tres canales, canal alfa opcional  | Tres canales de color (de 4 a 7 bits por canal) con de 0 a 8 bits de alfa  | BC7                | Direct3D 11                     |



 

\*El punto flotante "medio" es un valor de 16 bits que consta de un bit de signo opcional, un exponente sesgado de 5 bits y una mantisa de 10 o 11 bits.

## <a name="bc1-bc2-and-b3-formats"></a>Formatos BC1, BC2 y B3

Los formatos BC1, BC2 y BC3 son equivalentes a los formatos de compresión de textura de Direct3D 9 DXTn y son los mismos que los correspondientes formatos de Direct3D 10 BC1, BC2 y BC3. La compatibilidad con estos tres formatos es necesaria para todos los niveles de características (nivel de característica de D3D \_ \_ \_ 9 \_ 1, nivel de característica de D3D \_ \_ \_ 9 \_ 2, nivel de característica de D3D \_ \_ 9 3, nivel de característica de D3D \_ \_ \_ \_ \_ 10 \_ 0, \_ \_ nivel de característica de D3D \_ 10 \_ 1 y \_ nivel de característica \_ \_ 11 0 de D3D \_ .



| Formato de compresión de bloque | Formato de DXGI                                                                           | Formato equivalente de Direct3D 9                               | Bytes por bloque de píxeles 4x4 |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------|---------------------------|
| BC1                      | DXGI \_ format \_ BC1 \_ UNORM, \_ formato dxgi \_ BC1 \_ UNORM \_ sRGB, dxgi \_ format \_ BC1 \_ sin tipo | D3DFMT \_ DXT1, FourCC = "DXT1"                                | 8                         |
| BC2                      | DXGI \_ format \_ BC2 \_ UNORM, \_ formato dxgi \_ BC2 \_ UNORM \_ sRGB, dxgi \_ format \_ BC2 \_ sin tipo | D3DFMT \_ DXT2 \* , FourCC = "DXT2", D3DFMT \_ DXT3, FourCC = "DXT3" | 16                        |
| BC3                      | DXGI \_ format \_ BC3 \_ UNORM, \_ formato dxgi \_ BC3 \_ UNORM \_ sRGB, dxgi \_ format \_ BC3 \_ sin tipo | D3DFMT \_ DXT4 \* , FourCC = "DXT4", D3DFMT \_ DXT5, FourCC = "DXT5" | 16                        |



 

\*Estos esquemas de compresión (DXT2 y DXT4) no realizan ninguna distinción entre los formatos alfa de Direct3D 9 premultiplicados y los formatos alfa estándar. Los sombreadores programables deben controlar esta distinción en el momento de la representación.

## <a name="bc4-and-bc5-formats"></a>Formatos las texturas BC4 y BC5



| Formato de compresión de bloque | Formato de DXGI                                                                     | Formato equivalente de Direct3D 9 | Bytes por bloque de píxeles 4x4 |
|--------------------------|---------------------------------------------------------------------------------|------------------------------|---------------------------|
| LAS texturas BC4                      | Formato de DXGI \_ \_ las texturas BC4 \_ UNORM, \_ formato de dxgi \_ las texturas BC4 \_ SNORM, formato de dxgi \_ \_ las texturas BC4 \_ sin tipo | FourCC = "ATI1"                | 8                         |
| BC5                      | Formato de DXGI \_ \_ BC5 \_ UNORM, \_ formato de dxgi \_ BC5 \_ SNORM, formato de dxgi \_ \_ BC5 \_ sin tipo | FourCC = "ATI2"                | 16                        |



 

## <a name="bc6h-format"></a>Formato BC6H

Para obtener información más detallada sobre este formato, vea la documentación de [BC6H Format](bc6h-format.md) .



| Formato de compresión de bloque | Formato de DXGI                                                                      | Formato equivalente de Direct3D 9 | Bytes por bloque de píxeles 4x4 |
|--------------------------|----------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC6H                     | Formato de DXGI \_ \_ BC6H \_ UF16, \_ formato de dxgi \_ BC6H \_ SF16, formato de dxgi \_ \_ BC6H \_ sin tipo | N/D                          | 16                        |



 

El formato BC6H puede seleccionar diferentes modos de codificación para cada bloque de píxeles de 4x4. Hay disponible un total de 14 modos de codificación diferentes, cada uno con un equilibrio ligeramente diferente en la calidad visual resultante de la textura mostrada. La elección de los modos permite la descodificación rápida por el hardware con el nivel de calidad seleccionado o adaptado según el contenido de origen, pero también aumenta en gran medida la complejidad del espacio de búsqueda.

## <a name="bc7-format"></a>Formato BC7

Para obtener información más detallada sobre este formato, vea la documentación de [BC7 Format](bc7-format.md) .



| Formato de compresión de bloque | Formato de DXGI                                                                           | Formato equivalente de Direct3D 9 | Bytes por bloque de píxeles 4x4 |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC7                      | DXGI \_ format \_ BC7 \_ UNORM, \_ formato dxgi \_ BC7 \_ UNORM \_ sRGB, dxgi \_ format \_ BC7 \_ sin tipo | N/D                          | 16                        |



 

El formato BC7 puede seleccionar diferentes modos de codificación para cada bloque de píxeles de 4x4. Hay disponible un total de 8 modos de codificación diferentes, cada uno con un equilibrio ligeramente diferente en la calidad visual resultante de la textura mostrada. La elección de los modos permite la descodificación rápida por el hardware con el nivel de calidad seleccionado o adaptado según el contenido de origen, pero también aumenta en gran medida la complejidad del espacio de búsqueda.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                 | Descripción                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Formato BC6H](bc6h-format.md)<br/>                             | El formato BC6H es un formato de compresión de textura diseñado para admitir los espacios de colores de intervalos dinámicos (HDR) en los datos de origen.<br/> |
| [Formato BC7](bc7-format.md)<br/>                               | El formato BC7 es un formato de compresión de textura que se usa para la compresión de alta calidad de datos RGB y RGBA.<br/>                    |
| [Referencia del modo de formato BC7](bc7-format-mode-reference.md)<br/> | Esta documentación contiene una lista de los 8 modos de bloque y las asignaciones de bits para los bloques de formato de compresión de textura BC7.<br/>    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compresión de bloques (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

