---
description: Una anotación es un fragmento de información definido por el usuario, declarado con la sintaxis siguiente.
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: Sintaxis de anotación (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303065e9c49c380a5accba6faadbc641ec0f528a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063810"
---
# <a name="annotation-syntax-direct3d-10"></a>Sintaxis de anotación (Direct3D 10)

Una anotación es un fragmento de información definido por el usuario, declarado con la sintaxis siguiente.



| <*DataType* *Name*  =  *Value*; ... ; > |
|--------------------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                   | Descripción                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Datatype*<br/> | \[en \] El tipo de datos , que incluye cualquier tipo [HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) escalar, así como el tipo [de cadena](../direct3dhlsl/dx-graphics-hlsl-scalar.md).<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nombre*<br/>                 | \[en \] Una cadena ASCII, que representa el nombre de la anotación.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valor*<br/>             | \[en \] El valor inicial de la anotación.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[en \] Anotaciones adicionales (pares nombre-valor).<br/>                                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Puede agregar más de una anotación entre corchetes angulares, cada una separada por un punto y coma. Las API del marco de efecto reconocen anotaciones en variables globales. todas las demás anotaciones se omiten.

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

[Sintaxis de variable de efecto](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
