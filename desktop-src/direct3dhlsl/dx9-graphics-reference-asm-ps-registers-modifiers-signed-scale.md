---
title: Escala de registro de origen firmada
description: Resta 0,5 de cada canal y escala el resultado en 2,0. El nombre BX2 proviene de Bias y Scale-Times-Two, que es la operación que realiza.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269464"
---
# <a name="source-register-signed-scaling"></a>Escala de registro de origen firmada

Resta 0,5 de cada canal y escala el resultado en 2,0. El nombre BX2 proviene de Bias y Scale-Times-Two, que es la operación que realiza.

## <a name="syntax"></a>Sintaxis


```
source register_bx2
```



## <a name="register"></a>Registrarse

Registro de origen. Para obtener más información sobre los tipos de registro, vea [PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Observaciones

Esta operación se utiliza normalmente para expandir los datos de \[ 0,0 a 1,0 a \] \[ -1,0 a 1,0 \] . Este modificador está diseñado para su uso con las instrucciones aritméticas. Este modificador se usa normalmente en las entradas de la instrucción de producto DOT ([DP3-PS](dp3---ps.md)). \_El uso de BX2 en los datos que están fuera del intervalo de 0 a 1 puede producir resultados indefinidos.

La operación de escalado firmada se aplica a los datos leídos del registro antes de que se ejecute la siguiente instrucción. La operación se aplica a los cuatro canales de color (RGBA) de la siguiente manera:


```
y = 2(x - 0.5)
```



No se cambia el contenido del registro. El modificador se aplica solo a los datos leídos del registro.

Este modificador es mutuamente excluyente con la [inversión del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) , por lo que no se puede aplicar al mismo registro.

Información de versión:

-   Para PS \_ 1 \_ 0 y PS \_ 1 \_ 1, puede usar \_ BX2 en cualquier registro de origen para obtener instrucciones de textura con la forma texm3x2 \* y texm3x3 \* . \_BX2 no se puede usar en ninguna de las otras instrucciones de textura como [texreg2ar-PS](texreg2ar---ps.md) o [texreg2gb-PS](texreg2gb---ps.md).
-   Para PS \_ 1 \_ 2 y PS \_ 1 \_ 3, puede usar \_ BX2 en cualquier registro de origen para cualquier instrucción Tex, \* excepto: [texreg2ar-PS](texreg2ar---ps.md), [texreg2gb-PS](texreg2gb---ps.md), [texbem-PS](texbem---ps.md) o [texbeml-PS](texbeml---ps.md).

## <a name="example"></a>Ejemplo

En este ejemplo se muestrea una textura, se convierten los datos en el intervalo de-1 a + 1 y se calcula un producto de punto.


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




