---
description: Guarda un objeto de datos y sus secundarios en un archivo .x en el disco.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: Método ID3DXFileSaveObject::Save (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566613"
---
# <a name="id3dxfilesaveobjectsave-method"></a>Método ID3DXFileSaveObject::Save

Guarda un objeto de datos y sus secundarios en un archivo .x en el disco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser el siguiente: D3DXFERR \_ BADOBJECT.

## <a name="remarks"></a>Observaciones

Una vez que este método se realiza correctamente, ya no se puede llamar a [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) e [**ID3DXFileSaveData::AddDataReference**](id3dxfilesavedata--adddatareference.md) hasta que se cree un nuevo objeto [**ID3DXFile.**](id3dxfile.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




