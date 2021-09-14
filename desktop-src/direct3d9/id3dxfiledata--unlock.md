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
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966735"
---
# <a name="id3dxfiledataunlock-method"></a>Método ID3DXFileData::Unlock

Finaliza la duración del *puntero ppData* devuelto [**por ID3DXFileData::Lock**](id3dxfiledata--lock.md).

## <a name="syntax"></a>Sintaxis


```C++
BOOL Unlock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

El valor devuelto es S \_ OK.

## <a name="remarks"></a>Observaciones

Debe asegurarse de que el número de llamadas [**ID3DXFileData::Lock**](id3dxfiledata--lock.md) coincide con el número de llamadas **ID3DXFileData::Unlock.** Después de llamar a Unlock, ya no se debe usar el puntero ppData devuelto por **ID3DXFileData::Lock.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
