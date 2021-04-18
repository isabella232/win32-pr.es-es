---
description: 'Las API de la plataforma de Tablet PC llaman a los métodos que debe implementar para crear un reconocedor de tinta y no directamente mediante una aplicación habilitada para tinta. En los pasos siguientes se representa una secuencia de llamada típica para la implementación de estos métodos: se carga el archivo DLL. Un&\# 160; Se crea el identificador HRECOGNIZER. Un&\# 160; Se crea el identificador HRECOCONTEXT. Las opciones y los modos del reconocedor se establecen para este contexto. Los trazos se agregan a los datos de tinta. La entrada está finalizada. Se reconoce la tinta. Se devuelven los resultados del reconocimiento. Se destruye el identificador de HRECOCONTEXT. Se destruye el identificador de HRECOGNIZER. La secuencia de llamada también se muestra en el siguiente esquema de código: C + + CreateRecognizer (CLSID, &HREC); while (más fragmentos de tinta para reconocer...) {//Cree un contexto, una vez por cada entrada de lápiz para que se reconozca HRC = CreateContext (HREC, &HRC);//funciones para configurar opciones y modos para este contexto SetGuide (HRC, pGuide, 0); SetFactoid (HRC, 5, teléfono); solo si se trata de una aplicación con Forms SetFlags (HRC, RECOFLAG \_ WORDMODE);//raro, solo si se desea el modo de palabra, ningún diccionario fuera del diccionario o una sola segmentación SetWordList (HRC, HWL),//agregar todos los trazos de este fragmento de entrada de lápiz mientras (más trazos...) {AddStroke (HRC, NULL, 800, pPacket, pXForm);//una llamada por trazo} EndInkInput (HRC); Esto obtiene el proceso reconocido de entrada manuscrita (HRC); Si se trata de una aplicación sencilla, llama a esta para un GetBestResultString de respuesta simple (HRC, longitud, búfer); Si se trata de una aplicación compleja, la llama para obtener una respuesta completa GetLatticePtr (HRC, &pLattice); Destruir el contexto DestroyContext (HRC); }//Se llama justo antes de que la aplicación cierre DestroyRecognizer (HREC);'
ms.assetid: 484ba140-788f-4b71-9cc7-9baa919d9936
title: Secuencia de llamada típica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832ea396c1d73748c4636d2cad5e17529b8d54df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706568"
---
# <a name="typical-calling-sequence"></a><span data-ttu-id="40cb7-103">Secuencia de llamada típica</span><span class="sxs-lookup"><span data-stu-id="40cb7-103">Typical Calling Sequence</span></span>

<span data-ttu-id="40cb7-104">Las API de la plataforma de Tablet PC llaman a los métodos que debe implementar para crear un reconocedor de tinta y no directamente mediante una aplicación habilitada para tinta.</span><span class="sxs-lookup"><span data-stu-id="40cb7-104">The methods you must implement to create an ink recognizer are called by the Tablet PC Platform APIs and not directly by an ink-enabled application.</span></span>

<span data-ttu-id="40cb7-105">En los pasos siguientes se representa una secuencia de llamada típica para la implementación de estos métodos:</span><span class="sxs-lookup"><span data-stu-id="40cb7-105">The following steps represent a typical calling sequence for the implementation of these methods:</span></span>

1.  <span data-ttu-id="40cb7-106">Se carga el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="40cb7-106">The DLL is loaded.</span></span>
2.  <span data-ttu-id="40cb7-107">Se crea un identificador [HRECOGNIZER](hrecognizer-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="40cb7-107">An [HRECOGNIZER](hrecognizer-handle.md) handle is created.</span></span>
3.  <span data-ttu-id="40cb7-108">Se crea un identificador [HRECOCONTEXT](hrecocontext-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="40cb7-108">An [HRECOCONTEXT](hrecocontext-handle.md) handle is created.</span></span>
4.  <span data-ttu-id="40cb7-109">Las opciones y los modos del reconocedor se establecen para este contexto.</span><span class="sxs-lookup"><span data-stu-id="40cb7-109">Recognizer options and modes are set for this context.</span></span>
5.  <span data-ttu-id="40cb7-110">Los trazos se agregan a los datos de tinta.</span><span class="sxs-lookup"><span data-stu-id="40cb7-110">Strokes are added to the ink data.</span></span>
6.  <span data-ttu-id="40cb7-111">La entrada está finalizada.</span><span class="sxs-lookup"><span data-stu-id="40cb7-111">Input is ended.</span></span>
7.  <span data-ttu-id="40cb7-112">Se reconoce la tinta.</span><span class="sxs-lookup"><span data-stu-id="40cb7-112">The ink is recognized.</span></span>
8.  <span data-ttu-id="40cb7-113">Se devuelven los resultados del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="40cb7-113">The recognition results are returned.</span></span>
9.  <span data-ttu-id="40cb7-114">Se destruye el identificador de [HRECOCONTEXT](hrecocontext-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="40cb7-114">The [HRECOCONTEXT](hrecocontext-handle.md) handle is destroyed.</span></span>
10. <span data-ttu-id="40cb7-115">Se destruye el identificador de [HRECOGNIZER](hrecognizer-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="40cb7-115">The [HRECOGNIZER](hrecognizer-handle.md) handle is destroyed.</span></span>

<span data-ttu-id="40cb7-116">La secuencia de llamada también se muestra en el siguiente esquema de código:</span><span class="sxs-lookup"><span data-stu-id="40cb7-116">The calling sequence is also illustrated in the following code outline:</span></span>


```C++
CreateRecognizer(CLSID, &hrec);
while (more pieces of ink to recognize ... )
{
  // Create a context, once per piece of ink to be recognized
  hrc = CreateContext(hrec, &hrc);

  // Functions to set up options and modes for this context
  SetGuide(hrc, pGuide, 0);
  SetFactoid(hrc, 5, PHONE); // only if in application with forms
  SetFlags(hrc, RECOFLAG_WORDMODE); // rare, only if wanting word mode, no out-of-dictionary, or single segmentation
  SetWordList(hrc, hwl);

  // Adding all the strokes in this piece of ink
  while (more strokes ... )
  {
    AddStroke(hrc, NULL, 800, pPacket, pXForm);  // one call per stroke
  }
  EndInkInput(hrc);

  // This gets the ink recognized
  Process(hrc);

  // If this is a simple application, it calls this for a simple answer
  GetBestResultString(hrc, length, buffer);

  // If this is a complex application, it calls this for a complete answer
  GetLatticePtr(hrc, &pLattice);

  // Destroy the context
  DestroyContext(hrc);
}
// Called just before the application shuts down
DestroyRecognizer(hrec);
```



## <a name="related-topics"></a><span data-ttu-id="40cb7-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40cb7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40cb7-118">API de reconocedor</span><span class="sxs-lookup"><span data-stu-id="40cb7-118">Recognizer APIs</span></span>](recognizer-apis.md)
</dt> <dt>

[<span data-ttu-id="40cb7-119">Arquitectura de la API de reconocimiento</span><span class="sxs-lookup"><span data-stu-id="40cb7-119">Recognition API Architecture</span></span>](recognition-api-architecture.md)
</dt> </dl>

 

 



