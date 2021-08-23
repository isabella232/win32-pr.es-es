---
description: Método implementado por el usuario para abrir y leer el contenido de un archivo de contenido \# de un sombreador.
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: Método ID3DXInclude::Open (D3DX9Shader.h)
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
ms.openlocfilehash: e50b4774f6ed62b1e8a6e6cb85b5732efd878302563958e25e6b9017f9acc58d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987395"
---
# <a name="id3dxincludeopen-method"></a>Método ID3DXInclude::Open

Método implementado por el usuario para abrir y leer el contenido de un archivo de contenido \# de un sombreador.

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

*IncludeType* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXINCLUDE \_ TYPE**](./d3dxinclude-type.md)**

Ubicación del archivo \# de incluir. Vea [**D3DXINCLUDE \_ TYPE**](./d3dxinclude-type.md).

</dd> <dt>

*pFileName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre del archivo \# de incluir.

</dd> <dt>

*pParentData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al contenedor que incluye el \# archivo de incluir. El compilador podría pasar NULL en *pParentData.* Para obtener más información, vea la sección "Buscar archivos de incluir" en [Compilar un efecto (Direct3D 11).](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md)

</dd> <dt>

*ppData* \[ out\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Puntero al búfer devuelto que contiene las directivas include. Este puntero sigue siendo válido hasta [**que se llama a ID3DXInclude::Close.**](id3dxinclude--close.md)

</dd> <dt>

*pBytes* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Número de bytes devueltos en ppData.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ OK. Si se produce un error en la devolución de llamada al leer el archivo include, se producirá un error en la API que hizo que se llamara a \# la devolución de llamada. Es uno de los siguientes:

-   El sombreador HLSL producirá un error en una de las funciones D3DXCompileShader. \* \* \*
-   El sombreador de ensamblados producirá un error en una de las funciones D3DXAssembleShader. \* \* \*
-   El efecto producirá un error en una de las funciones D3DXCreateEffect \* \* \* o D3DXCreateEffectCompiler. \* \* \*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude::Close**](id3dxinclude--close.md)
</dt> </dl>

 

 
