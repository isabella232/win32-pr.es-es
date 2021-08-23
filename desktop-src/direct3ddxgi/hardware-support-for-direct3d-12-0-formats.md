---
description: En esta sección se especifican los formatos [**(DXGI_FORMAT_)** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de nivel de característica 12.0 de Direct3D.
ms.assetid: A039A82B-2E30-41A6-96B5-AD5538FE2285
title: Compatibilidad con el formato de hardware de la característica de nivel 12.0 de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f571d8529d53c15313b42b211f72d21fbf097debc61920c6108879b64df512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745625"
---
# <a name="format-support-for-direct3d-feature-level-120-hardware"></a>Compatibilidad con el formato de hardware de la característica de nivel 12.0 de Direct3D

En esta sección se especifican los formatos [**(DXGI_FORMAT_)** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de nivel de característica 12.0 de Direct3D.

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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32 PC \_ SIN<sup>TIPO</sup> (1)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a>DXGI_FORMAT_R32G32B32A32 FLOAT \_ <sup>FCS</sup> (2)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 128 |
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
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![requerido](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
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

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a>DXGI_FORMAT_R32G32B32A32 \_ UINT<sup>FCS</sup> (3)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a>DXGI_FORMAT_R32G32B32A32 \_ SINT<sup>FCS</sup> (4)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32 PC \_ SIN<sup>TIPO</sup> (5)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a>DXGI_FORMAT_R32G32B32 FLOAT \_ <sup>FCS</sup> (6)
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
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![opcional](images/letter-o.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![opcional](images/letter-o.jpg) |
| Shader gather4 \_ c | \- |
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
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a>DXGI_FORMAT_R32G32B32 \_ <sup>FCS</sup> de UINT (7)
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
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a>DXGI_FORMAT_R32G32B32 \_ <sup>FCS</sup> SINT (8)
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
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16 PC \_ SIN<sup>TIPO</sup> (9)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a>DXGI_FORMAT_R16G16B16A16 \_ FLOAT<sup>FCS</sup> (10)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a>DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FCS</sup> (11)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>FCS</sup> de UINT (12)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>FCS</sup> de SNORM (13)
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
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>FCS</sup> SINT (14)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32 PC \_ SIN<sup>TIPO</sup> (15)
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
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a>DXGI_FORMAT_R32G32 FLOAT \_ <sup>FCS</sup> (16)
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
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a>DXGI_FORMAT_R32G32 \_ <sup>FCS</sup> de UINT (17)
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
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a>DXGI_FORMAT_R32G32 \_ <sup>FCS</sup> SINT (18)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r32g8x24_typeless-19"></a>DXGI_FORMAT_R32G8X24 SIN \_ TIPO (19)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_d32_float_s8x24_uint-20"></a>DXGI_FORMAT_D32 FLOAT \_ \_ S8X24 \_ UINT (20)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r32_float_x8x24_typeless-21"></a>DXGI_FORMAT_R32 FLOAT \_ \_ X8X24 \_ SIN TIPO (21)
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
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_x32_typeless_g8x24_uint-22"></a>DXGI_FORMAT_X32 sin \_ TIPO \_ G8X24 \_ UINT (22)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2 \_ PC SIN<sup>TIPO</sup> (23)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a>DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FCS</sup> (24)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a>DXGI_FORMAT_R10G10B10A2 \_ <sup>FCS</sup> de UINT (25)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a>DXGI_FORMAT_R10G10B10 \_ \_ FCS UNORM DE XR BIAS \_ A2 \_ (89)<sup></sup>
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10 FLOAT \_ <sup>FNS</sup> (26)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8 PC \_ SIN<sup>TIPO</sup> (27)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FCS</sup> (28)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ SRGB<sup>FCS</sup> (29)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>FCS</sup> de UINT (30)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>FCS</sup> de SNORM (31)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>FCS</sup> SINT (32)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16 \_ PC SIN<sup>TIPO</sup> (33)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a>DXGI_FORMAT_R16G16 FLOAT \_ <sup>FCS</sup> (34)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a>DXGI_FORMAT_R16G16 \_ UNORM<sup>FCS</sup> (35)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a>DXGI_FORMAT_R16G16 \_ UINT<sup>FCS</sup> (36)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a>DXGI_FORMAT_R16G16 \_ <sup>FCS</sup> de SNORM (37)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a>DXGI_FORMAT_R16G16 \_ SINT<sup>FCS</sup> (38)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32 PC \_ SIN<sup>TIPO</sup> (39)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_d32_floatsupfcssup-40"></a>DXGI_FORMAT_D32 FLOAT \_ <sup>FCS</sup> (40)
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
| Shader ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r32_floatsupfcssup-41"></a>DXGI_FORMAT_R32 FLOAT \_ <sup>FCS</sup> (41)
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
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_r32_uintsupfcssup-42"></a>DXGI_FORMAT_R32 \_ <sup>FCS</sup> de UINT (42)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 32 |
| Compatibilidad con formatos | ![requerido](images/letter-r.jpg) |
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Add | ![requerido](images/letter-r.jpg) |
| Operaciones bit a bit atómicas de UAV | ![requerido](images/letter-r.jpg) |
| UAV Atomic Cmp&Store/Cmp&Exch | ![requerido](images/letter-r.jpg) |
| UAV Atomic Exchange | ![requerido](images/letter-r.jpg) |
| UAV Atomic Signed Min/Max | ![requerido](images/letter-r.jpg) |
| UAV Atomic Unsigned Min/Max | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_r32_sintsupfcssup-43"></a>DXGI_FORMAT_R32 \_ SINT<sup>FCS</sup> (43)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r24g8_typeless-44"></a>DXGI_FORMAT_R24G8 \_ SIN TIPO (44)
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
| Shader ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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
| Recurso en mosaico | \- |

## <a name="dxgi_format_d24_unorm_s8_uint-45"></a>DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT (45)
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
| Shader ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r24_unorm_x8_typeless-46"></a>DXGI_FORMAT_R24 \_ UNORM \_ X8 \_ SIN TIPO (46)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_x24_typeless_g8_uint-47"></a>DXGI_FORMAT_X24 \_ \_ UINT G8 \_ SIN TIPO (47)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8 PC \_ SIN<sup>TIPO</sup> (48)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a>DXGI_FORMAT_R8G8 \_ UNORM<sup>FCS</sup> (49)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a>DXGI_FORMAT_R8G8 \_ <sup>FCS</sup> de UINT (50)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a>DXGI_FORMAT_R8G8 \_ SNORM<sup>FCS</sup> (51)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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
| Carga multimuestreo | ![requerido](images/letter-r.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | ![requerido](images/letter-r.jpg) |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a>DXGI_FORMAT_R8G8 \_ <sup>FCS</sup> SINT (52)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16 \_ PC SIN<sup>TIPO</sup> (53)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_r16_floatsupfcssup-54"></a>DXGI_FORMAT_R16 FLOAT \_ <sup>FCS</sup> (54)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_d16_unormsupfcssup-55"></a>DXGI_FORMAT_D16 \_ <sup>FCS UNORM</sup> (55)
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
| Texture3D | \- |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16_unormsupfcssup-56"></a>DXGI_FORMAT_R16 \_ <sup>FCS UNORM</sup> (56)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_r16_uintsupfcssup-57"></a>DXGI_FORMAT_R16 \_ UINT<sup>FCS</sup> (57)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16_snormsupfcssup-58"></a>DXGI_FORMAT_R16 \_ SNORM<sup>FCS</sup> (58)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r16_sintsupfcssup-59"></a>DXGI_FORMAT_R16 \_ <sup>FCS</sup> sint (59)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8 PC \_ SIN<sup>TIPO</sup> (60)
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
| Shader ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_r8_unormsupfcssup-61"></a>DXGI_FORMAT_R8 \_ UNORM<sup>FCS</sup> (61)
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
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r8_uintsupfcssup-62"></a>DXGI_FORMAT_R8 \_ <sup>FCS</sup> UINT (62)
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
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r8_snormsupfcssup-63"></a>DXGI_FORMAT_R8 \_ <sup>FCS</sup> de SNORM (63)
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
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_r8_sintsupfcssup-64"></a>DXGI_FORMAT_R8 \_ <sup>FCS</sup> sint (64)
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
| Shader ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | \- |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)
| Destino | Soporte técnico |
| - | - |
| Bits por elemento (BPE) | 8 |
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificador de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)
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
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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
| Recurso en mosaico | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8 \_ FNC de \_ UNORM<sup>G8B8</sup> (69)
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
| Texture3D | ![requerido](images/letter-r.jpg) |
| TextureCube | ![requerido](images/letter-r.jpg) |
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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
| Recurso en mosaico | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1 \_ <sup>PCC</sup> SIN TIPO (70)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a>DXGI_FORMAT_BC1 \_ UNORM <sup>FCC</sup> (71)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a>DXGI_FORMAT_BC1 \_ UNORM \_ SRGB <sup>FCC</sup> (72)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2 \_ <sup>PCC</sup> SIN TIPO (73)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a>DXGI_FORMAT_BC2 \_ UNORM <sup>FCC</sup> (74)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a>DXGI_FORMAT_BC2 \_ UNORM \_ SRGB <sup>FCC</sup> (75)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3 \_ <sup>PCC</sup> SIN TIPO (76)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a>DXGI_FORMAT_BC3 \_ UNORM <sup>FCC</sup> (77)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a>DXGI_FORMAT_BC3 \_ UNORM \_ SRGB <sup>FCC</sup> (78)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4 \_ <sup>PCC</sup> SIN TIPO (79)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a>DXGI_FORMAT_BC4 \_ UNORM <sup>FCC</sup> (80)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a>DXGI_FORMAT_BC4 \_ <sup>FCC</sup> de SNORM (81)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5 \_ <sup>PCC</sup> SIN TIPO (82)
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
| Shader ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a>DXGI_FORMAT_BC5 \_ UNORM <sup>FCC</sup> (83)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a>DXGI_FORMAT_BC5 \_ <sup>FCC</sup> de SNORM (84)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5 \_ <sup>FNS de</sup> UNORM (85)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8 PC \_ SIN<sup>TIPO</sup> (90)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FCS</sup> (87)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ SRGB<sup>FCS</sup> (91)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8 PC \_ SIN<sup>TIPO</sup> (92)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FCS</sup> (88)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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
| Entrada del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Salida del procesador de vídeo | ![opcional](images/letter-o.jpg) |
| Recurso compartido | ![requerido](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ SRGB<sup>FCS</sup> (93)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a>DXGI_FORMAT_BC6H \_ <sup>PCC</sup> SIN TIPO (94)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a>DXGI_FORMAT_BC6H \_ UF16 <sup>FCC</sup> (95)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a>DXGI_FORMAT_BC6H \_ SF16 <sup>FCC</sup> (96)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a>DXGI_FORMAT_BC7 \_ <sup>PCC</sup> SIN TIPO (97)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a>DXGI_FORMAT_BC7 \_ UNORM <sup>FCC</sup> (98)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a>DXGI_FORMAT_BC7 \_ UNORM \_ SRGB <sup>FCC</sup> (99)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420 \_ OPAQUE<sup>V</sup> (106)
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
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | \- |
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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

## <a name="dxgi_format_y216supvsup-109"></a>DXGI_FORMAT_Y216<sup>V</sup> (109)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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
| Sombreador ld | ![requerido](images/letter-r.jpg) |
| Ejemplo de sombreador (cualquier filtro) | ![requerido](images/letter-r.jpg) |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_ia44supvsup-112"></a>DXGI_FORMAT_IA44<sup>V</sup> (112)
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
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_p8supvsup-113"></a>DXGI_FORMAT_P8<sup>V</sup> (113)
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
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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
| Sombreador ld | \- |
| Ejemplo de sombreador (cualquier filtro) | \- |
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
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

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a>DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)
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
| Ejemplo de \_ sombreador c (filtro de comparación) | \- |
| Ejemplo de sombreador (filtro mono de 1 \_ \_ bit) | \- |
| Recopilación del sombreador4 | ![requerido](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Add | \- |
| Operaciones bit a bit atómicas de UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU que se puede bloquear | ![requerido](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![opcional](images/letter-o.jpg) |
| Otros recuentos de varios muestreos RT | ![opcional](images/letter-o.jpg) |
| Resolución multimuestreo | ![requerido](images/letter-r.jpg) |
| Carga multimuestreo | ![opcional](images/letter-o.jpg) |
| Mostrar Scan-Out | \- |
| Conversión dentro del diseño de bits | \- |
| Compatibilidad con descodificadores de vídeo | \- |
| Entrada del procesador de vídeo | \- |
| Salida del procesador de vídeo | \- |
| Recurso compartido | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Recurso en mosaico | ![requerido](images/letter-r.jpg) |

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

## <a name="related-topics"></a>Temas relacionados

[Niveles de características de hardware D3D12](../direct3d12/hardware-feature-levels.md)

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)
