---
title: Función de tipo Point2 (D2d1helper.h)
description: Crea un punto que almacena sus coordenadas utilizando el tipo de datos especificado.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Función de tipo Point2 Direct2D
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
ms.openlocfilehash: d925cc5676e6f0c9a8fb27a3ba2a12591ee87a5a72d5937e365fa57179e47ce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160381"
---
# <a name="point2type-function"></a>Point2 <Type> (Función)

Crea un punto que almacena sus coordenadas utilizando el tipo de datos especificado.

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
| Tipo      | Tipo de datos utilizado para almacenar la coordenada x e y del punto. Los valores posibles son FLOAT y UINT32. |



 

## <a name="parameters"></a>Parámetros



| Parámetro | Descripción                    |
|-----------|--------------------------------|
| x         | La coordenada x del punto. |
| y         | La coordenada y del punto. |



 

## <a name="return-value"></a>Valor devuelto

Punto que contiene la coordenada x y la coordenada Y especificadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y Platform Update for Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y Actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 aplicaciones \[ \| para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Biblioteca<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| Archivo DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





