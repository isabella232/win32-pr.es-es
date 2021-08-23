---
description: Método implementado por el usuario para cerrar un archivo de incluir \# sombreador.
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: Método ID3DXInclude::Close (D3DX9Shader.h)
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
ms.openlocfilehash: 32df78aedcf4e7e229eec8c9648c82c86f6fea9f4c7176b8780cee67ccf49fcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987405"
---
# <a name="id3dxincludeclose-method"></a>Método ID3DXInclude::Close

Método implementado por el usuario para cerrar un archivo de incluir \# sombreador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al búfer devuelto que contiene las directivas include. Este es el puntero devuelto por la llamada [**ID3DXInclude::Open**](id3dxinclude--open.md) correspondiente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ OK. Si se produce un error en la devolución de llamada al leer el archivo de include, se producirá un error en la API que hizo que se llamara a \# la devolución de llamada. Es uno de los siguientes:

-   El sombreador HLSL producirá un error en una de las funciones D3DXCompileShader. \* \* \*
-   El sombreador de ensamblados producirá un error en una de las funciones D3DXAssembleShader. \* \* \*
-   El efecto producirá un error en una de las funciones D3DXCreateEffect \* \* \* o D3DXCreateEffectCompiler. \* \* \*

## <a name="remarks"></a>Comentarios

Si [**ID3DXInclude::Open**](id3dxinclude--open.md) se ha realizado correctamente, se garantiza que se llamará a **ID3DXInclude::Close** antes de que se devuelva la API que usa esta interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude::Open**](id3dxinclude--open.md)
</dt> </dl>

 

 
