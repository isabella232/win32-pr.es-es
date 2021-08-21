---
description: Extrae los datos de coeficiente de un búfer de canal único y agrega los datos a un objeto ID3DXMesh.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: Método ID3DXPRTBuffer::ExtractToMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c838a146a390aa72ac24781ca6f136b028ad41a6ee94fb4210ec4bd3f557acdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120619"
---
# <a name="id3dxprtbufferextracttomesh-method"></a>Método ID3DXPRTBuffer::ExtractToMesh

Extrae los datos de coeficiente de un búfer de canal único y agrega los datos a un [**objeto ID3DXMesh.**](id3dxmesh.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumCoefficients* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de coeficientes que se extraerán del búfer. Cuando se usa la transferencia de base precalutada (PRT) esférica (SH), el número de coeficientes debe ser Order ntes. El orden debe estar en el intervalo [de D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.

</dd> <dt>

*Uso* \[ En\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descripciones de uso de vértices de la malla. Vea [**D3DDECLUSAGE.**](./d3ddeclusage.md)

</dd> <dt>

*UsageIndexStart* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice inicial para los coeficientes que se almacenarán en la malla.

</dd> <dt>

*pScene* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a un [**objeto de malla ID3DXMesh**](id3dxmesh.md) que almacenará coeficientes.

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

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
