---
description: Quita un conjunto de animaciones del controlador de animación.
ms.assetid: 2ca99651-8249-44c2-9560-b3cfaa930862
title: 'ID3DXAnimationController:: UnregisterAnimationSet (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnregisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35c70552f16daac6d2cfed5cbccf268179526ae1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698424"
---
# <a name="id3dxanimationcontrollerunregisteranimationset-method"></a>ID3DXAnimationController:: UnregisterAnimationSet (método)

Quita un conjunto de animaciones del controlador de animación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnregisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAnimSet* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Puntero a la animación [**ID3DXAnimationSet**](id3dxanimationset.md) establecida en Remove.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTFOUND.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




