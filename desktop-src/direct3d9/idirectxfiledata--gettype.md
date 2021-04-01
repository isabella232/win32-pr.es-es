---
description: Recupera el GUID de la plantilla del objeto. En desuso.
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: 'IDirectXFileData:: GetType (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 463391c661b2d166a6fba773e3b01590daf0ebd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157224"
---
# <a name="idirectxfiledatagettype-method"></a>IDirectXFileData:: GetType (método)

Recupera el GUID de la plantilla del objeto. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppguid* \[ out, retval\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* \* const**

Dirección de un puntero para recibir el GUID de la plantilla del objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 




