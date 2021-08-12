---
title: Sintaxis de anotación (Direct3D 11)
description: Una anotación es un fragmento de información definido por el usuario, declarado con la sintaxis descrita en esta sección.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1109695f6239708e8f241b796b888b8d494acd7ab806b98c08352dbe3aeaee3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538569"
---
# <a name="annotation-syntax-direct3d-11"></a>Sintaxis de anotación (Direct3D 11)

Una anotación es un fragmento de información definido por el usuario, declarado con la sintaxis descrita en esta sección.



| <*Valor de nombre* *de tipo* de  =  *datos*; *...* ;> |
|----------------------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                   | Descripción                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Datatype*<br/> | \[en \] El tipo de datos , que incluye cualquier tipo [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) escalar, así como el tipo [de cadena](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nombre*<br/>                 | \[en \] Una cadena ASCII, que representa el nombre de la anotación.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valor*<br/>             | \[en \] El valor inicial de la anotación.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[en \] Anotaciones adicionales (pares nombre-valor).<br/>                                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Puede agregar más de una anotación entre corchetes angulares, cada una separada por un punto y coma. Las API del marco de trabajo de efecto reconocen anotaciones en variables globales; todas las demás anotaciones se omiten.

## <a name="example"></a>Ejemplo

A continuación se muestran algunos ejemplos.


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

[Sintaxis de variable de efecto](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

