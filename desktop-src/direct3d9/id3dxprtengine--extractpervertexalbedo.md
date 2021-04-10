---
description: Copia los valores de Albedo por vértice de una malla.
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: 'ID3DXPRTEngine:: ExtractPerVertexAlbedo (método) (D3DX9Mesh. h)'
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
ms.openlocfilehash: ed23b75b3113421b6242f49416e4b54bfce336f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003950"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a>ID3DXPRTEngine:: ExtractPerVertexAlbedo (método)

Copia los valores de Albedo por vértice de una malla.

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

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero al objeto de malla [**ID3DXMesh**](id3dxmesh.md) usado en [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) para crear el objeto [**ID3DXPRTEngine**](id3dxprtengine.md) .

</dd> <dt>

*Uso* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descripciones de uso de vértices para copiar desde la malla. Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*NumChanIn* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de canales de color que se copiarán de la malla. Establézcalo en 1 para especificar materiales grises (R = G = B) o 3 para habilitar los efectos de sangrado de color.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
