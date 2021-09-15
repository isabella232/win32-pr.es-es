---
description: Crea y agrega un objeto de referencia de datos como un objeto secundario. En desuso.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: Método IDirectXFileData::AddDataReference (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 44834af51380c3b8bdbb4e9a4b24bf911ea6a07f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466061"
---
# <a name="idirectxfiledataadddatareference-method"></a>IDirectXFileData::AddDataReference (método)

Crea y agrega un objeto de referencia de datos como un objeto secundario. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szRef* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre del objeto de datos al que se hace referencia. Este parámetro puede ser **NULL si** pguidRef proporciona una referencia al GUID.

</dd> <dt>

*pguidRef* \[ En\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Puntero al GUID que representa los datos. Este parámetro puede ser **NULL si** szRef proporciona una referencia al nombre.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes valores. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Observaciones

Para que este método se haga correctamente, el parámetro szRef o pguidRef debe ser distinto de **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 
