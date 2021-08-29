---
description: En esta sección se especifican los formatos [**(DXGI_FORMAT_)** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de Direct3D Feature 10Level9 9.1.
ms.assetid: 770A5396-C5D9-442B-99FE-3D220C54E8EB
title: Compatibilidad con el formato de hardware de la característica de nivel 9.1 de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce82c18804d1712a3ad8d731d82ba69537dc9e51ebffcfc22d22b3ccbb29c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627405"
---
# <a name="format-support-for-direct3d-feature-10level9-91-hardware"></a>Compatibilidad con el formato de hardware de la característica de nivel 9.1 de Direct3D

En esta sección se especifican los formatos [**(DXGI_FORMAT_)** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de Direct3D Feature 10Level9 9.1.

En la tabla se resume la compatibilidad con características con la siguiente clave.

| Símbolo                            | Descripción                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| **-**                             | No está permitido o no está disponible.                                                  |
| ![requerido](images/letter-r.jpg)  | Se requiere compatibilidad con hardware.                                                 |
| ![opcional](images/letter-o.jpg)  | Compatibilidad con hardware opcional, el formato puede ser o no acelerado por hardware. |
| ![Dependiente](images/letter-d.jpg) | Obligatorio si se admite la característica opcional relacionada.                            |

Este tema contiene una sección por formato. Un destino *de formato* (las tablas contienen una fila por destino) puede ser un tipo de recurso, una función intrínseca HLSL o una funcionalidad determinada que depende de un formato determinado.

Para comprobar mediante programación la compatibilidad con formato en D3D11 y D3D12, consulte Comprobación de la compatibilidad con características [de hardware.](checking-hardware-feature-support.md)

> [!NOTE] 
> Los números de los formatos son principalmente, pero no todos, en orden numérico ascendente, algunos están fuera del orden numérico y se enumeran junto &mdash; con otros formatos pertinentes. Tenga en *cuenta* también que sin  tipo en un nombre de formato puede [](#format-notes) significar parcialmente con tipo y no estrictamente sin tipo (consulte la sección Notas de formato al final del tema).

// 

## <a name="dxgi_format_unknownsuplsup-0"></a>DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 0 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32 PC \_ SIN<sup>TIPO</sup> (1)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a>DXGI_FORMAT_R32G32B32A32 FLOAT \_ <sup>FNS</sup> (2)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a>DXGI_FORMAT_R32G32B32A32 \_ <sup>FNS de</sup> UINT (3)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a>DXGI_FORMAT_R32G32B32A32 \_ SINT<sup>FNS</sup> (4)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32 PC \_ SIN<sup>TIPO</sup> (5)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 96 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a>DXGI_FORMAT_R32G32B32 FLOAT \_ <sup>FNS</sup> (6)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 96 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | ![Dependiente](images/letter-d.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | ![Dependiente](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Dependiente](images/letter-d.jpg) |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a>DXGI_FORMAT_R32G32B32 \_ <sup>FNS de</sup> UINT (7)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 96 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | ![Dependiente](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Dependiente](images/letter-d.jpg) |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a>DXGI_FORMAT_R32G32B32 \_ SINT<sup>FNS</sup> (8)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 96 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | ![Dependiente](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Dependiente](images/letter-d.jpg) |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16 PC \_ SIN<sup>TIPO</sup> (9)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a>DXGI_FORMAT_R16G16B16A16 FLOAT \_ <sup>FNS</sup> (10)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>FNS UNORM</sup> (11)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>FNS de</sup> UINT (12)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>FNS</sup> de SNORM (13)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a>DXGI_FORMAT_R16G16B16A16 \_ SINT<sup>FNS</sup> (14)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32 PC \_ SIN<sup>TIPO</sup> (15)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a>DXGI_FORMAT_R32G32 FLOAT \_ <sup>FNS</sup> (16)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a>DXGI_FORMAT_R32G32 \_ <sup>FNS de</sup> UINT (17)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a>DXGI_FORMAT_R32G32 \_ SINT<sup>FNS</sup> (18)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a>DXGI_FORMAT_R32G8X24 PC \_ SIN<sup>TIPO</sup> (19)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a>DXGI_FORMAT_D32 \_ FLOAT \_ S8X24 \_ UINT<sup>FNS</sup> (20)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a>DXGI_FORMAT_R32 FNS SIN TIPO \_ FLOAT \_ X8X24 \_ (21)<sup></sup>
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a>DXGI_FORMAT_X32 \_ \_ \_ <sup>FNS</sup> de UINT G8X24 SIN TIPO (22)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2 PC \_ SIN<sup>TIPO</sup> (23)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a>DXGI_FORMAT_R10G10B10A2 \_ <sup>FNS de</sup> UNORM (24)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a>DXGI_FORMAT_R10G10B10A2 \_ <sup>FNS de</sup> UINT (25)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a>DXGI_FORMAT_R10G10B10 \_ \_ FNS \_ UNORM DE XR BIAS A2 \_ (89)<sup></sup>
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10 FLOAT \_ <sup>FNS</sup> (26)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8 PC \_ SIN<sup>TIPO</sup> (27)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | ![requerido](images/letter-r.jpg) |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ SRGB<sup>FNS</sup> (29)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | ![requerido](images/letter-r.jpg) |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>FNS de</sup> UINT (30)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>FNS</sup> de SNORM (31)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a>DXGI_FORMAT_R8G8B8A8 \_ SINT<sup>FNS</sup> (32)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16 \_ PC SIN<sup>TIPO</sup> (33)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a>DXGI_FORMAT_R16G16 FLOAT \_ <sup>FNS</sup> (34)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a>DXGI_FORMAT_R16G16 \_ <sup>FNS UNORM</sup> (35)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a>DXGI_FORMAT_R16G16 \_ <sup>FNS de</sup> UINT (36)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a>DXGI_FORMAT_R16G16 \_ <sup>FNS</sup> de SNORM (37)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a>DXGI_FORMAT_R16G16 \_ SINT<sup>FNS</sup> (38)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32 PC \_ SIN<sup>TIPO</sup> (39)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a>DXGI_FORMAT_D32 FLOAT \_ <sup>FNS</sup> (40)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a>DXGI_FORMAT_R32 FLOAT \_ <sup>FNS</sup> (41)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a>DXGI_FORMAT_R32 \_ <sup>FNS de</sup> UINT (42)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a>DXGI_FORMAT_R32 \_ SINT<sup>FNS</sup> (43)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a>DXGI_FORMAT_R24G8 PC \_ SIN<sup>TIPO</sup> (44)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a>DXGI_FORMAT_D24 \_ FNS UINT de UNORM \_ S8 \_ (45)<sup></sup>
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | ![requerido](images/letter-r.jpg) |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a>DXGI_FORMAT_R24 \_ FNS SIN TIPO DE UNORM \_ X8 \_ (46)<sup></sup>
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a>DXGI_FORMAT_X24 \_ \_ \_ <sup>FNS</sup> de UINT G8 sin TIPO (47)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8 PC \_ SIN<sup>TIPO</sup> (48)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a>DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a>DXGI_FORMAT_R8G8 \_ <sup>FNS de</sup> UINT (50)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a>DXGI_FORMAT_R8G8 \_ <sup>FNS</sup> de SNORM (51)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a>DXGI_FORMAT_R8G8 \_ SINT<sup>FNS</sup> (52)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16 PC \_ SIN<sup>TIPO</sup> (53)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a>DXGI_FORMAT_R16 FLOAT \_ <sup>FNS</sup> (54)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a>DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | ![requerido](images/letter-r.jpg) |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a>DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a>DXGI_FORMAT_R16 \_ <sup>FNS de</sup> UINT (57)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a>DXGI_FORMAT_R16 \_ <sup>FNS</sup> de SNORM (58)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a>DXGI_FORMAT_R16 \_ SINT<sup>FNS</sup> (59)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8 PC \_ SIN<sup>TIPO</sup> (60)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a>DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a>DXGI_FORMAT_R8 \_ <sup>FNS de</sup> UINT (62)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a>DXGI_FORMAT_R8 \_ SNORM<sup>FNS</sup> (63)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a>DXGI_FORMAT_R8 \_ SINT<sup>FNS</sup> (64)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8 \_ <sup>FNS unorm</sup> (65)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8 \_ FNC de \_ UNORM<sup>G8B8</sup> (69)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1 \_ <sup>PCC</sup> SIN TIPO (70)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 4 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a>DXGI_FORMAT_BC1 \_ <sup>FNC de</sup> UNORM (71)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 4 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a>DXGI_FORMAT_BC1 \_ UNORM \_ SRGB<sup>FNC</sup> (72)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 4 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2 \_ <sup>PCC</sup> SIN TIPO (73)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a>DXGI_FORMAT_BC2 \_ <sup>FNC de</sup> UNORM (74)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a>DXGI_FORMAT_BC2 \_ UNORM \_ SRGB<sup>FNC</sup> (75)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3 \_ <sup>PCC</sup> SIN TIPO (76)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a>DXGI_FORMAT_BC3 \_ <sup>FNC de</sup> UNORM (77)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a>DXGI_FORMAT_BC3 \_ UNORM \_ SRGB<sup>FNC</sup> (78)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4 \_ <sup>PCC</sup> SIN TIPO (79)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 4 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a>DXGI_FORMAT_BC4 \_ <sup>FNC DE</sup> UNORM (80)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 4 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a>DXGI_FORMAT_BC4 \_ <sup>FNC</sup> de SNORM (81)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 4 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5 \_ <sup>PCC</sup> sin TIPO (82)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a>DXGI_FORMAT_BC5 \_ <sup>FNC de</sup> UNORM (83)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a>DXGI_FORMAT_BC5 \_ <sup>FNC</sup> de SNORM (84)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5 \_ <sup>FNS de</sup> UNORM (85)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1 \_ <sup>FNS de</sup> UNORM (86)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8 PC \_ SIN<sup>TIPO</sup> (90)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a>DXGI_FORMAT_B8G8R8A8 \_ <sup>FNS de</sup> UNORM (87)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | ![requerido](images/letter-r.jpg) |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ SRGB<sup>FNS</sup> (91)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | ![requerido](images/letter-r.jpg) |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8 PC \_ SIN<sup>TIPO</sup> (92)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | \- |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a>DXGI_FORMAT_B8G8R8X8 \_ <sup>FNS de</sup> UNORM (88)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a>DXGI_FORMAT_B8G8R8X8 \_ \_ UNORM SRGB<sup>FNS</sup> (93)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a>DXGI_FORMAT_AYUV<sup>V</sup> (100)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | ![opcional](images/letter-o.jpg) |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_y410supvsup-101"></a>DXGI_FORMAT_Y410<sup>V</sup> (101)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | ![opcional](images/letter-o.jpg) |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_y416supvsup-102"></a>DXGI_FORMAT_Y416<sup>V</sup> (102)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | ![opcional](images/letter-o.jpg) |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | ![opcional](images/letter-o.jpg) |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_p010supvsup-104"></a>DXGI_FORMAT_P010<sup>V</sup> (104)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | ![opcional](images/letter-o.jpg) |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_p016supvsup-105"></a>DXGI_FORMAT_P016<sup>V</sup> (105)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | ![opcional](images/letter-o.jpg) |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420 OPAQUE \_ <sup>V</sup> (106)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | ![requerido](images/letter-r.jpg) |
| Entrada del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min or Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | ![opcional](images/letter-o.jpg) |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_y210supvsup-108"></a>DXGI_FORMAT_Y210<sup>V</sup> (108)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | ![opcional](images/letter-o.jpg) |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_y216supvsup-109"></a>DXGI_FORMAT_Y216<sup>V</sup> (109)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | ![opcional](images/letter-o.jpg) |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_nv11supvsup-110"></a>DXGI_FORMAT_NV11<sup>V</sup> (110)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | ![opcional](images/letter-o.jpg) |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_ai44supvsup-111"></a>DXGI_FORMAT_AI44<sup>V</sup> (111)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_ia44supvsup-112"></a>DXGI_FORMAT_IA44<sup>V</sup> (112)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_p8supvsup-113"></a>DXGI_FORMAT_P8<sup>V</sup> (113)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a>DXGI_FORMAT_A8P8<sup>V</sup> (114)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Ejemplo de sombreador (solo ejemplo de punto) | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a>DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (solo ejemplo de punto) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min o Max | \- |
| UAV Atomic Unsigned Min o Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| Recurso en mosaico | \- |

## <a name="format-notes"></a>Notas de formato

El propósito del formato puede cambiar de un nivel de característica de hardware al siguiente.

<dl> <dt>

<sup>L:</sup> formato sin tipo
</dt> <dt>

<sup>PCS:</sup> diseño parcialmente con tipo, conversión y simple
</dt> <dt>

 <sup>FCS:</sup> diseño totalmente con tipo, conversión y simple
</dt> <dt>

<sup>FNS:</sup> diseño totalmente con tipo, no conversión y simple
</dt> <dt>

<sup>PCC:</sup> diseño parcialmente con tipo, conversión y complejo
</dt> <dt>

 <sup>FCC:</sup> diseño totalmente con tipo, conversión y complejo
</dt> <dt>

<sup>FNC:</sup> diseño completo, no conversión y complejo
</dt> <dt>

<sup>V:</sup> formato de vídeo
</dt> </dl>

## <a name="related-topics"></a>Temas relacionados

[Niveles de características de hardware D3D12](../direct3d12/hardware-feature-levels.md)

[Implementación de búferes de sombra para el nivel 9 de característica de Direct3D](/previous-versions/windows/apps/jj262110(v=win.10))

[Asignar formatos heredados](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)
