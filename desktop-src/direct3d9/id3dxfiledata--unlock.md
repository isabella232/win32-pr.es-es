---
description: Finaliza la duración del puntero ppData devuelto por ID3DXFileData::Lock.
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: Método ID3DXFileData::Unlock (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5eaa1466f722f34bb82152d22c85647cf5afa88310474585b7f944b37af3abf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026235"
---
# <a name="id3dxfiledataunlock-method"></a>Método ID3DXFileData::Unlock

Finaliza la duración del *puntero ppData* devuelto por [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).

## <a name="syntax"></a>Sintaxis


```C++
BOOL Unlock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

El valor devuelto es S \_ OK.

## <a name="remarks"></a>Comentarios

Debe asegurarse de que el número de llamadas [**ID3DXFileData::Lock**](id3dxfiledata--lock.md) coincide con el número de llamadas **ID3DXFileData::Unlock.** Después de llamar a Unlock, ya no se debe usar el puntero ppData devuelto por **ID3DXFileData::Lock.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
