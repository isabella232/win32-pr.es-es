---
description: Carga en memoria un búfer de transferencia de radiancia (PRT) precalutado que se guardó en el disco.
ms.assetid: b9296c9e-e8ff-4a18-8682-fcac4feb64e9
title: Función D3DXLoadPRTBufferFromFile (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d24bd428519673c907693f53a82498269cedad6f55d6626ab10094f8488ab78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986535"
---
# <a name="d3dxloadprtbufferfromfile-function"></a>Función D3DXLoadPRTBufferFromFile

Carga en memoria un búfer de transferencia de radiancia (PRT) precalutado que se guardó en el disco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXLoadPRTBufferFromFile(
  _In_    LPCSTR          pFileName,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFileName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre del archivo desde el que se cargan los datos del búfer.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

Dirección de un puntero al objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve en D3DXLoadPRTBufferFromFileW. De lo contrario, la llamada de función se resuelve en D3DXLoadPRTBufferFromFileA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de transferencia de radiancia precalutadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
