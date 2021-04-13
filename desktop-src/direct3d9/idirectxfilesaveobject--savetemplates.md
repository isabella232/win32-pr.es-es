---
description: Guarda las plantillas en un archivo de DirectX. En desuso.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'IDirectXFileSaveObject:: SaveTemplates (método) (DXFile. h)'
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
ms.openlocfilehash: 3c63ae2e0f211aa8e7064161d03a66cafe1e8289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362533"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a>IDirectXFileSaveObject:: SaveTemplates (método)

Guarda las plantillas en un archivo de DirectX. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cTemplates* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número total de plantillas que se van a guardar.

</dd> <dt>

*ppguidTemplates* \[ de\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* \* const**

Dirección de un puntero a una matriz de los GUID de todas las plantillas que se van a guardar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Observaciones

El siguiente fragmento de código proporciona una llamada de ejemplo a **IDirectXFileSaveObject:: SaveTemplates** y el contenido de ejemplo de la matriz a la que apunta ppguidTemplates.


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



Después de usar este método para guardar las plantillas, use el método [**IDirectXFileSaveObject:: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para crear un objeto de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
