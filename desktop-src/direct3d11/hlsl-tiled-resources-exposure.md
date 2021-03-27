---
title: Exposición de recursos en mosaico de HLSL
description: Se requiere una nueva sintaxis de lenguaje de sombreado de alto nivel (HLSL) de Microsoft para admitir recursos en mosaico en el modelo de sombreador 5.
ms.assetid: B6CE51E6-1BA9-4D15-9654-86FE9BAAF585
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b266b98045b38645e1e8d24ed0014a5f448a38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487963"
---
# <a name="hlsl-tiled-resources-exposure"></a>Exposición de recursos en mosaico de HLSL

Se requiere una nueva sintaxis de lenguaje de sombreado de alto nivel (HLSL) de Microsoft para admitir recursos en mosaico en el [modelo de sombreador 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).

La nueva sintaxis de HLSL solo se permite en dispositivos con compatibilidad con recursos en mosaico. Cada método HLSL relevante para los recursos en mosaico en la tabla siguiente acepta uno (comentarios) o dos (abrazadera y comentarios en este orden) parámetros opcionales adicionales. Por ejemplo, un método de **ejemplo** es:

**Ejemplo (muestra, ubicación \[ , desplazamiento \[ , abrazadera \[ , comentarios \] \] \] )**

Un ejemplo de método de **ejemplo** es [**Texture2D. sample (S, Float, int, Float, uint)**](/windows/desktop/direct3dhlsl/t2darray-sample-s-float-int-float-uint-).

Los parámetros offset, Clamp y feedback son opcionales. Debe especificar todos los parámetros opcionales hasta el que necesite, lo que es coherente con las reglas de C++ de los argumentos de función predeterminados. Por ejemplo, si se necesita el estado de los comentarios, los parámetros offset y Clamp deben proporcionarse explícitamente al **ejemplo**, aunque es posible que no sean necesarios lógicamente.

El parámetro Clamp es un valor Float escalar. El valor literal de Clamp = 0.0 f indica que no se realiza la operación de abrazadera.

El parámetro feedback es una variable **uint** que se puede proporcionar a la función [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) intrínseca de consulta de acceso a la memoria. No debe modificar ni interpretar el valor del parámetro feedback. pero el compilador no proporciona ningún diagnóstico y análisis avanzados para detectar si modificó el valor.

Esta es la sintaxis de [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped):

**bool CheckAccessFullyMapped (en uint FeedbackVar);**

[**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpreta el valor de *FeedbackVar* y devuelve true si todos los datos a los que se tiene acceso se asignaron en el recurso; de lo contrario, **CheckAccessFullyMapped** devuelve false.

Si el parámetro clamp o feedback está presente, el compilador emite una variante de la instrucción básica. Por ejemplo, el ejemplo de un recurso en mosaico genera la `sample_cl_s` instrucción. Si no se especifican Clamp ni feedback, el compilador emite la instrucción básica, de modo que no hay ningún cambio en el comportamiento actual. El valor de Clamp de 0,0 f indica que no se realiza ninguna abrazadera; por lo tanto, el compilador de controladores puede personalizar aún más la instrucción al hardware de destino. Si los comentarios son un registro nulo en una instrucción, los comentarios no se usan. por lo tanto, el compilador de controladores puede adaptar aún más la instrucción a la arquitectura de destino.

Si el compilador de HLSL infiere que la abrazadera es 0,0 f y los comentarios no se usan, el compilador emite la instrucción básica correspondiente (por ejemplo, `sample` en lugar de `sample_cl_s` ).

Si el acceso a un recurso en mosaico consta de varias instrucciones de código de bytes constituyentes, por ejemplo, para los recursos estructurados, el compilador agrega valores de comentarios individuales a través de la operación o para generar el valor final de los comentarios. Por lo tanto, verá un valor de comentarios único para este tipo de acceso complejo.

Esta es la tabla de Resumen de los métodos de HLSL que se cambian para admitir comentarios y/o abrazadera. Todas ellas funcionan en recursos en mosaico y no en mosaico de todas las dimensiones. Los recursos no mosaicos siempre parecen estar totalmente asignados.



| [Objetos HLSL](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5-objects)                                                                                                                                                                                                                                | Métodos intrínsecos con la opción feedback ( \* )-también tiene la opción Clamp                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[RW \] Texture2D<br/> \[RW \] Texture2DArray<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                                                                                                                    | Recopilar<br/> GatherRed<br/> GatherGreen<br/> GatherBlue<br/> GatherAlpha<br/> GatherCmp<br/> GatherCmpRed<br/> GatherCmpGreen<br/> GatherCmpBlue<br/> GatherCmpAlpha<br/> |
| \[RW \] Texture1D<br/> \[RW \] Texture1DArray<br/> \[RW \] Texture2D<br/> \[RW \] Texture2DArray<br/> \[RW \] Texture3D<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                              | Ejemplo\*<br/> SampleBias\*<br/> SampleCmp\*<br/> SampleCmpLevelZero<br/> SampleGrad\*<br/> SampleLevel<br/>                                                                                      |
| \[RW \] Texture1D<br/> \[RW \] Texture1DArray<br/> \[RW \] Texture2D<br/> Texture2DMS<br/> \[RW \] Texture2DArray<br/> Texture2DArrayMS<br/> \[RW \] Texture3D<br/> \[Búfer de RW \]<br/> \[RW \] ByteAddressBuffer<br/> \[RW \] StructuredBuffer<br/> | Carga                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

