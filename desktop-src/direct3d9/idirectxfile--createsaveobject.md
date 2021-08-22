---
description: Crea un objeto de guardado. En desuso.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: Método IDirectXFile::CreateSaveObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: c3646f54b1f232c6eec3e1b3d06441a8e6a7c090f784e3c4c016f7f1bcfc3b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491855"
---
# <a name="idirectxfilecreatesaveobject-method"></a>IDirectXFile::CreateSaveObject (método)

Crea un objeto de guardado. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szFileName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre del archivo que se usará para guardar datos.

</dd> <dt>

*dwFileFormat* \[ En\]
</dt> <dd>

Tipo: **[ **DXFILEFORMAT**](dxfile.md)**

Indica el formato que se usará al guardar el archivo DirectX. Este valor puede ser una de las marcas XXX de DXFILEFORMAT \_ en [constantes DXFILE](dxfile.md). Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*ppSaveObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***

Dirección de un puntero a una [**interfaz IDirectXFileSaveObject,**](idirectxfilesaveobject.md) que representa el objeto save creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILE, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Comentarios

Después de usar este método, use métodos de la [**interfaz IDirectXFileSaveObject**](idirectxfilesaveobject.md) para crear objetos de datos y guardar plantillas o datos.

El valor predeterminado para el formato de archivo es DXFILEFORMAT \_ BINARY. Los valores de formato de archivo se pueden combinar en un or lógico para crear archivos binarios comprimidos o de texto comprimido. Si se especifica un archivo como binario (0) y texto (1), se guardará como un archivo de texto porque el valor será indistinguible del valor de formato de archivo de texto (0 + 1 = 1). Si indica que el formato de archivo debe ser texto y comprimido, el archivo se escribirá primero como texto y, a continuación, se comprimirá. Sin embargo, los archivos de texto comprimidos no son tan eficaces como los archivos de texto binarios, por lo que en la mayoría de los casos querrá indicar binarios y comprimidos. Si se establece un archivo que se va a comprimir sin especificar un formato, se dará como resultado un archivo binario comprimido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> <dt>

[**IDirectXFileSaveObject**](idirectxfilesaveobject.md)
</dt> </dl>

 

 
