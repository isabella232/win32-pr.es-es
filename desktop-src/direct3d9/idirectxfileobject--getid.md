---
description: Recupera un puntero al GUID que identifica un objeto de archivo DirectX. En desuso.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: Método IDirectXFileObject::GetId (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 5cb6788afe0b937822b8895790584f6928a7b5aecb564a31540337935763b2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800187"
---
# <a name="idirectxfileobjectgetid-method"></a>IDirectXFileObject::GetId (método)

Recupera un puntero al GUID que identifica un objeto de archivo DirectX. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGuid* \[ out, retval\]
</dt> <dd>

Tipo: **LPGUID**

Puntero a un GUID para recibir el identificador del objeto. La función establecerá el GUID en un GUID **NULL** si el objeto no tiene un identificador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IDirectXFileObject](idirectxfileobject.md)
</dt> </dl>

 

 




