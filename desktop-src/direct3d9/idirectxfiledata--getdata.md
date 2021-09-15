---
description: Recupera los datos de uno de los miembros del objeto o los datos de todos los miembros. En desuso.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: Método IDirectXFileData::GetData (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: ed52aaf0b4c740b675129c81843c0bd49c7f428e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466060"
---
# <a name="idirectxfiledatagetdata-method"></a>IDirectXFileData::GetData (método)

Recupera los datos de uno de los miembros del objeto o los datos de todos los miembros. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szMember* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre del miembro para el que se recuperarán los datos. Especifique **NULL** para recuperar todos los datos de los miembros necesarios.

</dd> <dt>

*sizesize* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero para recibir el tamaño del búfer ppvData, en bytes.

</dd> <dt>

*ppvData* \[ out\]
</dt> <dd>

Tipo: **\* \* void**

Dirección de un puntero al búfer para recibir los datos asociados a szMember. Si szMember es **NULL,** ppvData se establece para que apunte a un búfer que contiene todos los datos de los miembros necesarios en un bloque contiguo de memoria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes valores: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADDataReference y DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Observaciones

Este método recupera los datos de los miembros necesarios de un objeto de datos, pero no los datos de los miembros opcionales (secundarios). Use [**IDirectXFileData::GetNextObject para**](idirectxfiledata--getnextobject.md) recuperar objetos secundarios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
