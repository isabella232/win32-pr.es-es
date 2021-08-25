---
description: Crea un objeto save que se usará para guardar datos en un archivo .x.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: Método ID3DXFile::CreateSaveObject (D3DX9Xof.h)
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
ms.openlocfilehash: aaf9f884a651182429de20fe261a250c8c6567eacd99d635213682e4d755b79a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951615"
---
# <a name="id3dxfilecreatesaveobject-method"></a>Método ID3DXFile::CreateSaveObject

Crea un objeto save que se usará para guardar datos en un archivo .x.

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

*pData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al nombre del archivo que se usará para guardar datos.

</dd> <dt>

*flags* \[ En\]
</dt> <dd>

Tipo: **[D3DXF \_ FILESAVEOPTIONS](d3dxf.md)**

Valor que especifica el nombre del archivo en el que se guardarán los datos. Este valor puede ser una de las marcas [Opciones de guardado de](d3dxf.md) archivos.

</dd> <dt>

*dwFileFormat* \[ En\]
</dt> <dd>

Tipo: **[D3DXF \_ FILEFORMAT](d3dxf.md)**

Indica el formato que se usará al guardar el archivo .x. Este valor puede ser una de las [marcas formatos de](d3dxf.md) archivo. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*ppSaveObj* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Dirección de un puntero a una [**interfaz ID3DXFileSaveObject,**](id3dxfilesaveobject.md) que representa el objeto save creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Comentarios

Después de usar este método, use métodos de la [**interfaz ID3DXFileSaveObject**](id3dxfilesaveobject.md) para crear objetos de datos y guardar plantillas o datos.

Para el formato de archivo *guardado dwFileFormat,* se debe especificar [](d3dxf.md) una de las marcas binaria, binaria heredada o de texto en Formatos de archivo. El archivo se puede comprimir mediante la marca opcional D3DXF \_ FILEFORMAT \_ COMPRESSED.

Los valores de formato de archivo se pueden combinar en un or lógico para crear texto comprimido o archivos binarios comprimidos. Si indica que el formato de archivo debe ser texto y comprimido, el archivo se escribirá primero como texto y, a continuación, se comprimirá. Sin embargo, los archivos de texto comprimidos no son tan eficaces como los archivos de texto binarios. En la mayoría de los casos, por lo tanto, querrá indicar binario y comprimido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)
</dt> </dl>

 

 
