---
title: registro
description: registro
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- registrar HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0102716529471b3e867e17b0e9b635274cdfc28ec603f239d66c76ffb0fdaa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983215"
---
# <a name="register"></a>registro

Palabra clave opcional para asignar una variable de sombreador a un registro determinado, que usa la sintaxis siguiente:



| : register ( *\[ shader \_ profile \]*, *Type \# \[ subcomponent \]* ) |
|----------------------------------------------------------------|



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="register"></span><span id="REGISTER"></span>Registro
</dt> <dd>

Palabra clave required.

</dd> <dt>

<span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[perfil de \_ sombreador\]*
</dt> <dd>

Perfil [de sombreador opcional,](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)que puede ser un destino de sombreador o simplemente **ps** o **vs.**

</dd> <dt>

<span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*\# \[ Subcomponente de tipo\]*
</dt> <dd>

Registre la declaración de tipo, número y subcomponente.

-   El tipo es uno de los siguientes:

    

    | Tipo | Descripción del registro       |
    |------|----------------------------|
    | b    | Búfer constante            |
    | t    | Búfer de textura y textura |
    | c    | Desplazamiento del búfer              |
    | s    | Muestra                    |
    | u    | Vista de acceso desordenado      |

    

     

-   *\#* es el número de registro, que es un número entero.
-   El *subcomponente* es un número entero opcional.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puede agregar una o varias asignaciones de registro a la misma declaración de variable, separadas por espacios.

En el caso de las variables de Direct3D 10 en el ámbito global, la palabra clave **register** actúa igual que la palabra clave [packoffset (HlSL de DirectX).](dx-graphics-hlsl-variable-packoffset.md)

## <a name="examples"></a>Ejemplos

Estos son algunos ejemplos:


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de variables](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variables (HLSL de DirectX)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 