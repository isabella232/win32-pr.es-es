---
description: 'Obtenga acceso al búfer de vértices de la malla una vez que se haya confirmado en el dispositivo con ID3DX10Mesh:: CommitToDevice. Esto es diferente de ID3DX10Mesh:: GetVertexBuffer, que devuelve el búfer de vértices antes de que se haya confirmado en el dispositivo.'
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'ID3DX10Mesh:: GetDeviceVertexBuffer (método) (D3DX10. h)'
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
ms.openlocfilehash: 9943050d174acb4e8f8e676f56a95cfdcde88f5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718369"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a>ID3DX10Mesh:: GetDeviceVertexBuffer (método)

Obtenga acceso al búfer de vértices de la malla una vez que se haya confirmado en el dispositivo con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md). Esto es diferente de [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), que devuelve el búfer de vértices antes de que se haya confirmado en el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iBuffer* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice que identifica a qué búfer de vértice se va a tener acceso.

</dd> <dt>

*ppVertexBuffer* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Búfer de vértices después de que se haya confirmado en el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
