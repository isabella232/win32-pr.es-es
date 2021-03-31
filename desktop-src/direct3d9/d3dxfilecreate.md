---
description: Crea una instancia de un objeto ID3DXFile.
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: Función D3DXFileCreate (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36fd57d15257323e86c0068709c3c73662eb0658
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157188"
---
# <a name="d3dxfilecreate-function"></a>D3DXFileCreate función)

Crea una instancia de un objeto [**ID3DXFile**](id3dxfile.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lplpDirectXFile* 
</dt> <dd>

Tipo: **[ **ID3DXFile**](id3dxfile.md)\*\***

Dirección de un puntero a una interfaz [**ID3DXFile**](id3dxfile.md) que representa el objeto de archivo. x creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: E \_ \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Después de usar esta función, use [**RegisterTemplates**](id3dxfile--registertemplates.md) o [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) para registrar plantillas, [**CreateEnumObject**](id3dxfile--createenumobject.md) para crear un objeto de enumerador o [**CreateSaveObject**](id3dxfile--createsaveobject.md) para crear un objeto de guardado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de archivo de D3DX X](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[**CreateEnumObject**](id3dxfile--createenumobject.md)
</dt> <dt>

[**CreateSaveObject**](id3dxfile--createsaveobject.md)
</dt> <dt>

[**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[**RegisterTemplates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




