---
description: Generar automáticamente una tabla de contenido
ms.assetid: 3acb9c12-0158-4b89-87c4-4abd35ae8c2f
title: Generar automáticamente una tabla de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd6ec833302ff24e79582a5bf3ee500d715a69e9e74910bdf9b72a2f5a64f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958315"
---
# <a name="generating-a-table-of-contents-automatically"></a>Generar automáticamente una tabla de contenido

En este tema se muestra cómo usar el componente [**Generador**](/previous-versions/ee264297(v=vs.85)) de tablas de contenido (GENERADOR DE CONTENIDO) para generar automáticamente una tabla de contenido para un archivo de vídeo.

El generador de TOC es un objeto multimedia DirectX (DMO). Para usar el generador de TOC DMO, cree un gráfico de filtros de DirectX que tenga un archivo de vídeo como origen. Inserte el generador de TOC DMO en el gráfico de filtros y ejecute el gráfico. A continuación, puede obtener la tabla de contenido generada automáticamente desde el generador de TOC DMO.

El procedimiento siguiente proporciona los pasos con más detalle.

1.  Llame [**a CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un objeto Filter Graph (**CLSID \_ FilterGraph**) y obtener una [**interfaz IGraphBuilder.**](/windows/win32/api/strmif/nn-strmif-igraphbuilder)
2.  Llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un objeto DMO wrapper filter **(CLSID \_ DMOWrapperFilter)** y obtener una [**interfaz IDMOWrapperFilter.**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter)
3.  Pase **CLSID \_ CTocGeneratorDmo** al [**método Init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) del filtro DMO contenedor. Esto crea un generador de TOC DMO lo encapsula en el filtro DMO contenedor.
4.  Llame al [**método AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) de la [**interfaz IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) para agregar el generador de TOC encapsulado DMO al gráfico de filtros.
    > [!Note]  
    > [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) hereda de [**IFilterGraph.**](/windows/win32/api/strmif/nn-strmif-ifiltergraph)

     

5.  Llame al [**método AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) de la [**interfaz IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) para crear un filtro de souce y agregarlo al gráfico.
6.  Enumera los pines en el filtro DMO contenedor y el filtro de origen. Esto implica obtener [**interfaces IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) e [**interfaces IPin.**](/windows/win32/api/strmif/nn-strmif-ipin)
7.  Conectar el filtro de origen y el filtro contenedor llamando al [**método Conectar**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) de la [**interfaz IGraphBuilder.**](/windows/win32/api/strmif/nn-strmif-igraphbuilder)
8.  Complete el gráfico llamando al [**método Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) de la [**interfaz IGraphBuilder.**](/windows/win32/api/strmif/nn-strmif-igraphbuilder)
9.  Ejecute el grafo ([**IMediaControl::Run**](/windows/win32/api/control/nf-control-imediacontrol-run)) y espere a que se complete ([**IMediaEvent::WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).
10. Obtenga una [**interfaz IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) en el contenedor DMO filtro y obtenga el valor de la propiedad [**\_ \_ TOCGENERATOR TOCREADY de MFPKEY.**](/previous-versions/ee264297(v=vs.85)) Repita si es necesario hasta que la tabla de contenido esté lista.
11. Use la [**interfaz IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obtener el valor de la propiedad [**\_ TOCOBJECT TOCGENERATOR \_ de MFPKEY.**](/previous-versions/ee264297(v=vs.85)) Esta propiedad es una [**interfaz IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) que representa la tabla de contenido generada automáticamente.

El código siguiente muestra el procedimiento para generar automáticamente una tabla de contenido. El código usa tres funciones auxiliares [**(BuildGraph,**](buildgraph-method-for-generating-a-table-of-contents.md) [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md)y [**GetToc)**](gettoc-method-for-generating-a-table-of-contents.md)que se muestran en otras páginas de esta documentación.


```C++
#include <dshow.h>
#include <dmodshow.h>
#include <wmcodecdsp.h>
#include <dmoreg.h>
#include <propsys.h>
#include <propidl.h>
#include <initguid.h>

HRESULT GetToc(IDMOWrapperFilter* pWrap, IToc** ppToc);
HRESULT RunGraphAndWait(IGraphBuilder* pGraph);
HRESULT BuildGraph(IGraphBuilder* pGraph, IDMOWrapperFilter* pWrap);

WCHAR g_sourceFile[] = L"c:\\experiment\\Seattle.wmv";

void main()
{
   HRESULT hr = E_FAIL;
   hr = CoInitialize(NULL);

   if(SUCCEEDED(hr))
   {
      IGraphBuilder* pBuilder = NULL;
      hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
         IID_IGraphBuilder, (VOID**)&pBuilder);

      if(SUCCEEDED(hr))
      {
         IDMOWrapperFilter* pWrap = NULL;
         hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, CLSCTX_INPROC, 
            IID_IDMOWrapperFilter, (VOID**)&pWrap);

         if(SUCCEEDED(hr))
         {
            hr = pWrap->Init(CLSID_CTocGeneratorDmo, DMOCATEGORY_VIDEO_EFFECT); 

            if(SUCCEEDED(hr))
            {
               hr = BuildGraph(pBuilder, pWrap);

               if(SUCCEEDED(hr))
               {
                  hr = RunGraphAndWait(pBuilder);

                  if(SUCCEEDED(hr))
                  {
                     IToc* pToc = NULL;
                     hr = GetToc(pWrap, &pToc);

                     if(SUCCEEDED(hr))
                     {
                        // Inspect the table of contents by calling IToc methods.

                        pToc->Release();
                        pToc = NULL;
                     }
                  }
               }
            }

            pWrap->Release();
            pWrap = NULL;
         }

         pBuilder->Release();
         pBuilder = NULL;
      }

      CoUninitialize();
   }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Función BuildGraph para generar una tabla de contenido](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Función GetToc para generar una tabla de contenido](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Función RunGraphAndWait para generar una tabla de contenido](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Guía de programación del analizador de tabla de contenido](toc-parser-programming-guide.md)
</dt> </dl>

 

 
