---
description: Crea una instancia de un objeto DirectXFile. En desuso.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: Función DirectXFileCreate (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 8ee1787941bbb902e6f0f50b082867aaf2f0a8bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964964"
---
# <a name="directxfilecreate-function"></a>Función DirectXFileCreate

Crea una instancia de un objeto DirectXFile. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lplpDirectXFile* 
</dt> <dd>

Tipo: **[ **LPDIRECTXFILE**](idirectxfile.md)\***

Dirección de un puntero a una [**interfaz IDirectXFile,**](idirectxfile.md) que representa el objeto DirectXFile creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Observaciones

Después de usar esta función, use [**RegisterTemplates**](idirectxfile--registertemplates.md) para registrar plantillas, [**CreateEnumObject para**](idirectxfile--createenumobject.md) crear un objeto enumerador o [**CreateSaveObject**](idirectxfile--createsaveobject.md) para crear un objeto save.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3dxof.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de archivo X](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[**CreateSaveObject**](idirectxfile--createsaveobject.md)
</dt> <dt>

[**RegisterTemplates**](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




