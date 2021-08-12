---
description: Acceda al búfer de vértices de la malla después de que se haya confirmado en el dispositivo con ID3DX10Mesh::CommitToDevice. Esto es diferente de ID3DX10Mesh::GetVertexBuffer, que devuelve el búfer de vértices antes de que se haya confirmado en el dispositivo.
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: Método ID3DX10Mesh::GetDeviceVertexBuffer (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 11493392f710fe3fd3bebab5187b61522434b268bf099489d84ea1cc3ec99309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540268"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a>Método ID3DX10Mesh::GetDeviceVertexBuffer

Acceda al búfer de vértices de la malla después de que se haya confirmado en el dispositivo [**con ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md). Esto es diferente de [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), que devuelve el búfer de vértices antes de que se haya confirmado en el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iBuffer* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice que identifica a qué búfer de vértices se va a acceder.

</dd> <dt>

*ppVertexBuffer* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Búfer de vértice después de que se haya confirmado en el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
