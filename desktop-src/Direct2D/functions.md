---
title: Funciones de Direct2D
description: Direct2D proporciona las siguientes funciones.
ms.assetid: 1a7ae962-9b70-442c-a676-f172a2d9bfd3
keywords:
- Direct2D, funciones
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 9cbe07a6c1054036030395ff965610919ee48a97
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104488494"
---
# <a name="direct2d-functions"></a>Funciones de Direct2D

Direct2D proporciona las siguientes funciones. Las funciones adicionales se definen en el [espacio de nombres D2D1](d2d1-namespace.md).

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**D2D1ComputeMaximumScaleFactor**](/windows/desktop/api/d2d1_2/nf-d2d1_2-d2d1computemaximumscalefactor) | Calcula el factor máximo por el que una transformación determinada puede expandir cualquier vector. |
| [**D2D1CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) | Crea un nuevo dispositivo Direct2D asociado al dispositivo DXGI proporcionado.  |
| [**D2D1CreateDeviceContext**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevicecontext) | Crea un nuevo contexto de dispositivo de Direct2D asociado a una superficie de DXGI.  |
| [**D2D1CreateFactory (D2D1_FACTORY_TYPE, REFIID, void \* \* )**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory-r1) | Crea un objeto de generador que se puede usar para crear recursos de Direct2D. |
| [**D2D1CreateFactory (D2D1_FACTORY_TYPE, REFIID, D2D1_FACTORY_OPTIONS \* , void \* \* )**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) | Crea un objeto de generador que se puede usar para crear recursos de Direct2D. |
| [**D2D1GetGradientMeshInteriorPointsFromCoonsPatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-d2d1getgradientmeshinteriorpointsfromcoonspatch) | Devuelve los puntos interiores de una revisión de malla de gradiente en función de los puntos que definen una revisión de Coons. |
| [**D2D1InvertMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1invertmatrix) | Intenta invertir la matriz especificada. |
| [**D2D1IsMatrixInvertible**](/windows/desktop/api/d2d1/nf-d2d1-d2d1ismatrixinvertible) | Indica si la matriz especificada se va a invertir. |
| [**D2D1MakeRotateMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makerotatematrix) | Crea una transformación de giro que gira en el ángulo especificado sobre el punto especificado. |
| [**D2D1MakeSkewMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makeskewmatrix) | Crea una transformación de sesgo que tiene el ángulo del eje x especificado, el ángulo del eje y y el punto central.  |
| [**operador \* (const D2D1\MATRIX\3X2\F&, const D2D1\MATRIX\3X2\F&)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-setproduct) | Multiplica dos matrices y devuelve el resultado. |
| [**BlobGetter**](blobgetter.md) | Llama a una devolución de llamada de captador de propiedad de función miembro para una propiedad de tipo de BLOB. |
| [**BlobSetter**](blobsetter.md) | Llama a una devolución de llamada del establecedor de propiedad de función miembro para una propiedad de tipo de BLOB. |
| [**DeducingBlobGetter**](deducingblobgetter.md) | Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del captador de propiedad de función miembro para una propiedad de tipo de BLOB. |
| [**DeducingBlobSetter**](deducingblobsetter.md) | Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del establecedor de la propiedad de función miembro para una propiedad de tipo BLOB. |
| [**DeducingStringGetter**](deducingstringgetter.md) | Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del captador de propiedad de función miembro para una propiedad de tipo cadena. |
| [**DeducingStringSetter**](deducingstringsetter.md) | Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del establecedor de la propiedad de función miembro para una propiedad de tipo cadena. |
| [**DeducingValueGetter**](deducingvaluegetter.md) | Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del captador de propiedad de función miembro para una propiedad de tipo de valor. |
| [**DeducingValueSetter**](deducingvaluesetter.md) | Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del establecedor de la propiedad de función miembro para una propiedad de tipo de valor. |
| [**GetType**](/previous-versions/windows/desktop/legacy/hh847962(v=vs.85)) | Recupera el tipo de la propiedad especificada. |
| [**StringGetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringgetter) | Llama a una devolución de llamada de captador de propiedad de función miembro para una propiedad de tipo cadena. |
| [**StringSetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringsetter) | Llama a una devolución de llamada del establecedor de propiedad de función miembro para una propiedad de tipo cadena. |
| [**ValueGetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuegetter) | Llama a una devolución de llamada del establecedor de propiedad de función miembro para una propiedad de tipo de valor. |
| [**ValueSetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuesetter) | Llama a una devolución de llamada del establecedor de propiedad de función miembro para una propiedad de tipo de valor. |
| [**D2D1ConvertColorSpace**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1convertcolorspace) | Convierte el color especificado de un ColorSpace en otro. |
| [**D2D1SinCos**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1sincos) | Devuelve el seno y el coseno de un ángulo. |
| [**D2D1Tan**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1tan) | Devuelve la tangente de un ángulo. |
| [**D2D1Vec3Length**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1vec3length) | Devuelve la longitud de un vector de tres dimensiones. |
| [**PD2D1\PROPERTY\GET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_get_function) | Obtiene una propiedad de un efecto. |
| [**PD2D1\PROPERTY\SET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_set_function) | Establece una propiedad en un efecto. |