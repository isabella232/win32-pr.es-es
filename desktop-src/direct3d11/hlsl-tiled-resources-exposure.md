---
title: Exposición de recursos en mosaico hlsl
description: Se requiere una nueva sintaxis de Lenguaje de sombreador de alto nivel (HLSL) de Microsoft para admitir recursos en mosaico en el modelo 5 de sombreador.
ms.assetid: B6CE51E6-1BA9-4D15-9654-86FE9BAAF585
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66ded502bebefc1061028115a12026f67c26cad89ddc57f98a5ae6fee923591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633335"
---
# <a name="hlsl-tiled-resources-exposure"></a>Exposición de recursos en mosaico hlsl

Se requiere una nueva sintaxis de Lenguaje de sombreador de alto nivel (HLSL) de Microsoft para admitir recursos en mosaico en [el modelo de sombreador 5.](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)

La nueva sintaxis HLSL solo se permite en dispositivos con compatibilidad con recursos en mosaico. Cada método HLSL pertinente para los recursos en mosaico de la tabla siguiente acepta uno (comentarios) o dos (fijación y comentarios en este orden) parámetros opcionales adicionales. Por ejemplo, un **método sample** es:

**Sample(sampler, location \[ , offset , clamp , feedback \[ \[ \] \] \] )**

Un ejemplo de un **método Sample** [**es Texture2D.Sample(S,float,int,float,uint).**](/windows/desktop/direct3dhlsl/t2darray-sample-s-float-int-float-uint-)

Los parámetros offset, clamp y feedback son opcionales. Debe especificar todos los parámetros opcionales hasta el que necesite, que es coherente con las reglas de C++ para los argumentos de función predeterminados. Por ejemplo, si se necesita el estado de los comentarios, los parámetros de desplazamiento y de fijación deben proporcionarse explícitamente a **Sample**, aunque es posible que no sean necesarios lógicamente.

El parámetro de fijación es un valor float escalar. El valor literal de clamp=0.0f indica que no se realiza la operación de fijación.

El parámetro feedback es una variable **uint** que puede proporcionar a la función [**intrínseca CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) de consulta de acceso a memoria. No debe modificar ni interpretar el valor del parámetro de comentarios; pero el compilador no proporciona ningún análisis y diagnóstico avanzados para detectar si ha modificado el valor.

Esta es la sintaxis [**de CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped):

**bool CheckAccessFullyMapped(in uint FeedbackVar);**

[**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpreta el valor de *FeedbackVar* y devuelve true si todos los datos a los que se accede se asignaron en el recurso; De lo contrario, **CheckAccessFullyMapped** devuelve false.

Si la fijación o el parámetro de comentarios están presentes, el compilador emite una variante de la instrucción básica. Por ejemplo, el ejemplo de un recurso en mosaico genera la `sample_cl_s` instrucción . Si no se especifica ninguna fijación ni comentarios, el compilador emite la instrucción básica, de modo que no haya ningún cambio con respecto al comportamiento actual. El valor de la fijación de 0,0f indica que no se realiza ninguna fijación; por lo tanto, el compilador del controlador puede adaptar aún más la instrucción al hardware de destino. Si los comentarios son un registro NULL en una instrucción, los comentarios no se usan; por lo tanto, el compilador del controlador puede adaptar aún más la instrucción a la arquitectura de destino.

Si el compilador HLSL deduce que la fijación es 0,0f y los comentarios no se usan, el compilador emite la instrucción básica correspondiente (por ejemplo, en lugar de `sample` `sample_cl_s` ).

Si un acceso a recursos en mosaico consta de varias instrucciones de código de bytes constituyentes, por ejemplo, para recursos estructurados, el compilador agrega valores de comentarios individuales a través de la operación OR para generar el valor de comentarios final. Por lo tanto, verá un único valor de comentarios para un acceso tan complejo.

Esta es la tabla de resumen de los métodos HLSL que se cambian para admitir comentarios o fijaciones. Todos funcionan en recursos en mosaico y no en mosaico de todas las dimensiones. Los recursos que no están en mosaico siempre parecen estar totalmente asignados.



| [Objetos HLSL](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5-objects)                                                                                                                                                                                                                                | Métodos intrínsecos con la opción de comentarios ( \* ) : también tiene la opción de fijación                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[RW \] Texture2D<br/> \[RW \] Texture2DArray<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                                                                                                                    | Reunir<br/> GatherRed<br/> GatherGreen<br/> GatherBlue<br/> GatherAlpha<br/> GatherCmp<br/> GatherCmpRed<br/> GatherCmpGreen<br/> GatherCmpBlue<br/> GatherCmpAlpha<br/> |
| \[RW \] Texture1D<br/> \[RW \] Texture1DArray<br/> \[RW \] Texture2D<br/> \[RW \] Texture2DArray<br/> \[RW \] Texture3D<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                              | Muestra\*<br/> SampleBias\*<br/> SampleCmp\*<br/> SampleCmpLevelZero<br/> SampleGrad\*<br/> SampleLevel<br/>                                                                                      |
| \[RW \] Texture1D<br/> \[RW \] Texture1DArray<br/> \[RW \] Texture2D<br/> Texture2DMS<br/> \[RW \] Texture2DArray<br/> Texture2DArrayMS<br/> \[RW \] Texture3D<br/> \[Búfer \] RW<br/> \[RW \] ByteAddressBuffer<br/> \[RW \] StructuredBuffer<br/> | Cargar                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

