---
description: Recupera un puntero a este nodo de datos de archivo ID3DXFileSaveObject.
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: Método ID3DXFileSaveData::GetSave (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e23296ad0a866a0ad289a9a587c433411ef9bb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063719"
---
# <a name="id3dxfilesavedatagetsave-method"></a>Método ID3DXFileSaveData::GetSave

Recupera un puntero a este nodo de datos [**de archivo ID3DXFileSaveObject.**](id3dxfilesaveobject.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppObj* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Dirección de un puntero a una [**interfaz ID3DXFileSaveObject**](id3dxfilesaveobject.md) que representa este nodo de datos de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el siguiente valor: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




