---
description: Extrae los coeficientes de proyección de análisis de componentes principales (PCA) por ejemplo de un búfer de datos comprimido ID3DXPRTCompBuffer y agrega los datos a un objeto ID3DXMesh.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: Método ID3DXPRTCompBuffer::ExtractToMesh (D3DX9Mesh.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060526"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a>Método ID3DXPRTCompBuffer::ExtractToMesh

Extrae los coeficientes de proyección de análisis de componentes principales (PCA) por ejemplo de un búfer de datos comprimido [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) y agrega los datos a un [**objeto ID3DXMesh.**](id3dxmesh.md)

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

*NumPCA* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de coeficientes de PCA que se extraerán del búfer.

</dd> <dt>

*Uso* \[ En\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descripciones de uso de vértices de la malla. Vea [**D3DDECLUSAGE.**](./d3ddeclusage.md)

</dd> <dt>

*UsageIndexStart* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice inicial para los coeficientes de PCA que se almacenarán en la malla.

</dd> <dt>

*pScene* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a un [**objeto de malla ID3DXMesh**](id3dxmesh.md) que almacenará coeficientes de PCA.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
