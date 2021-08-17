---
title: Interfaz ID3DX11EffectScalarVariable (D3dx11effect.h)
description: Una interfaz effect-scalar-variable tiene acceso a valores escalares.
ms.assetid: 52e3b856-aa1b-4ed2-b140-7ae96ec1c94b
keywords:
- Interfaz ID3DX11EffectScalarVariable direct3D 11
- Interfaz ID3DX11EffectScalarVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a33445045d463591659902a4d599deddb3b33f092ef646df736d72db501fde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408155"
---
# <a name="id3dx11effectscalarvariable-interface"></a>Interfaz ID3DX11EffectScalarVariable

Una interfaz effect-scalar-variable tiene acceso a valores escalares.

## <a name="members"></a>Miembros

La **interfaz ID3DX11EffectScalarVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectScalarVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectScalarVariable** tiene estos métodos.



| Método                                                             | Descripción                                          |
|:-------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBool**](id3dx11effectscalarvariable-getbool.md)             | Obtiene una variable booleana.<br/>                   |
| [**GetBoolArray**](id3dx11effectscalarvariable-getboolarray.md)   | Obtiene una matriz de variables booleanas.<br/>        |
| [**GetFloat**](id3dx11effectscalarvariable-getfloat.md)           | Obtiene una variable de punto flotante.<br/>            |
| [**GetFloatArray**](id3dx11effectscalarvariable-getfloatarray.md) | Obtiene una matriz de variables de punto flotante.<br/> |
| [**GetInt**](id3dx11effectscalarvariable-getint.md)               | Obtiene una variable de entero.<br/>                  |
| [**GetIntArray**](id3dx11effectscalarvariable-getintarray.md)     | Obtiene una matriz de variables de enteros.<br/>        |
| [**SetBool**](id3dx11effectscalarvariable-setbool.md)             | Establezca una variable booleana.<br/>                   |
| [**SetBoolArray**](id3dx11effectscalarvariable-setboolarray.md)   | Establezca una matriz de variables booleanas.<br/>        |
| [**SetFloat**](id3dx11effectscalarvariable-setfloat.md)           | Establezca una variable de punto flotante.<br/>            |
| [**SetFloatArray**](id3dx11effectscalarvariable-setfloatarray.md) | Establezca una matriz de variables de punto flotante.<br/> |
| [**SetInt**](id3dx11effectscalarvariable-setint.md)               | Establezca una variable de entero.<br/>                  |
| [**SetIntArray**](id3dx11effectscalarvariable-setintarray.md)     | Establezca una matriz de variables de enteros.<br/>        |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Efectos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





