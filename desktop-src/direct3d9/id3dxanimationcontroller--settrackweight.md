---
description: Establece el peso de la pista. El peso se utiliza para determinar cómo combinar varias pistas.
ms.assetid: a00ceae4-47b4-4fb9-a028-97493e3dc071
title: 'ID3DXAnimationController:: SetTrackWeight (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc42d283231a0e49359531827cc785bd83aefc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821506"
---
# <a name="id3dxanimationcontrollersettrackweight-method"></a>ID3DXAnimationController:: SetTrackWeight (método)

Establece el peso de la pista. El peso se utiliza para determinar cómo combinar varias pistas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTrackWeight(
  [in] UINT  Track,
  [in] FLOAT Weight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador de la pista en la que se va a establecer el peso.

</dd> <dt>

*Peso* \[ de de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor de peso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
