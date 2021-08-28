---
description: Registra plantillas personalizadas, dado un objeto de enumeración ID3DXFileEnumObject.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: Método ID3DXFile::RegisterEnumTemplates (D3DX9Xof.h)
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
ms.openlocfilehash: a7c63ed8c4a2c3a65a80ba18f1b0455111917e99dce2982eb7be1d85314b6541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630075"
---
# <a name="id3dxfileregisterenumtemplates-method"></a>Método ID3DXFile::RegisterEnumTemplates

Registra plantillas personalizadas, dado un [**objeto de enumeración ID3DXFileEnumObject.**](id3dxfileenumobject.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pEnum* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***

Puntero a un [**objeto de enumeración ID3DXFileEnumObject**](id3dxfileenumobject.md) que contiene plantillas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK .

Si se produce un error en el método, se devolverá el siguiente valor: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Comentarios

Cuando se llama a este método, copia las plantillas almacenadas con id3DXFileEnumObject, que representa el archivo, en el almacén de plantillas local del [**objeto ID3DXFile.**](id3dxfile.md)

Si un [**puntero ID3DXFileEnumObject**](id3dxfileenumobject.md) no está disponible, llame al [**método RegisterTemplates**](id3dxfile--registertemplates.md) en su lugar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**RegisterTemplates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




