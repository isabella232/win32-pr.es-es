---
description: Esta aplicación muestra cómo puede crear una aplicación de reconocimiento de escritura a mano simple. Este programa crea un objeto InkCollector para habilitar la ventana y un objeto de contexto de reconocedor predeterminado.
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: Ejemplo de reconocimiento básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf45aa7695866e1cf413ea42b7c377b07ea84984ecf2cc3f44da93ff868072d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111145"
---
# <a name="basic-recognition-sample"></a>Ejemplo de reconocimiento básico

Esta aplicación muestra cómo puede crear una aplicación de reconocimiento de escritura a *mano* simple.

Este programa crea un [**objeto InkCollector**](inkcollector-class.md) para *la entrada de* lápiz: habilita la ventana y un objeto de contexto de *reconocedor* predeterminado. Al recibir el mensaje "Recognize!" , desencadenado desde el menú de la aplicación, los trazos de lápiz recopilados se pasan al contexto del reconocedor. La cadena de mejor resultado se presenta en un cuadro de mensaje.

## <a name="creating-the-recognizercontext-object"></a>Creación del objeto RecognizerContext

En el procedimiento WndProc de la aplicación, cuando se recibe el mensaje WM CREATE al iniciarse, se crea un nuevo contexto de reconocedor que usa \_ el reconocedor predeterminado. Este contexto se usa para todo el reconocimiento en la aplicación.


```C++
case WM_CREATE:
{
    HRESULT hr;
    hr = CoCreateInstance(CLSID_InkRecognizerContext,
             NULL, CLSCTX_INPROC_SERVER, IID_IInkRecognizerContext,
             (void **) &g_pIInkRecoContext);
    if (FAILED(hr))
    {
        ::MessageBox(NULL, TEXT("There are no handwriting recognizers installed.\n"
            "You need to have at least one in order to run this sample.\nExiting."),
            gc_szAppName, MB_ICONERROR);
        return -1;
    }
  //...
```



## <a name="recognizing-the-strokes"></a>Reconocer los trazos

El comando recognize se recibe cuando el usuario hace clic en Reconocer. . El código obtiene un puntero a [**inkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (pIInkStrokes) fuera del objeto [**InkDisp**](inkdisp-class.md) y, a continuación, pasa **inkStrokes** al contexto del reconocedor mediante una llamada a putref \_ Strokes.


```C++
 case WM_COMMAND:
  //...
  else if (wParam == ID_RECOGNIZE)
  {
      // change cursor to the system's Hourglass
      HCURSOR hCursor = ::SetCursor(::LoadCursor(NULL, IDC_WAIT));
      // Get a pointer to the ink stroke collection
      // This collection is a snapshot of the entire ink object
      IInkStrokes* pIInkStrokes = NULL;
      HRESULT hr = g_pIInkDisp->get_Strokes(&pIInkStrokes);
      if (SUCCEEDED(hr)) 
      {
          // Pass the stroke collection to the recognizer context
          hr = g_pIInkRecoContext->putref_Strokes(pIInkStrokes);
          if (SUCCEEDED(hr)) 
          {
```



A continuación, el código llama al [**método Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) del objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) y pasa un puntero a un objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) para contener los resultados.


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



Por último, el código usa la propiedad [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) del objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) para recuperar el resultado de reconocimiento superior en una variable de cadena, libera el objeto **IInkRecognitionResult** y muestra la cadena en un cuadro de mensaje.


```C++
                  // Get the best result of the recognition 
                  BSTR bstrBestResult = NULL;
                  hr = pIInkRecoResult->get_TopString(&bstrBestResult);
                  pIInkRecoResult->Release();
                  pIInkRecoResult = NULL;

                  // Show the result string
                  if (SUCCEEDED(hr) && bstrBestResult)
                  {
                      MessageBoxW(hwnd, bstrBestResult, 
                                  L"Recognition Results", MB_OK);
                      SysFreeString(bstrBestResult);
                  }  }
        
```



Asegúrese de restablecer el contexto del reconocedor entre los usos.


```
              // Reset the recognizer context
              g_pIInkRecoContext->putref_Strokes(NULL);
          }
          pIInkStrokes->Release();
      }
      // restore the cursor
      ::SetCursor(hCursor);
  }
```



 

 
