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
ms.openlocfilehash: 2b378cd97bc9779951d62873d393009c98d32823
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573757"
---
# <a name="register"></a>registro

Palabra clave opcional para asignar una variable de sombreador a un registro determinado, que usa la sintaxis siguiente:



| : register ( *\[ perfil de \_ sombreador \]*, *tipo \# \[ subcomponente \]* ) |
|----------------------------------------------------------------|



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="register"></span><span id="REGISTER"></span>Registro
</dt> <dd>

Palabra clave Required.

</dd> <dt>

<span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[perfil de \_ sombreador\]*
</dt> <dd>

Perfil [de sombreador opcional,](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)que puede ser un destino de sombreador o simplemente **ps** o **vs**.

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

## <a name="remarks"></a>Observaciones

Puede agregar una o varias asignaciones de registro a la misma declaración de variable, separadas por espacios.

Para las variables de Direct3D 10 en el ámbito global, la palabra clave **register** actúa igual que la palabra clave [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)

## <a name="examples"></a>Ejemplos

A continuación se muestran algunos ejemplos:


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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis de variables](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variables (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 