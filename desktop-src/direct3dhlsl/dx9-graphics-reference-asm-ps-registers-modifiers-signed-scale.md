---
title: Escalado firmado del registro de origen
description: Resta 0,5 de cada canal y escala el resultado en 2,0. El nombre bx2 procede del sesgo y el escalado de dos veces, que es la operación que realiza.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360795"
---
# <a name="source-register-signed-scaling"></a>Escalado firmado del registro de origen

Resta 0,5 de cada canal y escala el resultado en 2,0. El nombre bx2 procede del sesgo y el escalado de dos veces, que es la operación que realiza.

## <a name="syntax"></a>Sintaxis


```
source register_bx2
```



## <a name="register"></a>Registrarse

Registro de origen. Para obtener más información sobre los tipos de registro, [vea ps \_ \_ 1 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Observaciones

Esta operación se usa normalmente para expandir los datos de \[ 0.0 a 1.0 a \] \[ -1.0 a 1.0. \] Este modificador está diseñado para usarse con las instrucciones aritméticas. Este modificador se usa normalmente en las entradas de la instrucción de producto de punto ([dp3 - ps](dp3---ps.md)). El \_ uso de bx2 en datos fuera del intervalo 0 a 1 puede producir resultados no definidos.

La operación de escalado firmada se aplica a los datos leídos del registro antes de ejecutar la siguiente instrucción. La operación se aplica a los cuatro canales de color (RGBA) como se muestra a continuación:


```
y = 2(x - 0.5)
```



No se cambia el contenido del registro. El modificador solo se aplica a los datos leídos del registro.

Este modificador es mutuamente excluyente con [Source Register Invert,](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) por lo que no se puede aplicar al mismo registro.

Información de versión:

-   Para ps 1 0 y ps 1 1, puede usar bx2 en cualquier registro de origen para obtener instrucciones de textura con el formato \_ \_ \_ \_ \_ texm3x2 y \* texm3x3 \* . \_bx2 no se puede usar en ninguna de las otras instrucciones de textura, como [texreg2ar - ps](texreg2ar---ps.md) o [texreg2gb - ps](texreg2gb---ps.md).
-   Para ps 1 2 y ps 1 3, puede usar bx2 en cualquier registro de origen para cualquier instrucción \_ \_ de \_ \_ \_ texas, \* excepto: [texreg2ar - ps](texreg2ar---ps.md), [texreg2gb - ps](texreg2gb---ps.md), [texbem - ps](texbem---ps.md) o [texbeml - ps](texbeml---ps.md).

## <a name="example"></a>Ejemplo

En este ejemplo se muestrea una textura, se convierten los datos en el intervalo de -1 a +1 y se calcula un producto de punto.


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




