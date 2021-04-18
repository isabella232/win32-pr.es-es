---
description: Aplica la animación establecida a la pista especificada.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'ID3DXAnimationController:: SetTrackAnimationSet (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718409"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a>ID3DXAnimationController:: SetTrackAnimationSet (método)

Aplica la animación establecida a la pista especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador de la pista a la que se aplica el conjunto de animaciones.

</dd> <dt>

*pAnimSet* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Puntero al conjunto de animaciones [**ID3DXAnimationSet**](id3dxanimationset.md) que se va a agregar a la pista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Este método establece la animación establecida en la pista especificada para la combinación. El conjunto de animación de cada pista se combina según el peso y la velocidad del seguimiento cuando se llama a [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
