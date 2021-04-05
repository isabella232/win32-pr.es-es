---
description: Esta aplicación muestra cómo puede compilar una aplicación sencilla de reconocimiento de escritura a mano. Este programa crea un objeto InkCollector para habilitar la entrada de lápiz en la ventana y un objeto de contexto de reconocedor predeterminado.
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: Ejemplo de reconocimiento básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19679a6d1642a94ed813ba0428654b6e03009ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912357"
---
# <a name="basic-recognition-sample"></a>Ejemplo de reconocimiento básico

Esta aplicación muestra cómo puede compilar una aplicación sencilla de reconocimiento de *escritura a mano* .

Este programa crea un objeto [**InkCollector**](inkcollector-class.md) para habilitar la *entrada de lápiz* en la ventana y un objeto de contexto de *reconocedor* predeterminado. Al recibir el "Recognize" comando, que se desencadena desde el menú de la aplicación, los trazos de tinta recopilados se pasan al contexto del reconocedor. La mejor cadena de resultado se presenta en un cuadro de mensaje.

## <a name="creating-the-recognizercontext-object"></a>Crear el objeto RecognizerContext

En el procedimiento WndProc de la aplicación, cuando \_ se recibe el mensaje de creación de WM en el inicio, se crea un nuevo contexto de reconocedor que usa el reconocedor predeterminado. Este contexto se usa para todo el reconocimiento en la aplicación.


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



## <a name="recognizing-the-strokes"></a>Reconocimiento de los trazos

El comando Recognize se recibe cuando el usuario hace clic en el reconocedor. . El código obtiene un puntero a la entrada de lápiz [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (pIInkStrokes) fuera del objeto [**InkDisp**](inkdisp-class.md) y, a continuación, pasa el **InkStrokes** al contexto del reconocedor mediante una llamada a los \_ trazos de putref.


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



A continuación, el código llama al método [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) del objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) y pasa un puntero a un objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) para almacenar los resultados.


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



Finalmente, el código usa la propiedad de [**cadena**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) del objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) recuperar el resultado de reconocimiento superior en una variable de cadena, libera el objeto **IInkRecognitionResult** y muestra la cadena en un cuadro de mensaje.


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



 

 
