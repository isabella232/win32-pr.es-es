---
description: En esta sección se especifican los formatos [**(DXGI_FORMAT_)** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de nivel de característica 12.1 de Direct3D.
ms.assetid: 0DC50FF3-3193-4F3B-9976-EE504C6FCC87
title: Compatibilidad con el formato de hardware de la característica de nivel 12.1 de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065192ffadf8667f82c0e1b0fc6fac165f103a7ed28982cba1fbc0e14ae47cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068765"
---
# <a name="format-support-for-direct3d-feature-level-121-hardware"></a>Compatibilidad con el formato de hardware de la característica de nivel 12.1 de Direct3D

En esta sección se especifican los formatos [**(DXGI_FORMAT_)** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de nivel de característica 12.1 de Direct3D.

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

## <a name="dxgi_format_unknownsuplsup-0"></a>DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 0 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | ![requerido](images/letter-r.jpg) |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
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
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32_TYPELESS<sup>PCS</sup> (1)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a>DXGI_FORMAT_R32G32B32A32_FLOAT<sup>FCS</sup> (2)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | ![requerido](images/letter-r.jpg) |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a>DXGI_FORMAT_R32G32B32A32_UINT<sup>FCS</sup> (3)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | ![requerido](images/letter-r.jpg) |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | ![requerido](images/letter-r.jpg) |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a>DXGI_FORMAT_R32G32B32A32_SINT<sup>FCS</sup> (4)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | ![requerido](images/letter-r.jpg) |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32_TYPELESS<sup>PCS</sup> (5)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 96 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a>DXGI_FORMAT_R32G32B32_FLOAT<sup>FCS</sup> (6)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 96 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | ![requerido](images/letter-r.jpg) |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![opcional](images/letter-o.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![opcional](images/letter-o.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![opcional](images/letter-o.jpg) |
| RenderTarget | ![opcional](images/letter-o.jpg) |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Dependiente](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Dependiente](images/letter-d.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a>DXGI_FORMAT_R32G32B32_UINT<sup>FCS</sup> (7)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 96 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | ![requerido](images/letter-r.jpg) |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![opcional](images/letter-o.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | ![requerido](images/letter-r.jpg) |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Dependiente](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Dependiente](images/letter-d.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a>DXGI_FORMAT_R32G32B32_SINT<sup>FCS</sup> (8)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 96 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | ![requerido](images/letter-r.jpg) |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![opcional](images/letter-o.jpg) |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Dependiente](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Dependiente](images/letter-d.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16_TYPELESS<sup>PCS</sup> (9)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Shader ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a>DXGI_FORMAT_R16G16B16A16_FLOAT<sup>FCS</sup> (10)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | ![requerido](images/letter-r.jpg) |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a>DXGI_FORMAT_R16G16B16A16_UNORM<sup>FCS</sup> (11)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a>DXGI_FORMAT_R16G16B16A16_UINT<sup>FCS</sup> (12)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | ![requerido](images/letter-r.jpg) |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a>DXGI_FORMAT_R16G16B16A16_SNORM<sup>FCS</sup> (13)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a>DXGI_FORMAT_R16G16B16A16_SINT<sup>FCS</sup> (14)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32_TYPELESS<sup>PCS</sup> (15)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a>DXGI_FORMAT_R32G32_FLOAT<sup>FCS</sup> (16)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | ![requerido](images/letter-r.jpg) |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a>DXGI_FORMAT_R32G32_UINT<sup>FCS</sup> (17)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | ![requerido](images/letter-r.jpg) |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | ![requerido](images/letter-r.jpg) |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a>DXGI_FORMAT_R32G32_SINT<sup>FCS</sup> (18)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | ![requerido](images/letter-r.jpg) |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g8x24_typelesssupvsup-19"></a>DXGI_FORMAT_R32G8X24_TYPELESS<sup>V</sup> (19)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupvsup-20"></a>DXGI_FORMAT_D32_FLOAT_S8X24_UINT<sup>V</sup> (20)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupvsup-21"></a>DXGI_FORMAT_R32_FLOAT_X8X24_TYPELESS<sup>V</sup> (21)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | ![requerido](images/letter-r.jpg) |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupvsup-22"></a>DXGI_FORMAT_X32_TYPELESS_G8X24_UINT<sup>V</sup> (22)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2_TYPELESS<sup>PCS</sup> (23)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Shader ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a>DXGI_FORMAT_R10G10B10A2_UNORM<sup>FCS</sup> (24)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | ![requerido](images/letter-r.jpg) |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a>DXGI_FORMAT_R10G10B10A2_UINT<sup>FCS</sup> (25)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | ![requerido](images/letter-r.jpg) |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a>DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM<sup>FCS</sup> (89)
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
| TextureCube | \- |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | ![requerido](images/letter-r.jpg) |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10_FLOAT<sup>FNS</sup> (26)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8_TYPELESS<sup>PCS</sup> (27)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a>DXGI_FORMAT_R8G8B8A8_UNORM<sup>FCS</sup> (28)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | ![requerido](images/letter-r.jpg) |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB<sup>FCS</sup> (29)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | ![requerido](images/letter-r.jpg) |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a>DXGI_FORMAT_R8G8B8A8_UINT<sup>FCS</sup> (30)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | ![requerido](images/letter-r.jpg) |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a>DXGI_FORMAT_R8G8B8A8_SNORM<sup>FCS</sup> (31)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a>DXGI_FORMAT_R8G8B8A8_SINT<sup>FCS</sup> (32)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16_TYPELESS<sup>PCS</sup> (33)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a>DXGI_FORMAT_R16G16_FLOAT<sup>FCS</sup> (34)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a>DXGI_FORMAT_R16G16_UNORM<sup>FCS</sup> (35)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a>DXGI_FORMAT_R16G16_UINT<sup>FCS</sup> (36)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | ![requerido](images/letter-r.jpg) |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a>DXGI_FORMAT_R16G16_SNORM<sup>FCS</sup> (37)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a>DXGI_FORMAT_R16G16_SINT<sup>FCS</sup> (38)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32_TYPELESS<sup>PCS</sup> (39)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | ![requerido](images/letter-r.jpg) |
| UAV estructurado y SRV | \- |
| UAV con tipo | \- |
| Almacén con tipo UAV | \- |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a>DXGI_FORMAT_D32_FLOAT<sup>FCS</sup> (40)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a>DXGI_FORMAT_R32_FLOAT<sup>FCS</sup> (41)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | ![requerido](images/letter-r.jpg) |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | ![requerido](images/letter-r.jpg) |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | ![requerido](images/letter-r.jpg) |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a>DXGI_FORMAT_R32_UINT<sup>FCS</sup> (42)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de salida de flujo | ![requerido](images/letter-r.jpg) |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | ![requerido](images/letter-r.jpg) |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| Adición atómica de UAV | ![requerido](images/letter-r.jpg) |
| Operaciones bit a bit atómicas de UAV | ![requerido](images/letter-r.jpg) |
| UAV Atomic Cmp&Store/Cmp&Exch | ![requerido](images/letter-r.jpg) |
| UAV Atomic Exchange | ![requerido](images/letter-r.jpg) |
| UAV Atomic Signed Min/Max | ![requerido](images/letter-r.jpg) |
| UAV Atomic Unsigned Min/Max | ![requerido](images/letter-r.jpg) |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a>DXGI_FORMAT_R32_SINT<sup>FCS</sup> (43)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | ![requerido](images/letter-r.jpg) |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| Adición atómica de UAV | ![requerido](images/letter-r.jpg) |
| Operaciones bit a bit atómicas de UAV | ![requerido](images/letter-r.jpg) |
| UAV Atomic Cmp&Store/Cmp&Exch | ![requerido](images/letter-r.jpg) |
| UAV Atomic Exchange | ![requerido](images/letter-r.jpg) |
| UAV Atomic Signed Min/Max | ![requerido](images/letter-r.jpg) |
| UAV Atomic Unsigned Min/Max | ![requerido](images/letter-r.jpg) |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r24g8_typelesssupvsup-44"></a>DXGI_FORMAT_R24G8_TYPELESS<sup>V</sup> (44)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupvsup-45"></a>DXGI_FORMAT_D24_UNORM_S8_UINT<sup>V</sup> (45)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupvsup-46"></a>DXGI_FORMAT_R24_UNORM_X8_TYPELESS<sup>V</sup> (46)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | ![requerido](images/letter-r.jpg) |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupvsup-47"></a>DXGI_FORMAT_X24_TYPELESS_G8_UINT<sup>V</sup> (47)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8_TYPELESS<sup>PCS</sup> (48)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Shader ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a>DXGI_FORMAT_R8G8_UNORM<sup>FCS</sup> (49)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a>DXGI_FORMAT_R8G8_UINT<sup>FCS</sup> (50)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | ![requerido](images/letter-r.jpg) |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a>DXGI_FORMAT_R8G8_SNORM<sup>FCS</sup> (51)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a>DXGI_FORMAT_R8G8_SINT<sup>FCS</sup> (52)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16_TYPELESS<sup>PCS</sup> (53)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a>DXGI_FORMAT_R16_FLOAT<sup>FCS</sup> (54)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a>DXGI_FORMAT_D16_UNORM<sup>FCS</sup> (55)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a>DXGI_FORMAT_R16_UNORM<sup>FCS</sup> (56)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | ![requerido](images/letter-r.jpg) |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a>DXGI_FORMAT_R16_UINT<sup>FCS</sup> (57)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | ![requerido](images/letter-r.jpg) |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a>DXGI_FORMAT_R16_SNORM<sup>FCS</sup> (58)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a>DXGI_FORMAT_R16_SINT<sup>FCS</sup> (59)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8_TYPELESS<sup>PCS</sup> (60)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a>DXGI_FORMAT_R8_UNORM<sup>FCS</sup> (61)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a>DXGI_FORMAT_R8_UINT<sup>FCS</sup> (62)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | ![requerido](images/letter-r.jpg) |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a>DXGI_FORMAT_R8_SNORM<sup>FCS</sup> (63)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a>DXGI_FORMAT_R8_SINT<sup>FCS</sup> (64)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![requerido](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | \- |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8_UNORM<sup>FNS</sup> (65)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5_SHAREDEXP<sup>FNC</sup> (67)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
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
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8_B8G8_UNORM<sup>FNC</sup> (68)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
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
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8_G8B8_UNORM<sup>FNC</sup> (69)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1_TYPELESS<sup>PCC</sup> (70)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a>DXGI_FORMAT_BC1_UNORM <sup>FCC</sup> (71)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a>DXGI_FORMAT_BC1_UNORM_SRGB <sup>FCC</sup> (72)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2_TYPELESS<sup>PCC</sup> (73)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a>DXGI_FORMAT_BC2_UNORM <sup>FCC</sup> (74)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a>DXGI_FORMAT_BC2_UNORM_SRGB <sup>FCC</sup> (75)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3_TYPELESS<sup>PCC</sup> (76)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a>DXGI_FORMAT_BC3_UNORM <sup>FCC</sup> (77)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a>DXGI_FORMAT_BC3_UNORM_SRGB <sup>FCC</sup> (78)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4_TYPELESS<sup>PCC</sup> (79)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a>DXGI_FORMAT_BC4_UNORM <sup>FCC</sup> (80)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a>DXGI_FORMAT_BC4_SNORM <sup>FCC</sup> (81)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 64 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5_TYPELESS<sup>PCC</sup> (82)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a>DXGI_FORMAT_BC5_UNORM <sup>FCC</sup> (83)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a>DXGI_FORMAT_BC5_SNORM <sup>FCC</sup> (84)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5_UNORM<sup>FNS</sup> (85)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | ![opcional](images/letter-o.jpg) |
| Búfer de vértices del ensamblador de entrada | ![opcional](images/letter-o.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![opcional](images/letter-o.jpg) |
| Almacén con tipo UAV | ![opcional](images/letter-o.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![requerido](images/letter-r.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1_UNORM<sup>FNS</sup> (86)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 16 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![opcional](images/letter-o.jpg) |
| Búfer de vértices del ensamblador de entrada | ![opcional](images/letter-o.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![opcional](images/letter-o.jpg) |
| RenderTarget | ![opcional](images/letter-o.jpg) |
| Blendable RenderTarget | ![opcional](images/letter-o.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![opcional](images/letter-o.jpg) |
| Almacén con tipo UAV | ![opcional](images/letter-o.jpg) |
| Carga con tipo UAV | ![opcional](images/letter-o.jpg) |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga de varios muestras | ![opcional](images/letter-o.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8_TYPELESS<sup>PCS</sup> (90)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a>DXGI_FORMAT_B8G8R8A8_UNORM<sup>FCS</sup> (87)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de muestras múltiples RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | ![requerido](images/letter-r.jpg) |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a>DXGI_FORMAT_B8G8R8A8_UNORM_SRGB<sup>FCS</sup> (91)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | ![requerido](images/letter-r.jpg) |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![requerido](images/letter-r.jpg) |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8_TYPELESS<sup>PCS</sup> (92)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a>DXGI_FORMAT_B8G8R8X8_UNORM<sup>FCS</sup> (88)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | ![requerido](images/letter-r.jpg) |
| Búfer de vértices del ensamblador de entrada | ![requerido](images/letter-r.jpg) |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a>DXGI_FORMAT_B8G8R8X8_UNORM_SRGB<sup>FCS</sup> (93)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | ![requerido](images/letter-r.jpg) |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a>DXGI_FORMAT_BC6H_TYPELESS<sup>PCC</sup> (94)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a>DXGI_FORMAT_BC6H_UF16 <sup>FCC</sup> (95)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a>DXGI_FORMAT_BC6H_SF16 <sup>FCC</sup> (96)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a>DXGI_FORMAT_BC7_TYPELESS<sup>PCC</sup> (97)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a>DXGI_FORMAT_BC7_UNORM <sup>FCC</sup> (98)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a>DXGI_FORMAT_BC7_UNORM_SRGB <sup>FCC</sup> (99)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
| Compatibilidad con formato | ![requerido](images/letter-r.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_ayuvsupvsup-100"></a>DXGI_FORMAT_AYUV<sup>V</sup> (100)
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
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | ![requerido](images/letter-r.jpg) |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | ![opcional](images/letter-o.jpg) |
| Entrada del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
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
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
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
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
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
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | ![requerido](images/letter-r.jpg) |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
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
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
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
| TextureCube | \- |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | ![requerido](images/letter-r.jpg) |
| Entrada del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
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
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
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
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_p016supvsup-105"></a>DXGI_FORMAT_P016<sup>V</sup> (105)
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
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
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
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420_OPAQUE<sup>V</sup> (106)
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
| TextureCube | \- |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | ![requerido](images/letter-r.jpg) |
| Entrada del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Salida del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
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
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| Cpu que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de muestras múltiples RT | \- |
| Resolución multimuestreo | \- |
| Carga de varios muestras | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | ![opcional](images/letter-o.jpg) |
| Entrada del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_y210supvsup-108"></a>DXGI_FORMAT_Y210<sup>V</sup> (108)
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
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
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
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
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
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | \- |
| Adición atómica de UAV | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
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
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_nv11supvsup-110"></a>DXGI_FORMAT_NV11<sup>V</sup> (110)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Sombreador gather4_c | \- |
| Mipmap | \- |
| Generación automática de Mipmap | \- |
| RenderTarget | ![requerido](images/letter-r.jpg) |
| Blendable RenderTarget | ![requerido](images/letter-r.jpg) |
| Operación lógica de fusión de salida | \- |
| Profundidad/destino de galería de símbolos | \- |
| UAV y SRV sin procesar | \- |
| UAV estructurado y SRV | \- |
| UAV con tipo | ![requerido](images/letter-r.jpg) |
| Almacén con tipo UAV | ![requerido](images/letter-r.jpg) |
| Carga con tipo UAV | \- |
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
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
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_ai44supvsup-111"></a>DXGI_FORMAT_AI44<sup>V</sup> (111)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
| Compatibilidad con formatos | ![opcional](images/letter-o.jpg) |
| Buffer | \- |
| Búfer de vértices del ensamblador de entrada | \- |
| Búfer de índice del ensamblador de entrada | \- |
| Búfer de salida de flujo | \- |
| Texture1D | \- |
| Texture2D | ![requerido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
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
| BackBuffer Castable Even Fully Typed | \- |
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
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (mono 1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
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
| BackBuffer Castable Even Fully Typed | \- |
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
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a>DXGI_FORMAT_A8P8<sup>V</sup> (114)
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
| Shader ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Sombreador sample_c (filtro de comparación) | \- |
| Ejemplo de sombreador (1_bit_filter) | \- |
| Recopilación del sombreador4 | \- |
| Sombreador gather4_c | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Otros recuentos de varios muestreos RT | \- |
| Resolución multimuestreo | \- |
| Carga multimuestreo | \- |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | ![requerido](images/letter-r.jpg) |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="format-notes"></a>Notas de formato

El propósito del formato puede cambiar de un nivel de característica de hardware al siguiente.

<dl> <dt>

<sup>L:</sup> formato sin tipo
</dt> <dt>

<sup>PCS:</sup> diseño parcialmente con tipo, conversión y simple
</dt> <dt>

 <sup>FCS:</sup> diseño completo, conversión y simple
</dt> <dt>

<sup>FNS:</sup> diseño completo, no conversiónble y simple
</dt> <dt>

<sup>PCC:</sup> diseño parcialmente con tipo, conversión y complejo
</dt> <dt>

 <sup>FCC:</sup> diseño completo, conversión y complejo
</dt> <dt>

<sup>FNC:</sup> diseño completo, no conversiónble y complejo
</dt> <dt>

<sup>V:</sup> formato de vídeo
</dt> </dl>

## <a name="dxgi_format_related-topics"></a>DXGI_FORMAT_Related temas

[Niveles de características de hardware D3D12](../direct3d12/hardware-feature-levels.md)

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)
