---
title: 'Registros: ds_5_0'
description: Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de dominios \_ .
ms.assetid: 8AE00EC6-0BDC-4F63-B95C-FF434B98D7CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b787f4a1f7e647a49340d49796dc2986e442178f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357607"
---
# <a name="registers---ds_5_0"></a>Registros-DS \_ 5 \_ 0

Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de dominios \_ .

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                              | Count                | L/E | Dimensión                           | Indexable por r\# | Valores predeterminados | Requiere DCL |
|------------------------------------------------------------|----------------------|-----|-------------------------------------|------------------|----------|--------------|
| 32-bit Temp (r \# )                                          | 4096 (r \# + x \# \[ n \] )   | L/E | 4                                   | No               | None     | Sí          |
| Matriz temporal Indizable de 32 bits (x \# \[ n \] )                     | 4096 (r \# + x \# \[ n \] )   | L/E | 4                                   | Sí              | None     | Sí          |
| Puntos de control de entrada de 32 bits ( \[ elemento de vértice VCP \] \[ \] )     | 32 vea la nota 1 a continuación. | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Sí              | None     | Sí          |
| Constantes de revisión de entrada de 32 bits ( \[ vértice de VPC \] )               | 32 vea la nota 2 a continuación. | R   | 4                                   | Sí              | None     | Sí          |
| Ubicación de entrada de 32 bits en el dominio (vDomain. XY, vDomain.xyz)) | 1                    | R   | 3                                   | No               | N/D      | Sí          |
| PrimitiveID de entrada UINT de 32 bits (vPrim)                      | 1                    | R   | 1                                   | No               | N/D      | Sí          |
| Elemento de un recurso de entrada (t \# )                         | 128                  | R   | 128                                 | Sí              | None     | Sí          |
| Muestras (s \# )                                              | 16                   | R   | 1                                   | Sí              | None     | Sí          |
| referencia de iConstantBuffer ( \# \[ Índice CB \] )                  | 15                   | R   | 4                                   | Sí              | None     | Sí          |
| referencia de ConstantBuffer de iImmediate (índice de ICB \[ \] )         | 1                    | R   | 4                                   | Sí (contenido)    | Ninguno     | Sí          |



 

**Nota 1:** El sombreador de dominios ve las salidas del sombreador de casco en dos conjuntos independientes de registros. Los registros VCP pueden ver todos los puntos de control de salida del sombreador de casco. Los registros de VPC pueden ver todos los datos de salida constantes de la revisión del sombreador de casco.

**Nota 2:** Dado que el código para las fases de bifurcación de la bifurcación o las fases de combinación de la corrección del sombreador de Casco genera TessFactors con nombres como VP \_ TessFactor, el sombreador de dominios debe coincidir con esas declaraciones en la entrada de VPC equivalente si desea ver esos valores.

## <a name="output-registers"></a>Registros de salida



| Tipo de registro                           | Count | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Elemento de datos de vértice de salida de 32 bits (o \# ) | 32    | W   | 4         | Sí              | None     | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




