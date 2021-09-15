---
description: Agrega una referencia de datos como elemento secundario de este nodo de datos de archivo ID3DXFileSaveData. La referencia de datos apunta a un objeto de datos de archivo.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: Método ID3DXFileSaveData::AddDataReference (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f4aabf5601ef73f4e1062b1db1a28c1f0deae5fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575220"
---
# <a name="id3dxfilesavedataadddatareference-method"></a>Método ID3DXFileSaveData::AddDataReference

Agrega una referencia de datos como elemento secundario de este nodo de datos de archivo [**ID3DXFileSaveData.**](id3dxfilesavedata.md) La referencia de datos apunta a un objeto de datos de archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre del objeto de datos que se agregará por referencia. Especifique **NULL** si el objeto de datos no tiene un nombre.

</dd> <dt>

*pId* \[ En\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Puntero a un GUID que representa el objeto de datos que se agregará por referencia. Si **es NULL,** se agregará una referencia que apunta al objeto de datos con el nombre especificado por szName.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

El objeto de datos de archivo al que se hace referencia debe tener un nombre o un GUID. El objeto de datos de archivo también debe derivar de un objeto [**ID3DXFileSaveData**](id3dxfilesavedata.md) primario diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
