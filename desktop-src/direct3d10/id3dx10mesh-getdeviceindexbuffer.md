---
description: Acceda al búfer de índice de la malla después de que se haya confirmado en el dispositivo con ID3DX10Mesh::CommitToDevice. Esto es diferente de ID3DX10Mesh::GetIndexBuffer, que devuelve el búfer de índice antes de que se haya confirmado en el dispositivo.
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: Método ID3DX10Mesh::GetDeviceIndexBuffer (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 869bd40b49801a1469ca08baa3a493cc23e6f6238624380411c8d91de829c79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990375"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a>Método ID3DX10Mesh::GetDeviceIndexBuffer

Acceda al búfer de índice de la malla después de que se haya confirmado en el dispositivo [**con ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md). Esto es diferente de [**ID3DX10Mesh::GetIndexBuffer,**](id3dx10mesh-getindexbuffer.md)que devuelve el búfer de índice antes de que se haya confirmado en el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIndexBuffer* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Búfer de índice después de que se haya confirmado en el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Si el búfer de índice de la malla aún no se ha confirmado en el dispositivo, esta API confirmará automáticamente el búfer de índice antes de devolver un puntero al búfer.

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

 

 




