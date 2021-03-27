---
title: Sintaxis de anotación (Direct3D 11)
description: Una anotación es una parte de la información definida por el usuario, declarada con la sintaxis descrita en esta sección.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9583dafd3e1fb314ae6ac9e53d609bebc74a030
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995283"
---
# <a name="annotation-syntax-direct3d-11"></a>Sintaxis de anotación (Direct3D 11)

Una anotación es una parte de la información definida por el usuario, declarada con la sintaxis descrita en esta sección.



| <Valor del nombre *DataType*   =  ; *...* ; > |
|----------------------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                   | Descripción                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Tipo*<br/> | \[en \] el tipo de datos, que incluye cualquier tipo de [HLSL escalar](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) , así como el [tipo de cadena](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*<br/>                 | \[en \] una cadena ASCII, que representa el nombre de la anotación.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valor*<br/>             | \[en \] el valor inicial de la anotación.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[en \] anotaciones adicionales (pares nombre-valor).<br/>                                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Puede agregar más de una anotación dentro de los corchetes angulares, cada una separada por un punto y coma. Las API del marco de efecto reconocen las anotaciones en las variables globales; se omiten todas las demás anotaciones.

## <a name="example"></a>Ejemplo

Estos son algunos ejemplos.


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](d3d11-effect-format.md)
</dt> <dt>

[Sintaxis de variables de efectos](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

