---
description: Escala todos los ejemplos asociados a un submesh determinado. El método es útil para calcular la dispersión de subsuelo.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: Método ID3DXPRTEngine::ScaleMeshChunk (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a42046678ef0b44f011c8440cd3456dc9ff236ec0f7a280b4650b49aa53c10d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729589"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a>Método ID3DXPRTEngine::ScaleMeshChunk

Escala todos los ejemplos asociados a un submesh determinado. El método es útil para calcular la dispersión de subsuelo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uMeshChunk* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ubicación en la malla en la que se empiezan a escalar los ejemplos.

</dd> <dt>

*fScale* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor por el que se va a multiplicar cada vector de la submesh.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un [**objeto ID3DXPRTBuffer**](id3dxprtbuffer.md) para recibir muestras reescaladas en el submesh.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
