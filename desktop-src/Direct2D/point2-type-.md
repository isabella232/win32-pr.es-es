---
title: Point2 (función de tipo) (D2d1helper. h)
description: Crea un punto que almacena sus coordenadas con el tipo de datos especificado.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Point2 (función de tipo Direct2D)
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f614f49077ed198c5e85d17b9ee3c84a5e300670
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658244"
---
# <a name="point2type-function"></a>Point2 ( <Type> función)

Crea un punto que almacena sus coordenadas con el tipo de datos especificado.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a>Parámetros de plantilla



| Parámetro | Descripción                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| Tipo      | El tipo de datos utilizado para almacenar la coordenada x y la coordenada y del punto. Los valores posibles son FLOAT y UINT32. |



 

## <a name="parameters"></a>Parámetros



| Parámetro | Descripción                    |
|-----------|--------------------------------|
| x         | La coordenada x del punto. |
| y         | La coordenada y del punto. |



 

## <a name="return-value"></a>Valor devuelto

Un punto que contiene la coordenada x y la coordenada y especificadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Biblioteca<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| Archivo DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





