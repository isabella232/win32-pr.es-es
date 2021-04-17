---
description: En esta tabla se enumeran los formatos de Direct3D 9 que se pueden asignar a un formato de Direct3D 10.
ms.assetid: 07c9b827-6e2e-4599-b48a-f726484b643d
title: 'Formatos heredados: asignar formatos de Direct3D 9 a Direct3D 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230b8ed17984d47a3b57ce287aa9b434a2b92aae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705291"
---
# <a name="legacy-formats-map-direct3d-9-formats-to-direct3d-10"></a>Formatos heredados: asignar formatos de Direct3D 9 a Direct3D 10

En esta tabla se enumeran los formatos de Direct3D 9 que se pueden asignar a un formato de Direct3D 10. Los formatos de Direct3D 10 se han diverge de los formatos de Direct3D 9 para que los formatos de textura y de vértices se puedan combinar para habilitar aplicaciones entre endian.



| Formato de textura/vértice/índice de Direct3D 9 | Formato de Direct3D 10 equivalente                                        |
|----------------------------------------|----------------------------------------------------------------------|
| D3DFMT \_ desconocido                        | formato de DXGI \_ \_ desconocido                                                |
| D3DFMT \_ R8G8B8                         | No disponible                                                        |
| D3DFMT \_ A8R8G8B8                       | Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM (dxgi 1,1)                             |
| D3DFMT \_ X8R8G8B8                       | Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM (dxgi 1,1)                             |
| D3DFMT \_ R5G6B5                         | Formato de DXGI \_ \_ B5G6R5 \_ UNORM (dxgi 1,2)                               |
| D3DFMT \_ X1R5G5B5                       | No disponible                                                        |
| D3DFMT \_ A1R5G5B5                       | Formato de DXGI \_ \_ B5G5R5A1 \_ UNORM (dxgi 1,2)                             |
| D3DFMT \_ A4R4G4B4                       | Formato de DXGI \_ \_ B4G4R4A4 \_ UNORM (dxgi 1,2)                             |
| D3DFMT \_ R3G3B2                         | No disponible                                                        |
| D3DFMT \_ A8                             | Formato de DXGI \_ \_ a8 \_ UNORM                                              |
| D3DFMT \_ A8R3G3B2                       | No disponible                                                        |
| D3DFMT \_ X4R4G4B4                       | No disponible                                                        |
| D3DFMT \_ A2B10G10R10                    | Formato de DXGI \_ \_ R10G10B10A2                                            |
| D3DFMT \_ A8B8G8R8                       | Formato \_ \_ de dxgi R8G8B8A8 \_ UNORM o dxgi \_ format \_ R8G8B8A8 \_ UNORM \_ sRGB |
| D3DFMT \_ X8B8G8R8                       | No disponible                                                        |
| D3DFMT \_ G16R16                         | Formato de DXGI \_ \_ R16G16 \_ UNORM                                          |
| D3DFMT \_ A2R10G10B10                    | No disponible                                                        |
| D3DFMT \_ A16B16G16R16                   | Formato de DXGI \_ \_ R16G16B16A16 \_ UNORM                                    |
| D3DFMT \_ A8P8                           | No disponible                                                        |
| D3DFMT \_ P8                             | No disponible                                                        |
| D3DFMT \_ L8                             | Formato de DXGI \_ \_ R8 \_ UNORM ¹                                            |
| D3DFMT \_ A8L8                           | No disponible                                                        |
| D3DFMT \_ A4L4                           | No disponible                                                        |
| D3DFMT \_ V8U8                           | Formato de DXGI \_ \_ R8G8 \_ SNORM                                            |
| D3DFMT \_ L6V5U5                         | No disponible                                                        |
| D3DFMT \_ X8L8V8U8                       | No disponible                                                        |
| D3DFMT \_ Q8W8V8U8                       | Formato de DXGI \_ \_ R8G8B8A8 \_ SNORM                                        |
| D3DFMT \_ V16U16                         | Formato de DXGI \_ \_ R16G16 \_ SNORM                                          |
| D3DFMT \_ W11V11U10                      | No disponible                                                        |
| D3DFMT \_ A2W10V10U10                    | No disponible                                                        |
| D3DFMT \_ UYVY                           | No disponible                                                        |
| D3DFMT \_ R8G8 \_ B8G8                     | DXGI \_ format \_ G8R8 \_ G8B8 \_ UNORM ²                                    |
| D3DFMT \_ YUY2                           | No disponible                                                        |
| D3DFMT \_ G8R8 \_ G8B8                     | DXGI \_ format \_ R8G8 \_ B8G8 \_ UNORM ²                                    |
| D3DFMT \_ DXT1                           | Formato \_ \_ de dxgi BC1 \_ UNORM o dxgi \_ format \_ BC1 \_ UNORM \_ sRGB           |
| D3DFMT \_ DXT2                           | Formato \_ \_ de dxgi BC2 \_ UNORM o dxgi \_ format \_ BC2 \_ UNORM \_ sRGB ³         |
| D3DFMT \_ DXT3                           | Formato \_ \_ de dxgi BC2 \_ UNORM o dxgi \_ format \_ BC2 \_ UNORM \_ sRGB           |
| D3DFMT \_ DXT4                           | Formato \_ \_ de dxgi BC3 \_ UNORM o dxgi \_ format \_ BC3 \_ UNORM \_ sRGB ³         |
| D3DFMT \_ DXT5                           | Formato \_ \_ de dxgi BC3 \_ UNORM o dxgi \_ format \_ BC3 \_ UNORM \_ sRGB           |
| D3DFMT \_ D16 y D3DFMT \_ D16 \_ bloqueable  | Formato de DXGI \_ \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32                            | No disponible                                                        |
| D3DFMT \_ D15S1                          | No disponible                                                        |
| D3DFMT \_ D24S8                          | No disponible                                                        |
| D3DFMT \_ D24X8                          | No disponible                                                        |
| D3DFMT \_ D24X4S4                        | No disponible                                                        |
| D3DFMT \_ D16                            | Formato de DXGI \_ \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32F \_ bloqueable                 | Formato de DXGI \_ \_ D32 \_ float                                             |
| D3DFMT \_ D24FS8                         | No disponible                                                        |
| D3DFMT \_ S1D15                          | No disponible                                                        |
| D3DFMT \_ S8D24                          | DXGI \_ format \_ D24 \_ UNORM \_ S8 \_ uint                                   |
| D3DFMT \_ X8D24                          | No disponible                                                        |
| D3DFMT \_ X4S4D24                        | No disponible                                                        |
| D3DFMT \_ L16                            | Formato de DXGI \_ \_ R16 \_ UNORM ¹                                           |
| D3DFMT \_ INDEX16                        | Formato de DXGI \_ \_ R16 \_ uint                                              |
| D3DFMT \_ INDEX32                        | Formato de DXGI \_ \_ R32 \_ uint                                              |
| D3DFMT \_ Q16W16V16U16                   | Formato de DXGI \_ \_ R16G16B16A16 \_ SNORM                                    |
| D3DFMT \_ MULTI2 \_ ARGB8                  | No disponible                                                        |
| D3DFMT \_ R16F                           | Formato de DXGI \_ \_ R16 \_ float                                             |
| D3DFMT \_ G16R16F                        | Formato de DXGI \_ \_ R16G16 \_ float                                          |
| D3DFMT \_ A16B16G16R16F                  | Formato de DXGI \_ \_ R16G16B16A16 \_ float                                    |
| D3DFMT \_ R32F                           | Formato de DXGI \_ \_ R32 \_ float                                             |
| D3DFMT \_ G32R32F                        | Formato de DXGI \_ \_ R32G32 \_ float                                          |
| D3DFMT \_ A32B32G32R32F                  | Formato de DXGI \_ \_ R32G32B32A32 \_ float                                    |
| D3DFMT \_ CxV8U8                         | No disponible                                                        |
| D3DDECLTYPE \_ FLOAT1                    | Formato de DXGI \_ \_ R32 \_ float                                             |
| D3DDECLTYPE \_ FLOAT2                    | Formato de DXGI \_ \_ R32G32 \_ float                                          |
| D3DDECLTYPE \_ FLOAT3                    | Formato de DXGI \_ \_ R32G32B32 \_ float                                       |
| D3DDECLTYPE \_ FLOAT4                    | Formato de DXGI \_ \_ R32G32B32A32 \_ float                                    |
| D3DDECLTYPED3DCOLOR                    | No disponible                                                        |
| D3DDECLTYPE \_ UBYTE4                    | Formato de DXGI \_ \_ R8G8B8A8 \_ uint ⁴                                       |
| D3DDECLTYPE \_ SHORT2                    | Formato de DXGI \_ \_ R16G16 \_ Sint                                           |
| D3DDECLTYPE \_ SHORT4                    | Formato de DXGI \_ \_ R16G16B16A16 \_ Sint                                     |
| D3DDECLTYPE \_ UBYTE4N                   | Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM                                        |
| D3DDECLTYPE \_ SHORT2N                   | Formato de DXGI \_ \_ R16G16 \_ SNORM                                          |
| D3DDECLTYPE \_ SHORT4N                   | Formato de DXGI \_ \_ R16G16B16A16 \_ SNORM                                    |
| D3DDECLTYPE \_ USHORT2N                  | Formato de DXGI \_ \_ R16G16 \_ UNORM                                          |
| D3DDECLTYPE \_ USHORT4N                  | Formato de DXGI \_ \_ R16G16B16A16 \_ UNORM                                    |
| D3DDECLTYPE \_ UDEC3                     | No disponible                                                        |
| D3DDECLTYPE \_ DEC3N                     | No disponible                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2                | Formato de DXGI \_ \_ R16G16 \_ float                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4                | Formato de DXGI \_ \_ R16G16B16A16 \_ float                                    |



 

1.  Use. r swizzle en un sombreador para duplicar el rojo en otros componentes para obtener el comportamiento de Direct3D 9.
2.  En Direct3D 9, los datos se escalaron verticalmente 255.0 f, lo que se puede hacer en el código del sombreador en su lugar.
3.  DXT2 y DXT3 son los mismos desde una perspectiva de API; DXT4 y DXT5 son los mismos desde una perspectiva de API. La única diferencia es alfa premultiplicado, que puede ser sometido a seguimiento por una aplicación y no necesita un formato diferente.
4.  Un sombreador obtiene valores UINT, pero si el estilo de Direct3D 9 es Float entero (0,0 f, 1,0 f... se necesita 255. f), UINT se puede convertir en float32 en un sombreador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



