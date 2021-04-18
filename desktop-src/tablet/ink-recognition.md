---
description: No todas las aplicaciones requieren el uso del reconocimiento, pero como la mayoría de las aplicaciones se diseñaron con texto como su tipo de datos principal, la capacidad de convertir tinta en texto es muy valiosa.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Reconocimiento de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca4ec6f897c797d86df96c5d9c2cfd5d80f16c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569685"
---
# <a name="ink-recognition"></a>Reconocimiento de tinta

No todas las aplicaciones requieren el uso del reconocimiento, pero como la mayoría de las aplicaciones se diseñaron con texto como su tipo de datos principal, la capacidad de convertir tinta en texto es muy valiosa. Puede usar las características de reconocimiento de la API de la plataforma de Tablet PC para consultar información acerca de los motores de reconocimiento que están disponibles, por ejemplo, los idiomas que reconocen. Después, puede enviar una colección de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) de un objeto de [**entrada manuscrita**](inkdisp-class.md) a un motor de reconocimiento y hacer que devuelva un objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .

## <a name="recognizercontext-object"></a>RecognizerContext (objeto)

Un objeto [**RecognizerContext**](inkrecognizercontext-class.md) es la creación de instancias de un reconocedor determinado. El objeto **RecognizerContext** le permite reconocer una colección determinada de trazos de forma sincrónica o asincrónica. Al reconocer de forma asincrónica, el objeto **RecognizerContext** devuelve el objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) en una devolución de llamada de evento a la aplicación.

## <a name="recognizers-and-recognizer-objects"></a>Reconocedores y objetos de reconocedor

Un solo Tablet PC puede tener uno o más reconocedores disponibles. Puede consultar la colección del reconocedor para determinar el reconocedor que se va a usar. Un reconocedor proporciona información específica sobre sus capacidades, como el idioma que puede reconocer y el fabricante.

Para determinar si se ha instalado al menos un reconocedor, cree una instancia de un objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) como se muestra en los siguientes ejemplos de código de C++ y C \# . Si un reconocedor no está presente, se produce un error en esta llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .


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

Los resultados del reconocimiento se devuelven en un objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) . Los resultados contienen una mejor cadena de resultado en la propiedad de [cadena](/previous-versions/ms829602(v=msdn.10)) , así como una colección de resultados alternativos en una colección [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) . El objeto **RecognitionResult** se puede almacenar con la colección de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) original desde la que se generó.

## <a name="recognizerguide-structure"></a>Estructura RecognizerGuide

La guía del reconocedor puede constar de filas y columnas, y proporciona al reconocedor un contexto mejor en el que realizar el reconocimiento. Por ejemplo, puede dibujar líneas horizontales en la pantalla de un usuario, al igual que una pieza de papel, que muestran dónde se debe producir la escritura a mano (este tipo de guía solo consistiría en filas y no en columnas). Si un usuario escribe las líneas en lugar de un espacio arbitrario, mejora la precisión del reconocimiento.

En la ilustración siguiente se muestra una estructura [**RecognizerGuide**](inkrecognizerguide-class.md) con dos líneas de entrada.

![Ilustración en la que se muestra la guía de reconocimiento de dos líneas](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

En la ilustración siguiente se muestra una estructura [**RecognizerGuide**](inkrecognizerguide-class.md) con cuatro columnas y tres filas.

![Ilustración en la que se muestra la guía del reconocedor de tres por cuatro](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

Para obtener más información sobre el uso de la estructura [**RecognizerGuide**](inkrecognizerguide-class.md) , vea el tema de referencia de **RecognizerGuide** .

 

 
