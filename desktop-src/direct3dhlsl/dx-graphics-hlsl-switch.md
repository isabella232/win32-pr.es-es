---
title: switch (Instrucción) (Urlmon.h)
description: Transfiera el control a un bloque de instrucciones diferente dentro del cuerpo del conmutador en función del valor de un selector.
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- switch (Instrucción HLSL)
topic_type:
- apiref
api_name:
- switch Statement
api_location:
- urlmon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8527853bf88b073f3505f4b4170ff6165f7f9aa7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477491"
---
# <a name="switch-statement"></a>switch (Instrucción)

Transfiera el control a un bloque de instrucciones diferente dentro del cuerpo del conmutador en función del valor de un selector.


\[*Atributo* \] switch( *Selector* ) { case 0 : { *StatementBlock*; }   break;   caso 1: { *StatementBlock*; }   break;   case n : { *StatementBlock*; }   break;   default : { *StatementBlock*; }   break;



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*
</dt> <dd>

Parámetro opcional que controla cómo se compila la instrucción. Cuando no se especifica ningún atributo, el compilador puede usar un conmutador de hardware o emitir una serie de **instrucciones if.**




| Atributo | Descripción | 
|-----------|-------------|
| quitar información de estructura jerárquica | Compile la instrucción como una serie de <strong>instrucciones if,</strong> cada una con el <strong>atributo flatten.</strong> | 
| branch | Compile la instrucción como una serie de <strong>instrucciones if</strong> cada una con el <strong>atributo branch.</strong><blockquote>[!Note]<br />Cuando se usa <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> o <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, cada vez que se usa la bifurcación dinámica se consumen recursos. Por lo tanto, si usa la bifurcación dinámica excesivamente cuando tiene como destino estos perfiles, puede recibir errores de compilación.</blockquote><br /> | 
| forcecase | Forzar una instrucción switch en el hardware.<blockquote>[!Note]<br />Requiere <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">hardware de nivel</a> de característica 10_0 o posterior.</blockquote><br /> | 
| llamada | Los cuerpos de los casos individuales del conmutador se trasladarán a subrutinas de hardware y el modificador será una serie de llamadas de subrutina.<blockquote>[!Note]<br />Requiere <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">hardware de nivel</a> de característica 10_0 o posterior.</blockquote><br /> | 




 

</dd> <dt>

<span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*
</dt> <dd>

Variable. Las instrucciones case dentro de los corchetes comprobarán cada una esta variable para ver si SwitchValue coincide con su caseValue determinado.

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

Una o varias [instrucciones](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios


```
[branch] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



Equivale a:


```
[branch] if( a == 2 )
    return 3;
else if( a == 1 )
    return 1;
else if( a == 0 )
    return 0;
else
    return 6;
```



Estos son ejemplos de usos de atributos de control de flujo de llamada y de mayúsculas y minúsculas:


```
[forcecase] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}

[call] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Urlmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Flow Control](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

