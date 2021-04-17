---
description: Obtenga acceso al búfer de atributo de la malla.
ms.assetid: 01ebb592-1e0d-4d93-b3f5-ad5f1e0225d0
title: 'ID3DX10Mesh:: GetAttributeBuffer (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 161711cd28dae790fd25ff8dd192945a366e9dd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707990"
---
# <a name="id3dx10meshgetattributebuffer-method"></a>ID3DX10Mesh:: GetAttributeBuffer (método)

Obtenga acceso al búfer de atributo de la malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAttributeBuffer(
  [out] ID3DX10MeshBuffer **ppAttributeBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAttributeBuffer* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Búfer de atributo. Vea [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).

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

 

 




