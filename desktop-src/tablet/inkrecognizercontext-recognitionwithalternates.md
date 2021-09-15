---
description: Se produce cuando la clase InkRecognizerContext ha generado resultados después de llamar al método BackgroundRecognizeWithAlternates.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: Evento InkRecognizerContext.RecognitionWithAlternates (Msalterut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247760"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a>Evento InkRecognizerContext.RecognitionWithAlternates

Se produce cuando la [**clase InkRecognizerContext**](inkrecognizercontext-class.md) ha generado resultados después de llamar al método [**BackgroundRecognizeWithAlternates.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)

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

*RecognitionResult* \[ En\]
</dt> <dd>

Resultado del reconocimiento del evento.

</dd> <dt>

*CustomData* \[ En\]
</dt> <dd>

Datos personalizados para el resultado del reconocimiento.

Para obtener más información sobre la estructura VARIANT, vea [Using the COM Library](using-the-com-library.md).

</dd> <dt>

*RecognitionStatus* \[ En\]
</dt> <dd>

El estado de reconocimiento en el resultado del reconocimiento más reciente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El comportamiento de la interfaz de programación de aplicaciones (API) es impredecible si intenta obtener acceso al objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) original desde el controlador de eventos de reconocimiento. No intente hacerlo. En su lugar, si necesita hacerlo, cree una marca y esta establezca en el controlador [**de eventos Recognition.**](inkrecognizercontext-recognition.md) A continuación, puede sondear esa marca para determinar cuándo se deben cambiar las **propiedades InkRecognizerContext** fuera del controlador de eventos.

Este método de evento se define en la \_ interfaz IInkEvents. La \_ interfaz IInkEvents implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IRERecognitionWithAlternates.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkRecognizerContext (clase)**](inkrecognizercontext-class.md)
</dt> <dt>

[**Método BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[**Método Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**IInkRecognitionResult (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

