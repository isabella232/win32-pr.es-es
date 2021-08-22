---
description: No todas las aplicaciones requieren el uso del reconocimiento, pero como la mayoría de las aplicaciones se diseñaron con texto como tipo de datos principal, la capacidad de convertir la entrada de lápiz en texto es muy valiosa.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Reconocimiento de entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c3f1431aca97f41b4de9aef64108f3e619ef7b6f9239f46fdde9f7bf4ff3da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718304"
---
# <a name="ink-recognition"></a>Reconocimiento de entrada de lápiz

No todas las aplicaciones requieren el uso del reconocimiento, pero como la mayoría de las aplicaciones se diseñaron con texto como tipo de datos principal, la capacidad de convertir la entrada de lápiz en texto es muy valiosa. Puede usar las características de reconocimiento de la API de la plataforma tablet PC para consultar información sobre los motores de reconocimiento que están disponibles, como los idiomas que reconocen. A continuación, puede enviar una [**colección Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) desde un [**objeto Ink**](inkdisp-class.md) a un motor de reconocimiento y hacer que devuelva un [**objeto RecognitionResult.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)

## <a name="recognizercontext-object"></a>RecognizerContext (objeto)

Un [**objeto RecognizerContext**](inkrecognizercontext-class.md) es la creación de instancias de un reconocedor determinado. El **objeto RecognizerContext** permite reconocer una colección determinada de trazos de forma sincrónica o asincrónica. Al reconocer de forma asincrónica, **el objeto RecognizerContext** devuelve el objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) en una devolución de llamada de evento a la aplicación.

## <a name="recognizers-and-recognizer-objects"></a>Reconocedores y objetos de reconocedor

Una sola tableta PC puede tener uno o varios reconocedores disponibles. Puede consultar la colección del reconocedor para determinar qué reconocedor usar. Un reconocedor proporciona información específica sobre sus funcionalidades, como el lenguaje que puede reconocer y el fabricante.

Para determinar si hay al menos un reconocedor instalado, cree una instancia de un objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) como se muestra en los siguientes ejemplos de código de C++ \# y C. Si un reconocedor no está presente, se produce un error en esta llamada a [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)


```C++
CComPtr<IInkRecognizerContext> g_pIInkRecoContext;
hr = CoCreateInstance(CLSID_InkRecognizerContext, 
      NULL, CLSCTX_INPROC_SERVER,
      IID_IInkRecognizerContext, 
(void **) &g_pIInkRecoContext);
if (FAILED(hr)) 
{
      ::MessageBox(NULL, TEXT("No recognizers installed.\nExiting."), 
      gc_szAppName, MB_ICONERROR);
      return -1;
}
```




```CSharp
try
{
  Recognizers recos = new Recognizers();//Check for recognizer.
  Recognizer defReco = recos.GetDefaultRecognizer();
  recoContext = defReco.CreateRecognizerContext();
}
catch
{
  MessageBox.Show("No recognizers installed.");
}
```



## <a name="recognitionresult-and-recognitionalternate-objects"></a>Objetos RecognitionResult y RecognitionAlternate

Los resultados del reconocimiento se devuelven en un [**objeto RecognitionResult.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) Los resultados contienen una cadena de mejor resultado en [la propiedad TopString,](/previous-versions/ms829602(v=msdn.10)) así como una colección de resultados alternativos en una [**colección RecognitionAlternates.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) El **objeto RecognitionResult** se puede conservar con la colección [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) original desde la que se generó.

## <a name="recognizerguide-structure"></a>RecognizerGuide (estructura)

La guía del reconocedor puede constar de filas y columnas, y proporciona al reconocedor un contexto mejor en el que realizar el reconocimiento. Por ejemplo, puede dibujar líneas horizontales en la pantalla de un usuario, casi como un fragmento de papel, que muestran dónde debe producirse la escritura a mano (este tipo de guía constaría solo de filas y ninguna columna). Si un usuario escribe en las líneas, en lugar de algún espacio arbitrario, mejora la precisión del reconocimiento.

En la ilustración siguiente se muestra [**una estructura RecognizerGuide**](inkrecognizerguide-class.md) con dos líneas para la entrada.

![ilustración en la que se muestra la guía del reconocedor de dos líneas](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

En la ilustración siguiente se muestra [**una estructura RecognizerGuide**](inkrecognizerguide-class.md) con cuatro columnas y tres filas.

![ilustración en la que se muestra la guía de reconocedor de tres por cuatro](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

Para obtener más información sobre el uso [**de la estructura RecognizerGuide,**](inkrecognizerguide-class.md) vea el tema **de referencia de RecognizerGuide.**

 

 
