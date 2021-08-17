---
description: Permite realizar el reconocimiento de entrada de lápiz, recuperar el resultado del reconocimiento y recuperar alternativas. InkRecognizerContext permite que los distintos reconocedores instalados en un sistema usen el reconocimiento de entrada de lápiz para procesar la entrada adecuadamente.
ms.assetid: 2b39fd32-831d-4606-8600-b52aaa7ed882
title: Clase InkRecognizerContext (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerContext
- InkRecognizerContext.IInkRecognizerContext
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 781d1b440f1287b22d5c3ddf7ecf7132f7311fc5f48da5da20e4145717f65bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218406"
---
# <a name="inkrecognizercontext-class"></a>InkRecognizerContext (clase)

Permite realizar el reconocimiento de entrada de lápiz, recuperar el resultado del reconocimiento y recuperar alternativas. **InkRecognizerContext permite** que los distintos reconocedores instalados en un sistema usen el reconocimiento de entrada de lápiz para procesar la entrada de forma adecuada.

**InkRecognizerContext** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Eventos

La **clase InkRecognizerContext** tiene estos eventos.



| Evento                                                                               | Descripción                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reconocimiento**](inkrecognizercontext-recognition.md)                             | Se produce cuando InkRecognizerContext ha generado resultados del método BackgroundRecognize.<br/>                                                                                             |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Se produce cuando **InkRecognizerContext** ha generado resultados después de llamar al [**método BackgroundRecognizeWithAlternates.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)<br/> |



 

### <a name="interfaces"></a>Interfaces

La **clase InkRecognizerContext** define estas interfaces.



| Interfaz                 | Descripción                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkRecognizerContext** | Este objeto implementa la **interfaz COM IInkRecognizerContext.**<br/> |



 

### <a name="methods"></a>Métodos

La **clase InkRecognizerContext** tiene estos métodos.



| Método                                                                                              | Descripción                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)                             | Especifica que el reconocedor debe reconocer los trazos asociados y se debe abrir un [**evento Recognition**](inkrecognizercontext-recognition.md) cuando se complete el reconocimiento.<br/>                                                                |
| [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) | Especifica que el reconocedor debe reconocer los trazos asociados y debe abrir un [**evento RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) cuando se complete el reconocimiento.<br/>                                    |
| [**Clon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                                                      | Crea un **objeto InkRecognizerContext duplicado.**<br/>                                                                                                                                                                                               |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)                                             | Finaliza la entrada de entrada de **lápiz en InkRecognizerContext.**<br/>                                                                                                                                                                                             |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)                                 | Indica si el diccionario del sistema, el diccionario de usuarios o la [**lista de palabras**](inkwordlist-class.md) contienen una cadena especificada.<br/>                                                                                                             |
| [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)                                                 | Realiza el reconocimiento en una [**colección InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) y devuelve los resultados del reconocimiento.<br/>                                                                                                                          |
| [**StopBackgroundRecognition**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition)                 | Finaliza el reconocimiento en segundo plano que se inició con una llamada a [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) o [**BackgroundRecognizeWithAlternates.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)<br/> |



 

### <a name="properties"></a>Propiedades

La **clase InkRecognizerContext** tiene estas propiedades.



| Propiedad                                                                                   | Tipo de acceso           | Descripción                                                                                                                                                |
|:-------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)<br/> | Lectura/escritura<br/> | Obtiene o establece el modo autocompletar de caracteres, que determina cuándo se reconocen caracteres o palabras.<br/>                                         |
| [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)<br/>                                 | Lectura/escritura<br/> | Obtiene o establece el nombre de cadena del factoid utilizado por el **objeto InkRecognizerContext.**<br/>                                                        |
| [**Guía**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide)<br/>                                     | Lectura/escritura<br/> | Obtiene o establece [**inkRecognizerGuide que**](inkrecognizerguide-class.md) se va a usar para la entrada de lápiz.<br/>                                                   |
| [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext)<br/>                           | Lectura/escritura<br/> | Obtiene o establece los caracteres que están delante de [**la colección InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) en el **objeto InkRecognizerContext.**<br/> |
| [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags)<br/>               | Lectura/escritura<br/> | Obtiene o establece las marcas que especifican cómo el reconocedor interpreta la entrada de lápiz y determina la cadena de resultado.<br/>                                     |
| [**Reconocedor**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognizer)<br/>                           | Lectura/escritura<br/> | Obtiene o establece el [**objeto IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) utilizado por el **objeto InkRecognizerContext.**<br/>                                   |
| [**Trazos**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)<br/>                                 | Lectura/escritura<br/> | Obtiene o establece la [**colección InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) asociada al **objeto InkRecognizerContext.**<br/>                    |
| [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext)<br/>                           | Lectura/escritura<br/> | Obtiene o establece los caracteres que vienen después de [**la colección InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) en el **objeto InkRecognizerContext.**<br/>  |
| [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)<br/>                               | Lectura/escritura<br/> | Obtiene o establece el [**objeto InkWordList**](inkwordlist-class.md) que se usa para mejorar los resultados del reconocimiento.<br/>                               |



 

## <a name="remarks"></a>Comentarios

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

Hay dos tipos de reconocimiento: fondo (asincrónico) o primer plano (sincrónico). El reconocimiento en segundo plano se inicia mediante una llamada a los métodos [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) o [**BackgroundRecognizeWithAlternates,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) se produce en un subproceso en segundo plano e informa de los resultados a la aplicación a través de un mecanismo de evento. El reconocimiento en primer plano no se devuelve hasta que se completa todo el reconocimiento, lo que hace que los resultados del reconocimiento estén disponibles para el subproceso que realiza la llamada sin escuchar el evento de reconocimiento.

La entrada manuscrita se procesa continuamente en segundo plano. Si se [**agrega un elemento IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) a la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) a la que hace referencia **InkRecognizerContext,** **IInkStrokeDisp** se reconoce inmediatamente. Consulte los comentarios en el tema [**sobre el método EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) para obtener más detalles.

Todo el reconocimiento se produce a través de un contexto de reconocedor. El contexto define la configuración de una sesión de reconocimiento única. Recibe la entrada de lápiz que se debe reconocer y define las restricciones en la entrada de lápiz y en la salida de reconocimiento. Las restricciones que se pueden establecer en el contexto incluyen el idioma, el diccionario y la gramática que se está utilizando.

> [!Note]  
> El establecimiento de propiedades que [**no son Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) o [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode) se realiza correctamente solo si la [colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) es **NULL.** Debe establecer las demás propiedades antes de adjuntar la colección InkStrokes a **InkRecognizerContext,** o bien debe establecer la colección InkStrokes en **NULL** y, a continuación, establecer las demás propiedades. Si establece la colección InkStrokes en **NULL** y, a continuación, establece las otras propiedades, es posible que tenga que volver a asociar la colección InkStrokes. Esto se debe a que el reconocimiento se inicia justo después de asignar InkStrokes a **InkRecognizerContext**. Cuando se realiza una llamada al método [**Recognize \[ \] InkRecognizeContext Class**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) o [**BackgroundRecognize,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)es posible que los resultados de la llamada ya estén disponibles.

 

Para mejorar el rendimiento de la aplicación, elimine el **objeto InkRecognizerContext** cuando ya no sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkRecognizer (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

