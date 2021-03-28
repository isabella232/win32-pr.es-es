---
title: registro
description: registro
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- registro de HLSL
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
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420744"
---
# <a name="register"></a>registro

Palabra clave opcional para asignar una variable de sombreador a un registro determinado, que usa la sintaxis siguiente:



| : Register ( *\[ \_ perfil \] de sombreador*, * \# \[ subcomponente \] de tipo* ) |
|----------------------------------------------------------------|



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="register"></span><span id="REGISTER"></span>el
</dt> <dd>

Palabra clave required.

</dd> <dt>

<span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[Perfil de sombreador \_\]*
</dt> <dd>

[Perfil de sombreador](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)opcional, que puede ser un destino de sombreador o simplemente **PS** o **vs**.

</dd> <dt>

<span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Subcomponente de tipo \# \[\]*
</dt> <dd>

Registra el tipo, el número y la declaración del subcomponente.

-   El tipo es uno de los siguientes:

    

    | Tipo | Descripción del registro       |
    |------|----------------------------|
    | b    | Búfer de constantes            |
    | t    | Búfer de textura y textura |
    | c    | Desplazamiento de búfer              |
    | s    | Muestra                    |
    | u    | Vista de acceso desordenado      |

    

     

-   *\#* es el número de registro, que es un número entero.
-   El *subcomponente* es un número entero opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede Agregar una o varias asignaciones de registro a la misma declaración de variable, separadas por espacios.

En el caso de las variables de Direct3D 10 en el ámbito global, la palabra clave **Register** actúa igual que la palabra clave [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de variables](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variables (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 