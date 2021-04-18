---
description: 'Quita los datos de malla del dispositivo que se ha confirmado en el dispositivo (con ID3DX10Mesh:: CommitToDevice).'
ms.assetid: 60eee1f8-f04b-4f33-8f86-0564d0334f97
title: ID3DX10Mesh::D método iscard (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Discard
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f861de8eefff603954e896a1b6684afc8806764f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678794"
---
# <a name="id3dx10meshdiscard-method"></a>ID3DX10Mesh::D método iscard

Quita los datos de malla del dispositivo que se ha confirmado en el dispositivo (con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md)).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Discard(
  [in] D3DX10_MESH_DISCARD_FLAGS dwDiscard
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwDiscard* \[ de\]
</dt> <dd>

Tipo: **[ **\_ \_ \_ marcas de descartado de malla D3DX10**](d3dx10-mesh-discard-flags.md)**

Especifica qué partes de los datos de la malla se van a descartar del dispositivo. Consulte [**D3DX10 \_ mesh \_ discard \_ Flags**](d3dx10-mesh-discard-flags.md).

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

 

 




