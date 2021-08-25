---
description: Agregue datos secundarios a la malla.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: Método ID3DXSaveUserData::AddMeshChildData (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 397dc9ade32222dd98e050110811464f6544a1d0af52729417c61fbc3367bdbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893315"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a>Método ID3DXSaveUserData::AddMeshChildData

Agregue datos secundarios a la malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddMeshChildData(
  [in] const D3DXMESHCONTAINER    *pMeshContainer,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofMeshData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMeshContainer* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***

Puntero a un contenedor de malla. Vea [**D3DXMESHCONTAINER.**](d3dxmeshcontainer.md)

</dd> <dt>

*pXofSave* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Puntero a un objeto de guardado de archivo .x. Use el puntero para llamar a [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) para agregar un objeto de datos secundario. No guarde los datos con [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*pXofMeshData* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Puntero a un nodo de datos de archivo .x. Use el puntero para llamar a [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) para agregar un objeto de datos secundario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Los valores devueltos de este método los implementa un programador de aplicaciones. En general, si no se produce ningún error, programe el método para devolver D3D \_ OK. De lo contrario, programe el método para devolver un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también devuelva el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
