---
description: Método implementado por el usuario para cerrar un archivo de inclusión de sombreador \# .
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'ID3DXInclude:: Close (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b60d01d59a4e54fa0d50c16a3fc845ea4e316792
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698395"
---
# <a name="id3dxincludeclose-method"></a>ID3DXInclude:: Close (método)

Método implementado por el usuario para cerrar un archivo de inclusión de sombreador \# .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdata* \[ de\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al búfer devuelto que contiene las directivas Include. Este es el puntero devuelto por la llamada a [**ID3DXInclude:: Open**](id3dxinclude--open.md) correspondiente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ correcto. Si se produce un error en la devolución de llamada al leer el \# archivo de inclusión, se producirá un error en la API que provocó la llamada de devolución de llamada. Es uno de los siguientes:

-   El sombreador HLSL producirá un error en una de las funciones de D3DXCompileShader \* \* \* .
-   El sombreador de ensamblado producirá un error en una de las funciones de D3DXAssembleShader \* \* \* .
-   El efecto producirá un error en una de las \* \* \* funciones D3DXCreateEffect o D3DXCreateEffectCompiler \* \* \* .

## <a name="remarks"></a>Observaciones

Si [**ID3DXInclude:: Open**](id3dxinclude--open.md) se ejecutó correctamente, se garantiza que se llamará a **ID3DXInclude:: Close** antes de que la API que usa esta interfaz devuelva.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude:: Open**](id3dxinclude--open.md)
</dt> </dl>

 

 
