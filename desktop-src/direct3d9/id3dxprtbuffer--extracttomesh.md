---
description: Extrae los datos coeficientes de un búfer de un solo canal y agrega los datos a un objeto ID3DXMesh.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: 'ID3DXPRTBuffer:: ExtractToMesh (método) (D3DX9Mesh. h)'
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
ms.openlocfilehash: e6dfe545a934f541938d6030cdc3814f451d93c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708117"
---
# <a name="id3dxprtbufferextracttomesh-method"></a>ID3DXPRTBuffer:: ExtractToMesh (método)

Extrae los datos coeficientes de un búfer de un solo canal y agrega los datos a un objeto [**ID3DXMesh**](id3dxmesh.md) .

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

*NumCoefficients* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de coeficientes que se van a extraer del búfer. Cuando se usa la transferencia Radiance (PRT) precalculada de armónico (SH), el número de coeficientes debe ser Order ². El orden debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.

</dd> <dt>

*Uso* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descripciones del uso de vértices de la malla. Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndexStart* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice inicial de los coeficientes que se van a almacenar en la malla.

</dd> <dt>

*pScene* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) que almacenará los coeficientes.

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

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
