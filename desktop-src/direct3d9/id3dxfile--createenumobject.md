---
description: Crea un objeto enumerador que leerá un archivo. x.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'ID3DXFile:: CreateEnumObject (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718326"
---
# <a name="id3dxfilecreateenumobject-method"></a>ID3DXFile:: CreateEnumObject (método)

Crea un objeto enumerador que leerá un archivo. x.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pvSource* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

El origen de datos. Tener instaladas localmente una de las siguientes:

-   Un nombre de archivo
-   Una estructura [**D3DXF \_ FILELOADMEMORY**](d3dxf-fileloadmemory.md)
-   Una estructura [**D3DXF \_ FILELOADRESOURCE**](d3dxf-fileloadresource.md)

Dependiendo del valor de loadflags.

</dd> <dt>

*loadflags* \[ de\]
</dt> <dd>

Tipo: **[D3DXF \_ FILELOADOPTIONS](d3dxf.md)**

Valor que especifica el origen de los datos. Este valor puede ser una de las marcas [D3DXF \_ FILELOADOPTIONS](d3dxf.md) .

</dd> <dt>

*ppEnumObj* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Dirección de un puntero a una interfaz [**ID3DXFileEnumObject**](id3dxfileenumobject.md) que representa el objeto de enumerador creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADVALUE, D3DXFERR \_ Nº.

## <a name="remarks"></a>Observaciones

Después de usar este método, use uno de los métodos [**ID3DXFileEnumObject**](id3dxfileenumobject.md) para recuperar un objeto de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileEnumObject**](id3dxfileenumobject.md)
</dt> </dl>

 

 
