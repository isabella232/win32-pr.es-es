---
description: Agregue un objeto de nivel superior después de la jerarquía de fotogramas.
ms.assetid: 43b3cdb3-c6f0-4028-bf86-43d643fba73d
title: Método ID3DXSaveUserData::AddTopLevelDataObjectsPost (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPost
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd0d631a814b25e8ff99272a29af377941e2a6865bd41e6a2fb2c6bcc8fc59a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727825"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspost-method"></a>Método ID3DXSaveUserData::AddTopLevelDataObjectsPost

Agregue un objeto de nivel superior después de la jerarquía de fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddTopLevelDataObjectsPost(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pXofSave* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Puntero a un objeto de guardado de archivo .x. Use este puntero para llamar a [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para crear el objeto de datos que se va a guardar. A continuación, [**llame a IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) para guardar los datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Los valores devueltos de este método los implementa un programador de aplicaciones. En general, si no se produce ningún error, programe el método para devolver D3D \_ OK. De lo contrario, programe el método para devolver un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también presente un error y devuelva el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
