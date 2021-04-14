---
description: Registra plantillas personalizadas, dado un objeto de enumeración ID3DXFileEnumObject.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'ID3DXFile:: RegisterEnumTemplates (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 89a8b136bdc0e202fc87ba8fd4d7f013203814eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424447"
---
# <a name="id3dxfileregisterenumtemplates-method"></a>ID3DXFile:: RegisterEnumTemplates (método)

Registra plantillas personalizadas, dado un objeto de enumeración [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pEnum* \[ de\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***

Puntero a un objeto de enumeración [**ID3DXFileEnumObject**](id3dxfileenumobject.md) que contiene plantillas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.

Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Observaciones

Cuando se llama a este método, copia las plantillas almacenadas con ID3DXFileEnumObject, que representan el archivo, en el almacén de plantillas local del objeto [**ID3DXFile**](id3dxfile.md) .

Si no está disponible un puntero [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , llame al método [**RegisterTemplates**](id3dxfile--registertemplates.md) en su lugar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**RegisterTemplates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




