---
description: Recupera el siguiente objeto de datos secundario, el objeto de referencia de datos o el objeto binario en el archivo DirectX. En desuso.
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: Método IDirectXFileData::GetNextObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466059"
---
# <a name="idirectxfiledatagetnextobject-method"></a>IDirectXFileData::GetNextObject (método)

Recupera el siguiente objeto de datos secundario, el objeto de referencia de datos o el objeto binario en el archivo DirectX. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppChildObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***

Dirección de un puntero a una [**interfaz IDirectXFileObject,**](idirectxfileobject.md) que representa la interfaz de objeto de archivo del objeto secundario devuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes valores: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS.

## <a name="remarks"></a>Observaciones

Para determinar el tipo de objeto recuperado, use QueryInterface para consultar el objeto recuperado para obtener compatibilidad con las interfaces [**IDirectXFileData,**](idirectxfiledata.md) [**IDirectXFileDataReference**](idirectxfiledatareference.md)o [**IDirectXFileBinary.**](idirectxfilebinary.md) La interfaz admitida indica el tipo de objeto (datos, referencia de datos o binario).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirectXFileBinary**](idirectxfilebinary.md)
</dt> <dt>

[**IDirectXFileData**](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileDataReference**](idirectxfiledatareference.md)
</dt> </dl>

 

 




