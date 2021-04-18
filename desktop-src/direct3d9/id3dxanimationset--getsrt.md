---
description: Obtiene los valores de escala, rotación y traslación del conjunto de animaciones.
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'ID3DXAnimationSet:: GetSRT (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b70243dd9aa2f304d80eaff2e2cc7695dad43379
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718521"
---
# <a name="id3dxanimationsetgetsrt-method"></a>ID3DXAnimationSet:: GetSRT (método)

Obtiene los valores de escala, rotación y traslación del conjunto de animaciones.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PeriodicPosition* \[ de\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Posición del conjunto de animaciones. La posición se puede obtener llamando a [**ID3DXAnimationSet:: GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).

</dd> <dt>

*Animación* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de animación.

</dd> <dt>

*pScale* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero al vector [**D3DXVECTOR3**](d3dxvector3.md) que describe la escala del conjunto de animaciones.

</dd> <dt>

*Prot.* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero al cuaternión [**D3DXQUATERNION**](d3dxquaternion.md) que describe el giro del conjunto de animaciones.

</dd> <dt>

*pTranslation* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero al vector [**D3DXVECTOR3**](d3dxvector3.md) que describe la traslación del conjunto de animaciones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Un programador de aplicaciones implementa los valores devueltos de este método. En general, si no se produce ningún error, programe el método para devolver D3D \_ OK. En caso contrario, programe el método para que devuelva un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
