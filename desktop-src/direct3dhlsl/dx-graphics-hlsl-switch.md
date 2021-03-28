---
title: Switch (instrucción) (urlmon. h)
description: Transfiere el control a un bloque de instrucciones diferente en el cuerpo del modificador en función del valor de un selector.
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- Instrucción switch HLSL
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
ms.openlocfilehash: 4c65049acce4265dd2abdf849119aad5902db9e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820919"
---
# <a name="switch-statement"></a>switch (Instrucción)

Transfiere el control a un bloque de instrucciones diferente en el cuerpo del modificador en función del valor de un selector.



|                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[*Atributo* \] de Switch ( *selector* ) {Case 0: { *StatementBlock*;}   eliminar   caso 1: { *StatementBlock*;}   eliminar   Case n: { *StatementBlock*;}   eliminar   valor predeterminado: { *StatementBlock*;}   eliminar |



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atribui*
</dt> <dd>

Parámetro opcional que controla cómo se compila la instrucción. Cuando no se especifica ningún atributo, el compilador puede usar un modificador de hardware o emitir una serie de instrucciones **If** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>quitar información de estructura jerárquica</td>
<td>Compile la instrucción como una serie de instrucciones <strong>If</strong> , cada una con el atributo <strong>Flatten</strong> .</td>
</tr>
<tr class="even">
<td>branch</td>
<td>Compile la instrucción como una serie de instrucciones <strong>If</strong> cada una con el atributo <strong>Branch</strong> .
<blockquote>
[!Note]<br />
Al usar el modelo de <a href="dx-graphics-hlsl-sm2.md">sombreador 2. x</a> o el <a href="dx-graphics-hlsl-sm3.md">modelo de sombreador 3,0</a>, cada vez que se usa la bifurcación dinámica, se consumen recursos. Por lo tanto, si utiliza la bifurcación dinámica de forma excesiva cuando tiene como destino estos perfiles, puede recibir errores de compilación.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>forcecase</td>
<td>Fuerce una instrucción switch en el hardware.
<blockquote>
[!Note]<br />
Requiere 10_0 de <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">nivel de característica</a> o hardware posterior.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>llamada</td>
<td>Los cuerpos de los casos individuales del conmutador se moverán a subrutinas de hardware y el modificador será una serie de llamadas subrutinas.
<blockquote>
[!Note]<br />
Requiere 10_0 de <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">nivel de característica</a> o hardware posterior.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Situado*
</dt> <dd>

Una variable. Las instrucciones Case dentro de los corchetes comprueban esta variable para ver si el SwitchValue coincide con su CaseValue determinado.

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

Una o más [instrucciones](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones


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



Es equivalente a:


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



Estos son los usos de ejemplo de forcecase y los atributos de control de flujo de llamadas:


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
| Encabezado<br/> | <dl> <dt>Urlmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de flujo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

