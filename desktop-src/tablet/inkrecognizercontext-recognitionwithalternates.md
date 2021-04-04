---
description: Se produce cuando la clase InkRecognizerContext ha generado resultados después de llamar al método de método BackgroundRecognizeWithAlternates.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: Evento InkRecognizerContext. RecognitionWithAlternates (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277785"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a>Evento InkRecognizerContext. RecognitionWithAlternates

Se produce cuando la [**clase InkRecognizerContext**](inkrecognizercontext-class.md) ha generado resultados después de llamar al método de [**método BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) .

## <a name="syntax"></a>Sintaxis


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RecognitionResult* \[ de\]
</dt> <dd>

Resultado del reconocimiento del evento.

</dd> <dt>

*CustomData* \[ de\]
</dt> <dd>

Datos personalizados para el resultado del reconocimiento.

Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).

</dd> <dt>

*RecognitionStatus* \[ de\]
</dt> <dd>

El estado de reconocimiento en el resultado de reconocimiento más reciente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El comportamiento de la interfaz de programación de aplicaciones (API) es imprevisible si se intenta obtener acceso al objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) original desde el controlador de eventos de reconocimiento. No intente hacerlo. En su lugar, si necesita hacerlo, cree una marca y establézcala en el controlador de eventos de [**reconocimiento**](inkrecognizercontext-recognition.md) . Después, puede sondear esa marca para determinar cuándo se deben cambiar las propiedades de **InkRecognizerContext** fuera del controlador de eventos.

Este método de evento se define en la \_ interfaz IInkEvents. La \_ interfaz IInkEvents implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IRERecognitionWithAlternates.

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

[**Método BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[**Recognize (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**Interfaz IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

