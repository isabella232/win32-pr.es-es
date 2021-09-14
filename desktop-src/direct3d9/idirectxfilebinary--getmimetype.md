---
description: Recupera el tipo de extensiones multipropósito de Correo electrónico de Internet (MIME) para los datos binarios. En desuso.
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: Método IDirectXFileBinary::GetMimeType (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168482"
---
# <a name="idirectxfilebinarygetmimetype-method"></a>IDirectXFileBinary::GetMimeType (método)

Recupera el tipo de extensiones multipropósito de Correo electrónico de Internet (MIME) para los datos binarios. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszMimeType* \[ out\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Dirección de un puntero para recibir la cadena de tipo MIME.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método , el valor devuelto puede ser DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Observaciones

Cuando no se especifica ningún tipo MIME en un archivo DirectX para un objeto binario, la función establecerá pszMimeType en **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
