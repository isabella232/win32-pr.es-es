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
# <a name="basic-recognition-sample"></a><span data-ttu-id="f03cc-103">Ejemplo de reconocimiento básico</span><span class="sxs-lookup"><span data-stu-id="f03cc-103">Basic Recognition Sample</span></span>

<span data-ttu-id="f03cc-104">Esta aplicación muestra cómo puede compilar una aplicación sencilla de reconocimiento de *escritura a mano* .</span><span class="sxs-lookup"><span data-stu-id="f03cc-104">This application demonstrates how you can build a simple *handwriting* recognition application.</span></span>

<span data-ttu-id="f03cc-105">Este programa crea un objeto [**InkCollector**](inkcollector-class.md) para habilitar la *entrada de lápiz* en la ventana y un objeto de contexto de *reconocedor* predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f03cc-105">This program creates an [**InkCollector**](inkcollector-class.md) object to *ink*-enable the window and a default *recognizer context* object.</span></span> <span data-ttu-id="f03cc-106">Al recibir el "Recognize"</span><span class="sxs-lookup"><span data-stu-id="f03cc-106">Upon receiving the "Recognize!"</span></span> <span data-ttu-id="f03cc-107">comando, que se desencadena desde el menú de la aplicación, los trazos de tinta recopilados se pasan al contexto del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="f03cc-107">command, fired from the application's menu, the collected ink strokes are passed to the recognizer context.</span></span> <span data-ttu-id="f03cc-108">La mejor cadena de resultado se presenta en un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f03cc-108">The best result string is presented in a message box.</span></span>

## <a name="creating-the-recognizercontext-object"></a><span data-ttu-id="f03cc-109">Crear el objeto RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="f03cc-109">Creating the RecognizerContext Object</span></span>

<span data-ttu-id="f03cc-110">En el procedimiento WndProc de la aplicación, cuando \_ se recibe el mensaje de creación de WM en el inicio, se crea un nuevo contexto de reconocedor que usa el reconocedor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f03cc-110">In the WndProc procedure for the application, when the WM\_CREATE message is received on startup, a new recognizer context that uses the default recognizer is created.</span></span> <span data-ttu-id="f03cc-111">Este contexto se usa para todo el reconocimiento en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f03cc-111">This context is used for all recognition in the application.</span></span>


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



## <a name="recognizing-the-strokes"></a><span data-ttu-id="f03cc-112">Reconocimiento de los trazos</span><span class="sxs-lookup"><span data-stu-id="f03cc-112">Recognizing the Strokes</span></span>

<span data-ttu-id="f03cc-113">El comando Recognize se recibe cuando el usuario hace clic en el reconocedor.</span><span class="sxs-lookup"><span data-stu-id="f03cc-113">The recognize command is received when the user clicks the Recognize!</span></span> <span data-ttu-id="f03cc-114">.</span><span class="sxs-lookup"><span data-stu-id="f03cc-114">menu item.</span></span> <span data-ttu-id="f03cc-115">El código obtiene un puntero a la entrada de lápiz [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (pIInkStrokes) fuera del objeto [**InkDisp**](inkdisp-class.md) y, a continuación, pasa el **InkStrokes** al contexto del reconocedor mediante una llamada a los \_ trazos de putref.</span><span class="sxs-lookup"><span data-stu-id="f03cc-115">The code gets a pointer to the ink [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (pIInkStrokes) off of the [**InkDisp**](inkdisp-class.md) object, and then passes the **InkStrokes** to the recognizer context using a call to putref\_Strokes.</span></span>


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



<span data-ttu-id="f03cc-116">A continuación, el código llama al método [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) del objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) y pasa un puntero a un objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) para almacenar los resultados.</span><span class="sxs-lookup"><span data-stu-id="f03cc-116">The code then calls the [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object, passing in a pointer to an [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object to hold the results.</span></span>


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



<span data-ttu-id="f03cc-117">Finalmente, el código usa la propiedad de [**cadena**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) del objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) recuperar el resultado de reconocimiento superior en una variable de cadena, libera el objeto **IInkRecognitionResult** y muestra la cadena en un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f03cc-117">Finally, the code uses the [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object's [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) property retrieve the top recognition result into a string variable, releases the **IInkRecognitionResult** object, and displays the string in a message box.</span></span>


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



<span data-ttu-id="f03cc-118">Asegúrese de restablecer el contexto del reconocedor entre los usos.</span><span class="sxs-lookup"><span data-stu-id="f03cc-118">Be sure to reset the recognizer context between usages.</span></span>


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



 

 
