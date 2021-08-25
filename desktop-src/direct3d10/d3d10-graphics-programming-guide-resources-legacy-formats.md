---
description: En esta tabla se enumeran los formatos de Direct3D 9 que se pueden asignar a un formato Direct3D 10.
ms.assetid: 07c9b827-6e2e-4599-b48a-f726484b643d
title: 'Formatos heredados: asignar formatos de Direct3D 9 a Direct3D 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40a437ef42b4ce24b468c39d169b39db7fb9cb7951c825da38bb63f85b9dba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895305"
---
# <a name="legacy-formats-map-direct3d-9-formats-to-direct3d-10"></a>Formatos heredados: asignar formatos de Direct3D 9 a Direct3D 10

En esta tabla se enumeran los formatos de Direct3D 9 que se pueden asignar a un formato Direct3D 10. Los formatos de Direct3D 10 han divergido de los formatos Direct3D 9 para que los formatos de vértice y textura se puedan combinar para habilitar las aplicaciones cross-endian.



| Formato de textura, vértice o índice de Direct3D 9 | Formato direct3D 10 equivalente                                        |
|----------------------------------------|----------------------------------------------------------------------|
| D3DFMT \_ UNKNOWN                        | FORMATO DXGI \_ \_ DESCONOCIDO                                                |
| D3DFMT \_ R8G8B8                         | No disponible                                                        |
| D3DFMT \_ A8R8G8B8                       | DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM (DXGI 1.1)                             |
| D3DFMT \_ X8R8G8B8                       | DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM (DXGI 1.1)                             |
| D3DFMT \_ R5G6B5                         | DXGI \_ FORMAT \_ B5G6R5 \_ UNORM (DXGI 1.2)                               |
| D3DFMT \_ X1R5G5B5                       | No disponible                                                        |
| D3DFMT \_ A1R5G5B5                       | DXGI \_ FORMAT \_ B5G5R5A1 \_ UNORM (DXGI 1.2)                             |
| D3DFMT \_ A4R4G4B4                       | FORMATO \_ DXGI \_ B4G4R4A4 \_ UNORM (DXGI 1.2)                             |
| D3DFMT \_ R3G3B2                         | No disponible                                                        |
| D3DFMT \_ A8                             | DXGI \_ FORMAT \_ A8 \_ UNORM                                              |
| D3DFMT \_ A8R3G3B2                       | No disponible                                                        |
| D3DFMT \_ X4R4G4B4                       | No disponible                                                        |
| D3DFMT \_ A2B10G10R10                    | FORMATO DXGI \_ \_ R10G10B10A2                                            |
| D3DFMT \_ A8B8G8R8                       | FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM o DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB |
| D3DFMT \_ X8B8G8R8                       | No disponible                                                        |
| D3DFMT \_ G16R16                         | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                          |
| D3DFMT \_ A2R10G10B10                    | No disponible                                                        |
| D3DFMT \_ A16B16G16R16                   | DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM                                    |
| D3DFMT \_ A8P8                           | No disponible                                                        |
| D3DFMT \_ P8                             | No disponible                                                        |
| D3DFMT \_ L8                             | DXGI \_ FORMAT \_ R8 \_ UNORM ¹                                            |
| D3DFMT \_ A8L8                           | No disponible                                                        |
| D3DFMT \_ A4L4                           | No disponible                                                        |
| D3DFMT \_ V8U8                           | DXGI \_ FORMAT \_ R8G8 \_ SNORM                                            |
| D3DFMT \_ L6V5U5                         | No disponible                                                        |
| D3DFMT \_ X8L8V8U8                       | No disponible                                                        |
| D3DFMT \_ Q8W8V8U8                       | FORMATO DXGI \_ \_ R8G8B8A8 \_ SNORM                                        |
| D3DFMT \_ V16U16                         | DXGI \_ FORMAT \_ R16G16 \_ SNORM                                          |
| D3DFMT \_ W11V11U10                      | No disponible                                                        |
| D3DFMT \_ A2W10V10U10                    | No disponible                                                        |
| D3DFMT \_ UYVY                           | No disponible                                                        |
| D3DFMT \_ R8G8 \_ B8G8                     | FORMATO DXGI \_ \_ G8R8 \_ G8B8 \_ UNORM MIENTO                                    |
| D3DFMT \_ YUY2                           | No disponible                                                        |
| D3DFMT \_ G8R8 \_ G8B8                     | DXGI \_ FORMAT \_ R8G8 \_ B8G8 \_ UNORM NTES                                    |
| D3DFMT \_ DXT1                           | FORMATO DXGI \_ \_ BC1 \_ UNORM o DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB           |
| D3DFMT \_ DXT2                           | FORMATO DXGI \_ \_ BC2 \_ UNORM o DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB 7         |
| D3DFMT \_ DXT3                           | FORMATO DXGI \_ \_ BC2 \_ UNORM o DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB           |
| D3DFMT \_ DXT4                           | FORMATO DXGI \_ \_ BC3 \_ UNORM o DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB 7         |
| D3DFMT \_ DXT5                           | FORMATO DXGI \_ \_ BC3 \_ UNORM o DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB           |
| D3DFMT \_ D16 y D3DFMT \_ D16 \_ LOCKABLE  | DXGI \_ FORMAT \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32                            | No disponible                                                        |
| D3DFMT \_ D15S1                          | No disponible                                                        |
| D3DFMT \_ D24S8                          | No disponible                                                        |
| D3DFMT \_ D24X8                          | No disponible                                                        |
| D3DFMT \_ D24X4S4                        | No disponible                                                        |
| D3DFMT \_ D16                            | DXGI \_ FORMAT \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32F \_ LOCKABLE                 | DXGI \_ FORMAT \_ D32 \_ FLOAT                                             |
| D3DFMT \_ D24FS8                         | No disponible                                                        |
| D3DFMT \_ S1D15                          | No disponible                                                        |
| D3DFMT \_ S8D24                          | DXGI \_ FORMAT \_ D24 \_ UNORM \_ S8 \_ UINT                                   |
| D3DFMT \_ X8D24                          | No disponible                                                        |
| D3DFMT \_ X4S4D24                        | No disponible                                                        |
| D3DFMT \_ L16                            | DXGI \_ FORMAT \_ R16 \_ UNORM ¹                                           |
| D3DFMT \_ INDEX16                        | DXGI \_ FORMAT \_ R16 \_ UINT                                              |
| D3DFMT \_ INDEX32                        | DXGI \_ FORMAT \_ R32 \_ UINT                                              |
| D3DFMT \_ Q16W16V16U16                   | DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM                                    |
| D3DFMT \_ MULTI2 \_ ARGB8                  | No disponible                                                        |
| D3DFMT \_ R16F                           | DXGI \_ FORMAT \_ R16 \_ FLOAT                                             |
| D3DFMT \_ G16R16F                        | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                          |
| D3DFMT \_ A16B16G16R16F                  | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                    |
| D3DFMT \_ R32F                           | DXGI \_ FORMAT \_ R32 \_ FLOAT                                             |
| D3DFMT \_ G32R32F                        | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                          |
| D3DFMT \_ A32B32G32R32F                  | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                    |
| D3DFMT \_ CxV8U8                         | No disponible                                                        |
| D3DDECLTYPE \_ FLOAT1                    | DXGI \_ FORMAT \_ R32 \_ FLOAT                                             |
| D3DDECLTYPE \_ FLOAT2                    | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                          |
| D3DDECLTYPE \_ FLOAT3                    | DXGI \_ FORMAT \_ R32G32B32 \_ FLOAT                                       |
| D3DDECLTYPE \_ FLOAT4                    | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                    |
| D3DDECLTYPED3DCOLOR                    | No disponible                                                        |
| D3DDECLTYPE \_ UBYTE4                    | Formato DXGI \_ \_ R8G8B8A8 \_ UINT ⁴                                       |
| D3DDECLTYPE \_ SHORT2                    | DXGI \_ FORMAT \_ R16G16 \_ SINT                                           |
| D3DDECLTYPE \_ SHORT4                    | FORMATO DXGI \_ \_ R16G16B16A16 \_ SINT                                     |
| D3DDECLTYPE \_ UBYTE4N                   | DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM                                        |
| D3DDECLTYPE \_ SHORT2N                   | DXGI \_ FORMAT \_ R16G16 \_ SNORM                                          |
| D3DDECLTYPE \_ SHORT4N                   | DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM                                    |
| D3DDECLTYPE \_ USHORT2N                  | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                          |
| D3DDECLTYPE \_ USHORT4N                  | DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM                                    |
| D3DDECLTYPE \_ UDEC3                     | No disponible                                                        |
| D3DDECLTYPE \_ DEC3N                     | No disponible                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2                | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4                | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                    |



 

1.  Use .r swzzle en un sombreador para duplicar el rojo a otros componentes para obtener el comportamiento de Direct3D 9.
2.  En Direct3D 9, los datos se escalaron verticalmente en 255,0f, lo que se puede hacer en el código del sombreador en su lugar.
3.  DXT2 y DXT3 son iguales desde la perspectiva de la API. DXT4 y DXT5 son los mismos desde la perspectiva de la API. La única diferencia era alfa premultiplicado, cuyo seguimiento puede realizar una aplicación y no necesita un formato independiente.
4.  Un sombreador obtiene valores UINT, pero si el estilo entero de Direct3D 9 flota (0,0f, 1,0f... Se necesitan 255.f), UINT se puede convertir a float32 en un sombreador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



