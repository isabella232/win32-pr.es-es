---
description: Copia los valores albedo por vértice de una malla.
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: Método ID3DXPRTEngine::ExtractPerVertexAlbedo (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ExtractPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8e094a7681c13e21cdaab71648b3733749fc179f845e23496a07f3c2b7b99234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747755"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a>Método ID3DXPRTEngine::ExtractPerVertexAlbedo

Copia los valores albedo por vértice de una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExtractPerVertexAlbedo(
  [in] LPD3DXMESH   pMesh,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         NumChanIn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero al [**objeto de malla ID3DXMesh**](id3dxmesh.md) usado en [**D3DXCreatePRTEngine para**](d3dxcreateprtengine.md) crear el objeto [**ID3DXPRTEngine.**](id3dxprtengine.md)

</dd> <dt>

*Uso* \[ En\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descripciones de uso de vértices que se copian desde la malla. Vea [**D3DDECLUSAGE.**](./d3ddeclusage.md)

</dd> <dt>

*NumChanIn* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de canales de color que se copian de la malla. Establezca en 1 para especificar materiales grises (R = G = B) o 3 para habilitar los efectos de color de color.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
