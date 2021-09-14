---
description: Agregue un objeto de nivel superior antes de la jerarquía de fotogramas.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: Método ID3DXSaveUserData::AddTopLevelDataObjectsPre (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPre
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0194c8c9c6806f96cbe75394e6650ca3e7dc74b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966651"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a>Método ID3DXSaveUserData::AddTopLevelDataObjectsPre

Agregue un objeto de nivel superior antes de la jerarquía de fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddTopLevelDataObjectsPre(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pXofSave* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Puntero a un objeto de guardado de archivo .x. Use este puntero para llamar a [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para crear el objeto de datos que se va a guardar. A [**continuación, llame a IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) para guardar los datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Los valores devueltos de este método los implementa un programador de aplicaciones. En general, si no se produce ningún error, programe el método para devolver D3D \_ OK. De lo contrario, programe el método para devolver un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también devuelva el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
