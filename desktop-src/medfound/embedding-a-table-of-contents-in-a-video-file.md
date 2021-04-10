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
# <a name="embedding-a-table-of-contents-in-a-video-file"></a>Incrustar una tabla de contenido en un archivo de vídeo

En este tema se muestra cómo crear una tabla de contenido (TDC) e incrustarla en un archivo de vídeo. Para que el código de ejemplo sea breve, la tabla de contenido es muy sencilla. contiene solo una entrada y la entrada se rellena con un mínimo de información.

Para crear una tabla de contenido e incrustarla en un archivo, debe crear los cuatro objetos siguientes llamando a **CoCreateInstance**.

-   Entrada de TDC
-   Lista de entradas de TDC
-   TABLA DE CONTENIDO
-   Analizador de TDC

Los identificadores de clase de los objetos se proporcionan en los [identificadores de clase para el analizador de tabla de contenido](class-identifiers-for-toc-parser.md).

En primer lugar, rellene la entrada de la TDC con información que describe una parte del archivo de vídeo. Agregue la entrada de TDC a la lista de entradas de TDC y, a continuación, agregue la lista de entradas de TDC a la TDC. Por último, agregue la TDC al analizador de TDC, que proporciona la funcionalidad para insertar la TDC en el archivo de vídeo. La lista siguiente proporciona los pasos con más detalle.

1.  Cree un objeto de entrada de TDC y obtenga una interfaz [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) en él.
2.  Rellene una estructura de [**\_ \_ descriptor de entrada de TDC**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) y pásela a [**ITocEntry:: SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).
3.  Cree un objeto de lista de entradas de TDC y obtenga una interfaz [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) en él.
4.  Agregue el objeto de entrada de TDC que creó en el paso 1 al objeto de lista de entradas de TDC llamando a [**ITocEntryList:: AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).
5.  Cree un objeto TOC y obtenga una interfaz [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) en él.
6.  Agregue el objeto de lista de entradas de TDC que creó en el paso 3 al objeto TOC llamando a [**IToc:: AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).
7.  Cree un objeto de analizador de TDC y obtenga una interfaz [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) en él.
8.  Llame a [**ITocParser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) para inicializar el objeto de analizador de TDC y asociarlo a un archivo de vídeo.
9.  Agregue el objeto TOC que creó en el paso 5 al objeto analizador de TDC llamando a [**ITocParser:: AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).
10. Inserte la tabla de contenido en el archivo de vídeo llamando a [**ITocParser:: commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).

En el código siguiente se muestran los pasos indicados en la lista anterior.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Leer una tabla de contenido de un archivo de vídeo](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[Objetos de analizador de tabla de contenido](toc-parser-objects.md)
</dt> <dt>

[Guía de programación del analizador de tabla de contenido](toc-parser-programming-guide.md)
</dt> </dl>

 

 



