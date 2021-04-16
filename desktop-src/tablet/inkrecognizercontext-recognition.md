---
description: Se produce cuando InkRecognizerContext ha generado resultados del método BackgroundRecognize.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Evento InkRecognizerContext. Recognition (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86da1a7470169f9f978e92a87f3e32f7e63acb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720680"
---
# <a name="inkrecognizercontextrecognition-event"></a>Evento InkRecognizerContext. Recognition

Se produce cuando [**InkRecognizerContext**](inkrecognizercontext-class.md) ha generado resultados del método [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) .

## <a name="syntax"></a>Sintaxis


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RecognizedString* \[ de\]
</dt> <dd>

El texto del resultado del reconocimiento con la mayor confianza.

Para obtener más información sobre el tipo de datos BSTR, vea el [uso de la biblioteca com](using-the-com-library.md).

</dd> <dt>

*CustomData* \[ de\]
</dt> <dd>

Objeto que contiene los datos personalizados para el resultado del reconocimiento.

Para obtener más información acerca de la estructura de variante, vea el [uso de la biblioteca com](using-the-com-library.md).

</dd> <dt>

*RecognitionStatus* \[ de\]
</dt> <dd>

El estado de reconocimiento en el resultado de reconocimiento más reciente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El comportamiento de la interfaz de programación de aplicaciones (API) es imprevisible si se intenta obtener acceso al objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) original desde el controlador de eventos de reconocimiento. No intente hacerlo. En su lugar, si necesita hacerlo, cree una marca y establézcala en el controlador de eventos de [reconocimiento](ink-recognition.md) . Después, puede sondear esa marca para determinar cuándo se deben cambiar las propiedades de **InkRecognizerContext** fuera del controlador de eventos.

Este método de evento se define en la \_ interfaz IInkEvents. La \_ interfaz IInkEvents implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IRERecognition.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> <dt>

[**Método BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[**Enumeración InkRecognitionStatus**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[**Recognize (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**Interfaz IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

