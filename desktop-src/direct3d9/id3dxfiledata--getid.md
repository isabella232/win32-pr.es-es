---
description: Recupera el GUID de este objeto de datos de archivo.
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: Método ID3DXFileData::GetId (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1dafb296541b1702e9163dcc6d460cf149b4007
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969640"
---
# <a name="id3dxfiledatagetid-method"></a>Método ID3DXFileData::GetId

Recupera el GUID de este objeto de datos de archivo.

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

Puntero a un GUID para recibir el identificador de este objeto de datos de archivo. Si el objeto de datos de archivo no tiene ningún identificador, el valor del parámetro devuelto será GUID \_ NULL.

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

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




