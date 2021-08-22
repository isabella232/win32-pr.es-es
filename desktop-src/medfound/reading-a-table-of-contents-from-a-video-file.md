---
description: Leer una tabla de contenido de un archivo de vídeo
ms.assetid: 10c4f4ca-cb30-453c-b18d-0470bfecc14e
title: Leer una tabla de contenido de un archivo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bee379b0c50263463b0aa56e7ebb86bba447e70ef94ff82a6ba89e025d450bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034943"
---
# <a name="reading-a-table-of-contents-from-a-video-file"></a>Leer una tabla de contenido de un archivo de vídeo

En este tema se muestra cómo leer una tabla de contenido que ya se ha insertado en un archivo de vídeo.

Empiece llamando a [**CoCreateInstance para**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) crear un objeto toc Parser y obtener una [**interfaz ITocParser.**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) A continuación, obtenga las interfaces siguientes mediante una llamada a métodos .

-   [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

Use los métodos de [**ITocEntry para**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) inspeccionar una entrada individual en la tabla de contenido. Por ejemplo, puede inspeccionar el título, la hora de inicio y la hora de finalización de la entrada.

En la lista siguiente se indican los pasos con más detalle.

1.  Llame [**a CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un objeto toc Parser y obtener una [**interfaz ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) en él.
2.  Llame [**a ITocParser::Init para**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) inicializar el analizador de TOC y asociarlo a un archivo de vídeo.
3.  Obtenga una [**interfaz IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) llamando a [**ITocParser::GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex).
4.  Obtenga una [**interfaz ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) llamando a [**IToc::GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex).
5.  Obtenga una [**interfaz ITocEntry llamando**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) a [**ITocEntryList::GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex).
6.  Asigne una [**estructura DESCRIPTOR \_ TOC ENTRY. \_**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor)
7.  Rellene la [**estructura DESCRIPTOR \_ TOC ENTRY \_**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) mediante una llamada a [**ITocEntry::GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).

En el código siguiente se muestran los pasos de la lista anterior.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Insertar una tabla de contenido en un archivo de vídeo](embedding-a-table-of-contents-in-a-video-file.md)
</dt> <dt>

[Tabla de objetos del analizador de contenido](toc-parser-objects.md)
</dt> <dt>

[Guía de programación del analizador de tabla de contenido](toc-parser-programming-guide.md)
</dt> </dl>

 

 
