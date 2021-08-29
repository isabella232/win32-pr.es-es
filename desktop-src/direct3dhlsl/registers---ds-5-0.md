---
title: 'Registros: ds_5_0'
description: Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de \_ dominios.
ms.assetid: 8AE00EC6-0BDC-4F63-B95C-FF434B98D7CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5bd34609ef289a0cf6671c21e21d219c4b8b19ea392e5f3103b6267ffaea58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672195"
---
# <a name="registers---ds_5_0"></a>Registros: ds \_ 5 \_ 0

Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de \_ dominios.

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                              | Count                | L/E | Dimensión                           | Indexable by r\# | Valores predeterminados | Requiere DCL |
|------------------------------------------------------------|----------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                          | 4096(r \# +x \# \[ n \] )   | L/E | 4                                   | No               | None     | Sí          |
| Matriz temporal indexable de 32 bits (x \# \[ n \] )                     | 4096(r \# +x \# \[ n \] )   | L/E | 4                                   | Sí              | None     | Sí          |
| Puntos de control de entrada de 32 bits (elemento de \[ vértice \] \[ \] vcp)     | 32 Vea la nota 1 a continuación. | R   | 4(component) \* 32(element) \* 32(vert) | Sí              | None     | Sí          |
| Constantes de revisión de entrada de 32 bits (vértice \[ de \] vpc)               | 32 Vea la nota 2 a continuación. | R   | 4                                   | Sí              | None     | Sí          |
| Ubicación de entrada de 32 bits en el dominio (vDomain.xy, vDomain.xyz)) | 1                    | R   | 3                                   | No               | N/D      | Sí          |
| PrimitiveID de entrada UINT de 32 bits (vPrim)                      | 1                    | R   | 1                                   | No               | N/D      | Sí          |
| Elemento de un recurso de entrada (t \# )                         | 128                  | R   | 128                                 | Sí              | None     | Sí          |
| Sampler (s \# )                                              | 16                   | R   | 1                                   | Sí              | None     | Sí          |
| Referencia de iConstantBuffer (índice \# \[ \] cb)                  | 15                   | R   | 4                                   | Sí              | None     | Sí          |
| Referencia de ConstantBuffer de iImmediate (índice \[ \] icb)         | 1                    | R   | 4                                   | Sí (contenido)    | Ninguno     | Sí          |



 

**Nota 1:** El sombreador de dominio ve las salidas del sombreador de casco en dos conjuntos de registros independientes. Los registros de vcp pueden ver todos los puntos de control de salida del sombreador de casco. Los registros de vpc pueden ver todos los datos de salida de patch constant del sombreador de casco.

**Nota 2:** Dado que el código de las fases de bifurcación constante de revisión o combinación del sombreador de casco genera TessFactors mediante nombres como SV TessFactor, el sombreador de dominio debe coincidir con esas declaraciones en la entrada de Laco equivalente si desea ver \_ esos valores.

## <a name="output-registers"></a>Registros de salida



| Tipo de registro                           | Count | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Elemento de datos vertex de salida de 32 bits (o \# ) | 32    | W   | 4         | Sí              | None     | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




