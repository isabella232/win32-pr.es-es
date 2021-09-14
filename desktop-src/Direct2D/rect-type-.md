---
title: Función de tipo Rect (D2d1helper.h)
description: Crea una estructura de rectángulo que almacena sus coordenadas utilizando el tipo de datos especificado.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Función de tipo Rect Direct2D
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5f56fd9cbcfd576a441d9199e7ec1114cfb9f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162617"
---
# <a name="rectlttypegt-function"></a>Función de &lt; tipo Rect &gt;

Crea una estructura de rectángulo que almacena sus coordenadas utilizando el tipo de datos especificado.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a>Parámetros de plantilla



| Parámetro | Descripción                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| Tipo      | Tipo de datos utilizado para almacenar las dimensiones del rectángulo. Los valores posibles **son FLOAT** **y UINT32.** |



 

## <a name="parameters"></a>Parámetros



| Parámetro | Descripción                                             |
|-----------|---------------------------------------------------------|
| izquierda      | Coordenada x de la esquina superior izquierda del rectángulo.  |
| top       | Coordenada y de la esquina superior izquierda del rectángulo.  |
| right     | Coordenada x de la esquina inferior derecha del rectángulo. |
| abajo    | Coordenada y de la esquina inferior derecha del rectángulo. |



 

## <a name="return-value"></a>Valor devuelto

Estructura de rectángulo que contiene las coordenadas especificadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y Actualización de plataforma para aplicaciones de escritorio Windows Vista \[ \| aplicaciones para UWP\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y Actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 aplicaciones \[ \| para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Biblioteca<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| Archivo DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





