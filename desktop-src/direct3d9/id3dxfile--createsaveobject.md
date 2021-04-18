---
description: Crea un objeto Save que se usará para guardar los datos en un archivo. x.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'ID3DXFile:: CreateSaveObject (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7c5b3de020ad50abfd8834aabbdc8e6e848d71d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718325"
---
# <a name="id3dxfilecreatesaveobject-method"></a>ID3DXFile:: CreateSaveObject (método)

Crea un objeto Save que se usará para guardar los datos en un archivo. x.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdata* \[ de\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al nombre del archivo que se va a usar para guardar los datos.

</dd> <dt>

*marcas* \[ de de\]
</dt> <dd>

Tipo: **[D3DXF \_ FILESAVEOPTIONS](d3dxf.md)**

Valor que especifica el nombre del archivo en el que se van a guardar los datos. Este valor puede ser una de las marcas de [opciones para guardar archivos](d3dxf.md) .

</dd> <dt>

*dwFileFormat* \[ de\]
</dt> <dd>

Tipo: **[D3DXF \_ FILEFORMAT](d3dxf.md)**

Indica el formato que se va a utilizar al guardar el archivo. x. Este valor puede ser una de las marcas de [formatos de archivo](d3dxf.md) . Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*ppSaveObj* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Dirección de un puntero a una interfaz [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) que representa el objeto guardado que se ha creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADVALUE, D3DXFERR \_ Nº.

## <a name="remarks"></a>Observaciones

Después de usar este método, use los métodos de la interfaz [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) para crear objetos de datos y guardar plantillas o datos.

Para el formato de archivo guardado *dwFileFormat*, se debe especificar una de las marcas binarias, binarias heredadas o de texto en [formatos de archivo](d3dxf.md) . El archivo se puede comprimir mediante el uso de la \_ marca D3DXF FILEFORMAT \_ comprimida opcional.

Los valores de formato de archivo se pueden combinar en un OR lógico para crear texto comprimido o archivos binarios comprimidos. Si indica que el formato de archivo debe ser texto y comprimido, el archivo se escribirá primero como texto y después se comprimirá. Sin embargo, los archivos de texto comprimidos no son tan eficaces como los archivos de texto binario; en la mayoría de los casos, por lo tanto, querrá indicar binario y comprimido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)
</dt> </dl>

 

 
