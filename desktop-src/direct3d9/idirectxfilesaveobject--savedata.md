---
description: Guarda un objeto de datos y sus elementos secundarios en un archivo de DirectX. En desuso.
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: 'IDirectXFileSaveObject:: SaveData (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: cb901bd984e1fcd923d0ea172fb5f387b3a9302a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717720"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a>IDirectXFileSaveObject:: SaveData (método)

Guarda un objeto de datos y sus elementos secundarios en un archivo de DirectX. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDataObj* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**

Puntero a una interfaz [**IDirectXFileData**](idirectxfiledata.md) que representa el objeto de datos de archivo que se va a guardar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> </dl>

 

 




