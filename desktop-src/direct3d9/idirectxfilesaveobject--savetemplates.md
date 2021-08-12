---
description: Guarda las plantillas en un archivo DirectX. En desuso.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: Método IDirectXFileSaveObject::SaveTemplates (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 87ec95932b26877354c22089a97b249bd542aa841552c3e3f9e4827a20f6d608
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292226"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a>IDirectXFileSaveObject::SaveTemplates (método)

Guarda las plantillas en un archivo DirectX. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cTemplates* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número total de plantillas que se guardarán.

</dd> <dt>

*ppguidTemplates* \[ En\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* \* const**

Dirección de un puntero a una matriz de GUID para todas las plantillas que se guardarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método , el valor devuelto puede ser DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Comentarios

El fragmento de código siguiente proporciona una llamada de ejemplo a **IDirectXFileSaveObject::SaveTemplates** y el contenido de ejemplo de la matriz a la que apunta ppguidTemplates.


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



Después de usar este método para guardar las plantillas, use el método [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para crear un objeto de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
