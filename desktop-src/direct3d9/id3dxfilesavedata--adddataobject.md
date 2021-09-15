---
description: Agrega un objeto de datos como elemento secundario del nodo de datos de archivo ID3DXFileSaveData.
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: Método ID3DXFileSaveData::AddDataObject (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b097e63792b32bc1688ce93c8ce32ffaedeae6ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270183"
---
# <a name="id3dxfilesavedataadddataobject-method"></a>Método ID3DXFileSaveData::AddDataObject

Agrega un objeto de datos como elemento secundario del nodo de datos [**de archivo ID3DXFileSaveData.**](id3dxfilesavedata.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rguidTemplate* \[ En\]
</dt> <dd>

Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

GUID que representa la plantilla del objeto de datos.

</dd> <dt>

*szName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre del objeto de datos que se agrega. Especifique **NULL** si el objeto no tiene un nombre.

</dd> <dt>

*pId* \[ En\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Puntero a un GUID que representa el objeto de datos. El objeto de datos debe estar registrado con [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) o [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md). Especifique **NULL** si el objeto no tiene un GUID.

</dd> <dt>

*cbSize* \[ En\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Tamaño del objeto de datos, en bytes.

</dd> <dt>

*pvData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero a un búfer que contiene todos los datos necesarios en el objeto de datos.

</dd> <dt>

*ppObj* \[ in, retval\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***

Dirección de un puntero a una [**interfaz ID3DXFileSaveData,**](id3dxfilesavedata.md) que representa el nodo de datos de archivo al que se agregará el objeto de datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
