---
description: Extrae los coeficientes de proyección de análisis de componentes principales por ejemplo (PCA) de un búfer de datos comprimidos ID3DXPRTCompBuffer y agrega los datos a un objeto ID3DXMesh.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'ID3DXPRTCompBuffer:: ExtractToMesh (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 607b583b89358d2d28030a4187b1608174d849c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707783"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a>ID3DXPRTCompBuffer:: ExtractToMesh (método)

Extrae los coeficientes de proyección de análisis de componentes principales por ejemplo (PCA) de un búfer de datos comprimidos [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) y agrega los datos a un objeto [**ID3DXMesh**](id3dxmesh.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumPCA* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de coeficientes de PCA que se van a extraer del búfer.

</dd> <dt>

*Uso* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descripciones del uso de vértices de la malla. Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndexStart* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice inicial de los coeficientes de PCA que se va a almacenar en la malla.

</dd> <dt>

*pScene* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) que almacenará los coeficientes del PCA.

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

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
