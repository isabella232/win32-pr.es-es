---
description: Crea un objeto enumerador que leerá un archivo .x.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: Método ID3DXFile::CreateEnumObject (D3DX9Xof.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964756"
---
# <a name="id3dxfilecreateenumobject-method"></a>Método ID3DXFile::CreateEnumObject

Crea un objeto enumerador que leerá un archivo .x.

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

*pvSource* \[ out\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

El origen de datos. Tener instaladas localmente una de las siguientes:

-   Un nombre de archivo
-   Una [**estructura \_ FILELOADMEMORY de D3DXF**](d3dxf-fileloadmemory.md)
-   Estructura [**\_ FILELOADRESOURCE de D3DXF**](d3dxf-fileloadresource.md)

Según el valor de loadflags.

</dd> <dt>

*loadflags* \[ En\]
</dt> <dd>

Tipo: **[D3DXF \_ FILELOADOPTIONS](d3dxf.md)**

Valor que especifica el origen de los datos. Este valor puede ser una de las marcas [ \_ FILELOADOPTIONS de D3DXF.](d3dxf.md)

</dd> <dt>

*ppEnumObj* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Dirección de un puntero a una [**interfaz ID3DXFileEnumObject,**](id3dxfileenumobject.md) que representa el objeto enumerador creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Observaciones

Después de usar este método, use uno de [**los métodos ID3DXFileEnumObject**](id3dxfileenumobject.md) para recuperar un objeto de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileEnumObject**](id3dxfileenumobject.md)
</dt> </dl>

 

 
