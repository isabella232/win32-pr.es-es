---
description: Incrustar una tabla de contenido en un archivo de vídeo
ms.assetid: 1546388a-7868-4411-be20-34d28becbe76
title: Incrustar una tabla de contenido en un archivo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8303082e454dde181de336ee0f64ff9d583312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153635"
---
# <a name="embedding-a-table-of-contents-in-a-video-file"></a><span data-ttu-id="d7dd6-103">Incrustar una tabla de contenido en un archivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="d7dd6-103">Embedding a Table of Contents in a Video File</span></span>

<span data-ttu-id="d7dd6-104">En este tema se muestra cómo crear una tabla de contenido (TDC) e incrustarla en un archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-104">This topic demonstrates how to create a table of contents (TOC) and embed it in a video file.</span></span> <span data-ttu-id="d7dd6-105">Para que el código de ejemplo sea breve, la tabla de contenido es muy sencilla. contiene solo una entrada y la entrada se rellena con un mínimo de información.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-105">To keep the example code short, the table of contents is very simple; it contains only one entry, and the entry is populated with a minimum of information.</span></span>

<span data-ttu-id="d7dd6-106">Para crear una tabla de contenido e incrustarla en un archivo, debe crear los cuatro objetos siguientes llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-106">To create a table of contents and embed it in a file, you must create the following four objects by calling **CoCreateInstance**.</span></span>

-   <span data-ttu-id="d7dd6-107">Entrada de TDC</span><span class="sxs-lookup"><span data-stu-id="d7dd6-107">TOC Entry</span></span>
-   <span data-ttu-id="d7dd6-108">Lista de entradas de TDC</span><span class="sxs-lookup"><span data-stu-id="d7dd6-108">TOC Entry List</span></span>
-   <span data-ttu-id="d7dd6-109">TABLA DE CONTENIDO</span><span class="sxs-lookup"><span data-stu-id="d7dd6-109">TOC</span></span>
-   <span data-ttu-id="d7dd6-110">Analizador de TDC</span><span class="sxs-lookup"><span data-stu-id="d7dd6-110">TOC Parser</span></span>

<span data-ttu-id="d7dd6-111">Los identificadores de clase de los objetos se proporcionan en los [identificadores de clase para el analizador de tabla de contenido](class-identifiers-for-toc-parser.md).</span><span class="sxs-lookup"><span data-stu-id="d7dd6-111">Class identifiers for the objects are given in [Class Identifiers for Table of Contents Parser](class-identifiers-for-toc-parser.md).</span></span>

<span data-ttu-id="d7dd6-112">En primer lugar, rellene la entrada de la TDC con información que describe una parte del archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-112">First populate the TOC entry with information that describes one portion of the video file.</span></span> <span data-ttu-id="d7dd6-113">Agregue la entrada de TDC a la lista de entradas de TDC y, a continuación, agregue la lista de entradas de TDC a la TDC.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-113">Add the TOC entry to the TOC entry list, and then add the TOC entry list to the TOC.</span></span> <span data-ttu-id="d7dd6-114">Por último, agregue la TDC al analizador de TDC, que proporciona la funcionalidad para insertar la TDC en el archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-114">Finally, add the TOC to the TOC parser, which provides the functionality for embedding the TOC in the video file.</span></span> <span data-ttu-id="d7dd6-115">La lista siguiente proporciona los pasos con más detalle.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-115">The following list gives the steps in more detail.</span></span>

1.  <span data-ttu-id="d7dd6-116">Cree un objeto de entrada de TDC y obtenga una interfaz [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) en él.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-116">Create a TOC Entry object and obtain an [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) interface on it.</span></span>
2.  <span data-ttu-id="d7dd6-117">Rellene una estructura de [**\_ \_ descriptor de entrada de TDC**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) y pásela a [**ITocEntry:: SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span><span class="sxs-lookup"><span data-stu-id="d7dd6-117">Populate a [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure and pass it to [**ITocEntry::SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span></span>
3.  <span data-ttu-id="d7dd6-118">Cree un objeto de lista de entradas de TDC y obtenga una interfaz [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) en él.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-118">Create a TOC Entry List object and obtain an [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) interface on it.</span></span>
4.  <span data-ttu-id="d7dd6-119">Agregue el objeto de entrada de TDC que creó en el paso 1 al objeto de lista de entradas de TDC llamando a [**ITocEntryList:: AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).</span><span class="sxs-lookup"><span data-stu-id="d7dd6-119">Add the TOC Entry object you created in step 1 to the TOC Entry List object by calling [**ITocEntryList::AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).</span></span>
5.  <span data-ttu-id="d7dd6-120">Cree un objeto TOC y obtenga una interfaz [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) en él.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-120">Create a TOC object and obtain an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface on it.</span></span>
6.  <span data-ttu-id="d7dd6-121">Agregue el objeto de lista de entradas de TDC que creó en el paso 3 al objeto TOC llamando a [**IToc:: AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).</span><span class="sxs-lookup"><span data-stu-id="d7dd6-121">Add the TOC Entry List object you created in step 3 to the TOC object by calling [**IToc::AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).</span></span>
7.  <span data-ttu-id="d7dd6-122">Cree un objeto de analizador de TDC y obtenga una interfaz [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) en él.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-122">Create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface on it.</span></span>
8.  <span data-ttu-id="d7dd6-123">Llame a [**ITocParser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) para inicializar el objeto de analizador de TDC y asociarlo a un archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-123">Call [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) to initialize the TOC Parser object and associate it with a video file.</span></span>
9.  <span data-ttu-id="d7dd6-124">Agregue el objeto TOC que creó en el paso 5 al objeto analizador de TDC llamando a [**ITocParser:: AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).</span><span class="sxs-lookup"><span data-stu-id="d7dd6-124">Add the TOC object you created in step 5 to the TOC Parser object by calling [**ITocParser::AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).</span></span>
10. <span data-ttu-id="d7dd6-125">Inserte la tabla de contenido en el archivo de vídeo llamando a [**ITocParser:: commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).</span><span class="sxs-lookup"><span data-stu-id="d7dd6-125">Embed the table of contents in the video file by calling [**ITocParser::Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).</span></span>

<span data-ttu-id="d7dd6-126">En el código siguiente se muestran los pasos indicados en la lista anterior.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-126">The following code demonstrates the steps given in the preceding list.</span></span>


```C++
#include <wmcodecdsp.h>
HRESULT InitTocParserAndCommit(IToc* pToc);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocEntry* pEntry = NULL;
      hr = CoCreateInstance(CLSID_CTocEntry, NULL, 
         CLSCTX_INPROC_SERVER, IID_ITocEntry, (VOID**)&pEntry); 

      if(SUCCEEDED(hr))
      {
         TOC_ENTRY_DESCRIPTOR tocDesc = {0};
         tocDesc.qwStartTime = 4; 
         tocDesc.qwEndTime = 8;
         pEntry->SetDescriptor(&tocDesc); // HRESULT ignored for simplicity.    
    
         ITocEntryList* pEntryList = NULL;
         hr = CoCreateInstance(CLSID_CTocEntryList, NULL, 
            CLSCTX_INPROC_SERVER, IID_ITocEntryList, (VOID**)&pEntryList);

         if(SUCCEEDED(hr))
         {
            pEntryList->AddEntryByIndex(0, pEntry); // HRESULT ignored.
      
            IToc* pToc = NULL;
            hr = CoCreateInstance(CLSID_CToc, NULL, 
               CLSCTX_INPROC_SERVER, IID_IToc, (VOID**)&pToc);

            if(SUCCEEDED(hr))
            {
               pToc->AddEntryListByIndex(0, pEntryList); // HRESULT ignored.
               hr = InitTocParserAndCommit(pToc);
            }
         }
      }
     
      CoUninitialize();
   }
}

HRESULT InitTocParserAndCommit(IToc* pToc)
{
   ITocParser* pTocParser = NULL;
   HRESULT hr = CoCreateInstance(CLSID_CTocParser, NULL, 
      CLSCTX_INPROC_SERVER, IID_ITocParser, (VOID**)&pTocParser);

   if(SUCCEEDED(hr))
   {
      hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

      if(SUCCEEDED(hr))
      {
         DWORD tocIndex = 0;
         hr = pTocParser->AddToc(TOC_POS_TOPLEVELOBJECT, pToc, &tocIndex);

         if(SUCCEEDED(hr))
         {
            hr = pTocParser->Commit();
         }
      }

      pTocParser->Release();
      pTocParser = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d7dd6-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7dd6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7dd6-128">Leer una tabla de contenido de un archivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="d7dd6-128">Reading a Table of Contents From a Video File</span></span>](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[<span data-ttu-id="d7dd6-129">Objetos de analizador de tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="d7dd6-129">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> <dt>

[<span data-ttu-id="d7dd6-130">Guía de programación del analizador de tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="d7dd6-130">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 



