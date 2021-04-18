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
# <a name="ink-recognition"></a><span data-ttu-id="55649-103">Reconocimiento de tinta</span><span class="sxs-lookup"><span data-stu-id="55649-103">Ink Recognition</span></span>

<span data-ttu-id="55649-104">No todas las aplicaciones requieren el uso del reconocimiento, pero como la mayoría de las aplicaciones se diseñaron con texto como su tipo de datos principal, la capacidad de convertir tinta en texto es muy valiosa.</span><span class="sxs-lookup"><span data-stu-id="55649-104">Not all applications require the use of recognition, but because most applications were designed with text as their primary data type, the ability to convert ink into text is very valuable.</span></span> <span data-ttu-id="55649-105">Puede usar las características de reconocimiento de la API de la plataforma de Tablet PC para consultar información acerca de los motores de reconocimiento que están disponibles, por ejemplo, los idiomas que reconocen.</span><span class="sxs-lookup"><span data-stu-id="55649-105">You can use the recognition features of the Tablet PC platform API to query for information about the recognition engines that are available, such as what languages they recognize.</span></span> <span data-ttu-id="55649-106">Después, puede enviar una colección de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) de un objeto de [**entrada manuscrita**](inkdisp-class.md) a un motor de reconocimiento y hacer que devuelva un objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .</span><span class="sxs-lookup"><span data-stu-id="55649-106">You can then send a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from an [**Ink**](inkdisp-class.md) object to a recognition engine and have it return a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span>

## <a name="recognizercontext-object"></a><span data-ttu-id="55649-107">RecognizerContext (objeto)</span><span class="sxs-lookup"><span data-stu-id="55649-107">RecognizerContext Object</span></span>

<span data-ttu-id="55649-108">Un objeto [**RecognizerContext**](inkrecognizercontext-class.md) es la creación de instancias de un reconocedor determinado.</span><span class="sxs-lookup"><span data-stu-id="55649-108">A [**RecognizerContext**](inkrecognizercontext-class.md) object is the instantiation of a given recognizer.</span></span> <span data-ttu-id="55649-109">El objeto **RecognizerContext** le permite reconocer una colección determinada de trazos de forma sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="55649-109">The **RecognizerContext** object enables you to recognize a given collection of strokes synchronously or asynchronously.</span></span> <span data-ttu-id="55649-110">Al reconocer de forma asincrónica, el objeto **RecognizerContext** devuelve el objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) en una devolución de llamada de evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="55649-110">When recognizing asynchronously, the **RecognizerContext** object returns the [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object in an event callback to the application.</span></span>

## <a name="recognizers-and-recognizer-objects"></a><span data-ttu-id="55649-111">Reconocedores y objetos de reconocedor</span><span class="sxs-lookup"><span data-stu-id="55649-111">Recognizers and Recognizer Objects</span></span>

<span data-ttu-id="55649-112">Un solo Tablet PC puede tener uno o más reconocedores disponibles.</span><span class="sxs-lookup"><span data-stu-id="55649-112">A single Tablet PC may have one or more recognizers available.</span></span> <span data-ttu-id="55649-113">Puede consultar la colección del reconocedor para determinar el reconocedor que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="55649-113">You can query the recognizer's collection to determine which recognizer to use.</span></span> <span data-ttu-id="55649-114">Un reconocedor proporciona información específica sobre sus capacidades, como el idioma que puede reconocer y el fabricante.</span><span class="sxs-lookup"><span data-stu-id="55649-114">A recognizer provides specific information about its capabilities such as the language it can recognize and the manufacturer.</span></span>

<span data-ttu-id="55649-115">Para determinar si se ha instalado al menos un reconocedor, cree una instancia de un objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) como se muestra en los siguientes ejemplos de código de C++ y C \# .</span><span class="sxs-lookup"><span data-stu-id="55649-115">To determine whether at least one recognizer is installed, instantiate an [**InkRecognizerContext**](inkrecognizercontext-class.md) object as shown in the following C++ and C\# code examples.</span></span> <span data-ttu-id="55649-116">Si un reconocedor no está presente, se produce un error en esta llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="55649-116">If a recognizer is not present, this call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails.</span></span>


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



## <a name="recognitionresult-and-recognitionalternate-objects"></a><span data-ttu-id="55649-117">Objetos RecognitionResult y RecognitionAlternate</span><span class="sxs-lookup"><span data-stu-id="55649-117">RecognitionResult and RecognitionAlternate Objects</span></span>

<span data-ttu-id="55649-118">Los resultados del reconocimiento se devuelven en un objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .</span><span class="sxs-lookup"><span data-stu-id="55649-118">The results of the recognition are returned in a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span> <span data-ttu-id="55649-119">Los resultados contienen una mejor cadena de resultado en la propiedad de [cadena](/previous-versions/ms829602(v=msdn.10)) , así como una colección de resultados alternativos en una colección [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) .</span><span class="sxs-lookup"><span data-stu-id="55649-119">The results contain a best result string in the [TopString](/previous-versions/ms829602(v=msdn.10)) property, as well as a collection of alternative results in a [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) collection.</span></span> <span data-ttu-id="55649-120">El objeto **RecognitionResult** se puede almacenar con la colección de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) original desde la que se generó.</span><span class="sxs-lookup"><span data-stu-id="55649-120">The **RecognitionResult** object can be persisted with the original [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from which it was generated.</span></span>

## <a name="recognizerguide-structure"></a><span data-ttu-id="55649-121">Estructura RecognizerGuide</span><span class="sxs-lookup"><span data-stu-id="55649-121">RecognizerGuide Structure</span></span>

<span data-ttu-id="55649-122">La guía del reconocedor puede constar de filas y columnas, y proporciona al reconocedor un contexto mejor en el que realizar el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="55649-122">The recognizer guide can consist of rows and columns, and gives the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="55649-123">Por ejemplo, puede dibujar líneas horizontales en la pantalla de un usuario, al igual que una pieza de papel, que muestran dónde se debe producir la escritura a mano (este tipo de guía solo consistiría en filas y no en columnas).</span><span class="sxs-lookup"><span data-stu-id="55649-123">For example, you can draw horizontal lines on a user's screen, almost like a ruled piece of paper, that show where handwriting should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="55649-124">Si un usuario escribe las líneas en lugar de un espacio arbitrario, mejora la precisión del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="55649-124">If a user writes on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="55649-125">En la ilustración siguiente se muestra una estructura [**RecognizerGuide**](inkrecognizerguide-class.md) con dos líneas de entrada.</span><span class="sxs-lookup"><span data-stu-id="55649-125">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with two lines for input.</span></span>

![Ilustración en la que se muestra la guía de reconocimiento de dos líneas](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

<span data-ttu-id="55649-127">En la ilustración siguiente se muestra una estructura [**RecognizerGuide**](inkrecognizerguide-class.md) con cuatro columnas y tres filas.</span><span class="sxs-lookup"><span data-stu-id="55649-127">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with four columns and three rows.</span></span>

![Ilustración en la que se muestra la guía del reconocedor de tres por cuatro](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

<span data-ttu-id="55649-129">Para obtener más información sobre el uso de la estructura [**RecognizerGuide**](inkrecognizerguide-class.md) , vea el tema de referencia de **RecognizerGuide** .</span><span class="sxs-lookup"><span data-stu-id="55649-129">For more information about using the [**RecognizerGuide**](inkrecognizerguide-class.md) structure, see the **RecognizerGuide** reference topic.</span></span>

 

 
