---
description: Leer una tabla de contenido de un archivo de vídeo
ms.assetid: 10c4f4ca-cb30-453c-b18d-0470bfecc14e
title: Leer una tabla de contenido de un archivo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d75d1101b2ad0a2ecd57dcf53acbe6a6e7d435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715503"
---
# <a name="reading-a-table-of-contents-from-a-video-file"></a><span data-ttu-id="8c213-103">Leer una tabla de contenido de un archivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="8c213-103">Reading a Table of Contents from a Video File</span></span>

<span data-ttu-id="8c213-104">En este tema se muestra cómo leer una tabla de contenido que ya se ha incrustado en un archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8c213-104">This topic demonstrates how to read a table of contents that has already been embedded in a video file.</span></span>

<span data-ttu-id="8c213-105">Empiece por llamar a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un objeto de analizador de TDC y obtener una interfaz [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) .</span><span class="sxs-lookup"><span data-stu-id="8c213-105">Start by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface.</span></span> <span data-ttu-id="8c213-106">A continuación, obtenga las siguientes interfaces llamando a los métodos.</span><span class="sxs-lookup"><span data-stu-id="8c213-106">Then obtain the following interfaces by calling methods.</span></span>

-   [<span data-ttu-id="8c213-107">**IToc**</span><span class="sxs-lookup"><span data-stu-id="8c213-107">**IToc**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [<span data-ttu-id="8c213-108">**ITocEntryList**</span><span class="sxs-lookup"><span data-stu-id="8c213-108">**ITocEntryList**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [<span data-ttu-id="8c213-109">**ITocEntry**</span><span class="sxs-lookup"><span data-stu-id="8c213-109">**ITocEntry**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

<span data-ttu-id="8c213-110">Use los métodos de [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) para inspeccionar una entrada individual en la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="8c213-110">Use the methods of [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) to inspect an individual entry in the table of contents.</span></span> <span data-ttu-id="8c213-111">Por ejemplo, puede inspeccionar el título, la hora de inicio y la hora de finalización de la entrada.</span><span class="sxs-lookup"><span data-stu-id="8c213-111">For example, you can inspect the title, the start time, and the end time of the entry.</span></span>

<span data-ttu-id="8c213-112">La lista siguiente proporciona los pasos con más detalle.</span><span class="sxs-lookup"><span data-stu-id="8c213-112">The following list gives the steps in more detail.</span></span>

1.  <span data-ttu-id="8c213-113">Llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un objeto de analizador de TDC y obtener una interfaz [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) en él.</span><span class="sxs-lookup"><span data-stu-id="8c213-113">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface on it.</span></span>
2.  <span data-ttu-id="8c213-114">Llame a [**ITocParser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) para inicializar el analizador de TDC y asociarlo a un archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8c213-114">Call [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) to initialize the TOC parser and associate it with a video file.</span></span>
3.  <span data-ttu-id="8c213-115">Obtenga una interfaz [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) llamando a [**ITocParser:: GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex).</span><span class="sxs-lookup"><span data-stu-id="8c213-115">Obtain an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface by calling [**ITocParser::GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex).</span></span>
4.  <span data-ttu-id="8c213-116">Obtenga una interfaz [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) llamando a [**IToc:: GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex).</span><span class="sxs-lookup"><span data-stu-id="8c213-116">Obtain an [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) interface by calling [**IToc::GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex).</span></span>
5.  <span data-ttu-id="8c213-117">Obtenga una interfaz [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) llamando a [**ITocEntryList:: GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex).</span><span class="sxs-lookup"><span data-stu-id="8c213-117">Obtain an [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) interface by calling [**ITocEntryList::GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex).</span></span>
6.  <span data-ttu-id="8c213-118">Asigna una estructura de [**\_ \_ descriptor de entrada de TDC**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="8c213-118">Allocate a [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure.</span></span>
7.  <span data-ttu-id="8c213-119">Rellene la estructura del [**\_ \_ descriptor de entrada de TDC**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) mediante una llamada a [**ITocEntry:: GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).</span><span class="sxs-lookup"><span data-stu-id="8c213-119">Populate the [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure by calling [**ITocEntry::GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).</span></span>

<span data-ttu-id="8c213-120">En el código siguiente se muestran los pasos descritos en la lista anterior.</span><span class="sxs-lookup"><span data-stu-id="8c213-120">The following code demonstrates the steps in the preceding list.</span></span>


```C++
#include <stdio.h>
#include <wmcodecdsp.h>

HRESULT ShowEntryInfo(ITocEntry* pEntry);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocParser* pTocParser = NULL;

      hr = CoCreateInstance(CLSID_CTocParser, NULL, CLSCTX_INPROC_SERVER, 
         IID_ITocParser, (VOID**)&pTocParser);  
      
      if(SUCCEEDED(hr))
      {  
         hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

         if(SUCCEEDED(hr))
         {
            IToc* pToc = NULL;
            hr = pTocParser->GetTocByIndex(TOC_POS_TOPLEVELOBJECT, 0, &pToc);

            if(SUCCEEDED(hr))
            {
               ITocEntryList* pEntryList = NULL;
               hr = pToc->GetEntryListByIndex(0, &pEntryList);

               if(SUCCEEDED(hr))
               {
                  ITocEntry* pEntry = NULL;
                  hr = pEntryList->GetEntryByIndex(0, &pEntry);

                  if(SUCCEEDED(hr))
                  {
                     hr = ShowEntryInfo(pEntry);
                     pEntry->Release();
                     pEntry = NULL;
                  }

                  pEntryList->Release();
                  pEntryList = NULL;
               }

               pToc->Release();
               pToc = NULL;
            }
         }

         pTocParser->Release();
         pTocParser = NULL;  
      }
                   
      CoUninitialize();
   }
}

HRESULT ShowEntryInfo(ITocEntry* pEntry)
{
   HRESULT hr = E_FAIL;

   TOC_ENTRY_DESCRIPTOR entryDesc = {0};
   hr = pEntry->GetDescriptor(&entryDesc);

   if(SUCCEEDED(hr))
   {
      printf_s("qwStartTime: %x\n", entryDesc.qwStartTime);
      printf_s("qwEndTime: %x\n", entryDesc.qwEndTime);
      printf_s("qwStartStartPacketOffset: %x\n", entryDesc.qwStartPacketOffset);
      printf_s("qwEndPacketOffset: %x\n", entryDesc.qwEndPacketOffset);
      printf_s("qwRepresentativeFrameTime: %x\n", entryDesc.qwRepresentativeFrameTime);
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="8c213-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c213-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c213-122">Incrustar una tabla de contenido en un archivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="8c213-122">Embedding a Table of Contents in a Video File</span></span>](embedding-a-table-of-contents-in-a-video-file.md)
</dt> <dt>

[<span data-ttu-id="8c213-123">Objetos de analizador de tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="8c213-123">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> <dt>

[<span data-ttu-id="8c213-124">Guía de programación del analizador de tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="8c213-124">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 
