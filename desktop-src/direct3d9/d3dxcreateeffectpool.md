---
description: Cree un grupo de efectos. Un grupo se utiliza para compartir parámetros entre efectos.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: Función D3DXCreateEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280474"
---
# <a name="d3dxcreateeffectpool-function"></a>D3DXCreateEffectPool función)

Cree un grupo de efectos. Un grupo se utiliza para compartir parámetros entre efectos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppPool* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Devuelve un puntero al grupo creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.

Si los argumentos no son válidos, el método devolverá D3DERR \_ INVALIDCALL.

Si se produce un error en el método, el valor devuelto será E \_ producirá un error.

## <a name="remarks"></a>Observaciones

En el caso de los efectos de un grupo, los parámetros compartidos con el mismo nombre comparten los mismos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de efecto](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




