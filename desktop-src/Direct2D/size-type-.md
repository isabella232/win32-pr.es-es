---
title: Función de tipo de tamaño (D2d1helper. h)
description: Crea una estructura de tamaño que almacena su ancho y alto mediante el tipo de datos especificado.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Size Type (función) Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490150"
---
# <a name="sizetype-function"></a><Type>Función size

Crea una estructura de tamaño que almacena su ancho y alto mediante el tipo de datos especificado.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a>Parámetros de plantilla



| Parámetro | Descripción                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| Tipo      | El tipo de datos utilizado para almacenar el ancho y el alto del tamaño. Los valores posibles son FLOAT y UINT32. |



 

## <a name="parameters"></a>Parámetros



| Parámetro | Descripción        |
|-----------|--------------------|
| width     | Ancho del tamaño.  |
| height    | Alto del tamaño. |



 

## <a name="return-value"></a>Valor devuelto

Tamaño que contiene el ancho y el alto especificados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Biblioteca<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| Archivo DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





