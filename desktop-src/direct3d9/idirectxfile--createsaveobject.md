---
description: Crea un objeto Save. En desuso.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: 'IDirectXFile:: CreateSaveObject (método) (DXFile. h)'
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
ms.openlocfilehash: 848010a1f701b39f5cc77a126272bc019ed01f4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670255"
---
# <a name="idirectxfilecreatesaveobject-method"></a>IDirectXFile:: CreateSaveObject (método)

Crea un objeto Save. En desuso.

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

*szFileName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre del archivo que se va a usar para guardar los datos.

</dd> <dt>

*dwFileFormat* \[ de\]
</dt> <dd>

Tipo: **[ **DXFILEFORMAT**](dxfile.md)**

Indica el formato que se va a utilizar al guardar el archivo de DirectX. Este valor puede ser una de las \_ marcas DXFILEFORMAT XXX en las [constantes DXFILE](dxfile.md). Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*ppSaveObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***

Dirección de un puntero a una interfaz [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) que representa el objeto guardado que se ha creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILE, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Observaciones

Después de usar este método, use los métodos de la interfaz [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) para crear objetos de datos y guardar plantillas o datos.

El valor predeterminado para el formato de archivo es DXFILEFORMAT \_ Binary. Los valores de formato de archivo se pueden combinar en un OR lógico para crear texto comprimido o archivos binarios comprimidos. Si se especifica un archivo como binario (0) y texto (1), se guardará como un archivo de texto porque no se puede distinguir el valor del valor de formato de archivo de texto (0 + 1 = 1). Si indica que el formato de archivo debe ser texto y comprimido, el archivo se escribirá primero como texto y se comprimirá. Sin embargo, los archivos de texto comprimidos no son tan eficaces como los archivos de texto binario, por lo que en la mayoría de los casos querrá indicar binario y comprimido. Si se establece un archivo que se va a comprimir sin especificar un formato, se generará un archivo comprimido binario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> <dt>

[**IDirectXFileSaveObject**](idirectxfilesaveobject.md)
</dt> </dl>

 

 
