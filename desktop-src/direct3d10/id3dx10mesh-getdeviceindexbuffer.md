---
description: 'Obtenga acceso al búfer de índice de la malla una vez que se haya confirmado en el dispositivo con ID3DX10Mesh:: CommitToDevice. Esto es diferente de ID3DX10Mesh:: GetIndexBuffer, que devuelve el búfer de índice antes de que se haya confirmado en el dispositivo.'
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'ID3DX10Mesh:: GetDeviceIndexBuffer (método) (D3DX10. h)'
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
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698328"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a>ID3DX10Mesh:: GetDeviceIndexBuffer (método)

Obtenga acceso al búfer de índice de la malla una vez que se haya confirmado en el dispositivo con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md). Esto es diferente de [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), que devuelve el búfer de índice antes de que se haya confirmado en el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIndexBuffer* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Búfer de índice después de haberse confirmado en el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Si el búfer de índice de la malla aún no se ha confirmado en el dispositivo, esta API confirmará automáticamente el búfer de índice antes de devolver un puntero al búfer.

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

 

 




