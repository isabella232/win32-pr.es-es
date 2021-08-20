---
description: Se produce cuando InkRecognizerContext ha generado resultados del método BackgroundRecognize.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Evento InkRecognizerContext.Recognition (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f6c4799f3366003d14451a19a7bea19ea35aadcce9226f25f1fe80a14ab19e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966944"
---
# <a name="inkrecognizercontextrecognition-event"></a>Evento InkRecognizerContext.Recognition

Se produce cuando [**InkRecognizerContext**](inkrecognizercontext-class.md) ha generado resultados del [**método BackgroundRecognize.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)

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

*RecognizedString* \[ En\]
</dt> <dd>

Texto del resultado del reconocimiento con la mayor confianza.

Para obtener más información sobre el tipo de datos BSTR, vea [Usar la biblioteca COM](using-the-com-library.md).

</dd> <dt>

*CustomData* \[ En\]
</dt> <dd>

Objeto que contiene los datos personalizados para el resultado del reconocimiento.

Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).

</dd> <dt>

*RecognitionStatus* \[ En\]
</dt> <dd>

Estado del reconocimiento en el resultado del reconocimiento más reciente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

El comportamiento de la interfaz de programación de aplicaciones (API) es impredecible si intenta obtener acceso al objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) original desde el controlador de eventos de reconocimiento. No intente hacerlo. En su lugar, si necesita hacerlo, cree una marca y esta establezca en el controlador [de eventos Recognition.](ink-recognition.md) A continuación, puede sondear esa marca para determinar cuándo se deben cambiar las propiedades **InkRecognizerContext** fuera del controlador de eventos.

Este método de evento se define en la \_ interfaz IInkEvents. La \_ interfaz IInkEvents implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IRERecognition.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkRecognizerContext (clase)**](inkrecognizercontext-class.md)
</dt> <dt>

[**BackgroundRecognize (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[**InkRecognitionStatus (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[**Método Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**IInkRecognitionResult (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

