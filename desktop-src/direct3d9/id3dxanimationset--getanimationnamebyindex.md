---
description: Obtiene el nombre de una animación, dado su índice.
ms.assetid: vs|directx_sdk|~\id3dxanimationset__getanimationnamebyindex.htm
title: Método ID3DXAnimationSet::GetAnimationNameByIndex (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationNameByIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 820b21fa69fd7007bdd1971e83ea44368dce5cc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060632"
---
# <a name="id3dxanimationsetgetanimationnamebyindex-method"></a>Método ID3DXAnimationSet::GetAnimationNameByIndex

Obtiene el nombre de una animación, dado su índice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAnimationNameByIndex(
  [in]  UINT   Index,
  [out] LPCSTR *ppName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de la animación.

</dd> <dt>

*ppName* \[ out\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Dirección de un puntero a una cadena que recibe el nombre de animación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Los valores devueltos de este método los implementa un programador de aplicaciones. En general, si no se produce ningún error, programe el método para devolver D3D \_ OK. De lo contrario, programe el método para devolver un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
