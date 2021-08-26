---
description: 'Método ID3DXAnimationSet::GetCallback: obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.'
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: Método ID3DXAnimationSet::GetCallback (D3dx9anim.h)
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
ms.openlocfilehash: 4ded66bbe90320250667511d1c9468073693ce789cdb7add8574f42a4756136d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026595"
---
# <a name="id3dxanimationsetgetcallback-method"></a>Método ID3DXAnimationSet::GetCallback

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

*Posición* \[ En\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Posición desde la que se buscarán las devoluciones de llamada.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Marcas de búsqueda de devolución de llamada. Este parámetro se puede establecer en una combinación de una o varias marcas de [**D3DXCALLBACK \_ SEARCH \_ FLAGS**](./d3dxcallback-search-flags.md).

</dd> <dt>

*pCallbackPosition* \[ out\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)\***

Puntero a la posición de la devolución de llamada.

</dd> <dt>

*ppCallbackData* \[ out\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

Dirección del puntero de datos de devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Los valores devueltos de este método los implementa un programador de aplicaciones. En general, si no se produce ningún error, programe el método para devolver D3D \_ OK. De lo contrario, programe el método para devolver un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR.**](./d3dxerr.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
