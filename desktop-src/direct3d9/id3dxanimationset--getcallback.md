---
description: Obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'ID3DXAnimationSet:: GetCallback (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4cde6c9d51fd29c0412f33b34ca7bea8260dfea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280505"
---
# <a name="id3dxanimationsetgetcallback-method"></a>ID3DXAnimationSet:: GetCallback (método)

Obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Posición* \[ de de\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Posición desde la que se van a buscar devoluciones de llamada.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Marcas de búsqueda de devolución de llamada. Este parámetro se puede establecer en una combinación de una o varias marcas de [**las \_ \_ marcas de búsqueda de D3DXCALLBACK**](./d3dxcallback-search-flags.md).

</dd> <dt>

*pCallbackPosition* \[ enuncia\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)\***

Puntero a la posición de la devolución de llamada.

</dd> <dt>

*ppCallbackData* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

Dirección del puntero de datos de devolución de llamada.

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

 

 
