---
description: Recupera el GUID de este nodo de datos de archivo ID3DXFileSaveData.
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: Método ID3DXFileSaveData::GetId (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e6f502357510cc1c8fc51e9ada844a988a79b1571435639586380929b121c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748505"
---
# <a name="id3dxfilesavedatagetid-method"></a>Método ID3DXFileSaveData::GetId

Recupera el GUID de este nodo [**de datos de archivo ID3DXFileSaveData.**](id3dxfilesavedata.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pId* \[ out\]
</dt> <dd>

Tipo: **LPGUID**

Puntero a un GUID para recibir el identificador de este nodo de datos de archivo. Si el objeto no tiene ningún identificador, el valor del parámetro devuelto será GUID \_ NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el siguiente valor: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




