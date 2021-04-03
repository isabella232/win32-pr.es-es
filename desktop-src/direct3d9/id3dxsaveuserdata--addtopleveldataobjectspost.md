---
description: Agregue un objeto de nivel superior después de la jerarquía de fotogramas.
ms.assetid: 43b3cdb3-c6f0-4028-bf86-43d643fba73d
title: 'ID3DXSaveUserData:: AddTopLevelDataObjectsPost (método) (D3dx9anim. h)'
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
ms.openlocfilehash: 3573bae8cbcb6858b04207f936545b7cf93959c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083800"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspost-method"></a>ID3DXSaveUserData:: AddTopLevelDataObjectsPost (método)

Agregue un objeto de nivel superior después de la jerarquía de fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddTopLevelDataObjectsPost(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pXofSave* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Puntero a un archivo. x guarda el objeto. Use este puntero para llamar a [**IDirectXFileSaveObject:: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para crear el objeto de datos que se va a guardar. A continuación, llame a [**IDirectXFileSaveObject:: savedata**](idirectxfilesaveobject--savedata.md) para guardar los datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Un programador de aplicaciones implementa los valores devueltos de este método. En general, si no se produce ningún error, programe el método para devolver D3D \_ OK. De lo contrario, programe el método para que devuelva un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
