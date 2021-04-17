---
description: Método implementado por el usuario para abrir y leer el contenido de un archivo de inclusión de sombreador \# .
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'ID3DXInclude:: Open (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698394"
---
# <a name="id3dxincludeopen-method"></a>ID3DXInclude:: Open (método)

Método implementado por el usuario para abrir y leer el contenido de un archivo de inclusión de sombreador \# .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IncludeType* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXINCLUDE \_ Type**](./d3dxinclude-type.md)**

Ubicación del archivo de \# inclusión. Consulte [**\_ tipo de D3DXINCLUDE**](./d3dxinclude-type.md).

</dd> <dt>

*pFileName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre del \# archivo de inclusión.

</dd> <dt>

*pParentData* \[ de\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al contenedor que incluye el \# archivo de inclusión. El compilador podría pasar NULL en *pParentData*. Para obtener más información, vea la sección "buscar archivos de inclusión" en [compilar un efecto (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).

</dd> <dt>

*ppData* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Puntero al búfer devuelto que contiene las directivas Include. Este puntero sigue siendo válido hasta que se llama a [**ID3DXInclude:: Close**](id3dxinclude--close.md) .

</dd> <dt>

*pBytes* \[ enuncia\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Número de bytes devueltos en ppData.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ correcto. Si se produce un error en la devolución de llamada al leer el \# archivo de inclusión, se producirá un error en la API que provocó la llamada de devolución de llamada. Es uno de los siguientes:

-   El sombreador HLSL producirá un error en una de las funciones de D3DXCompileShader \* \* \* .
-   El sombreador de ensamblado producirá un error en una de las funciones de D3DXAssembleShader \* \* \* .
-   El efecto producirá un error en una de las \* \* \* funciones D3DXCreateEffect o D3DXCreateEffectCompiler \* \* \* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude:: Close**](id3dxinclude--close.md)
</dt> </dl>

 

 
