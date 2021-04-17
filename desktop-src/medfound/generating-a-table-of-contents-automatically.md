---
description: Generar automáticamente una tabla de contenido
ms.assetid: 3acb9c12-0158-4b89-87c4-4abd35ae8c2f
title: Generar automáticamente una tabla de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22adc4d48ad7f4b1d89a446eb28c25d6011804a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705405"
---
# <a name="generating-a-table-of-contents-automatically"></a><span data-ttu-id="b98a8-103">Generar automáticamente una tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="b98a8-103">Generating a Table of Contents Automatically</span></span>

<span data-ttu-id="b98a8-104">En este tema se muestra cómo usar el componente [**generador de tablas de contenido**](/previous-versions/ee264297(v=vs.85)) (generador de TDC) para generar automáticamente una tabla de contenido para un archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b98a8-104">This topic demonstrates how to use [**Table of Contents Generator**](/previous-versions/ee264297(v=vs.85)) (TOC Generator) component to automatically generate a table of contents for a video file.</span></span>

<span data-ttu-id="b98a8-105">El generador de TDC es un objeto multimedia de DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="b98a8-105">TOC Generator is a DirectX Media Object (DMO).</span></span> <span data-ttu-id="b98a8-106">Para usar el generador de TDC DMO, cree un gráfico de filtros de DirectX que tenga un archivo de vídeo como origen.</span><span class="sxs-lookup"><span data-stu-id="b98a8-106">To use the TOC Generator DMO, build a DirectX filter graph that has a video file as its source.</span></span> <span data-ttu-id="b98a8-107">Inserte el generador de TDC DMO en el gráfico de filtros y ejecute el gráfico.</span><span class="sxs-lookup"><span data-stu-id="b98a8-107">Insert the TOC Generator DMO into the filter graph, and run the graph.</span></span> <span data-ttu-id="b98a8-108">A continuación, puede obtener la tabla de contenido generada automáticamente desde el generador de TDC DMO.</span><span class="sxs-lookup"><span data-stu-id="b98a8-108">You can then obtain the automatically generated table of contents from the TOC Generator DMO.</span></span>

<span data-ttu-id="b98a8-109">El siguiente procedimiento proporciona los pasos con más detalle.</span><span class="sxs-lookup"><span data-stu-id="b98a8-109">The following procedure gives the steps in more detail.</span></span>

1.  <span data-ttu-id="b98a8-110">Llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un objeto de gráfico de filtro (**CLSID \_ FilterGraph**) y obtener una interfaz [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="b98a8-110">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a Filter Graph object (**CLSID\_FilterGraph**) and obtain an [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
2.  <span data-ttu-id="b98a8-111">Llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un objeto de filtro contenedor de DMO (**CLSID \_ DMOWrapperFilter**) y obtener una interfaz [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) .</span><span class="sxs-lookup"><span data-stu-id="b98a8-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a DMO Wrapper Filter object (**CLSID\_DMOWrapperFilter**) and obtain an [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="b98a8-112">Pase **CLSID \_ CTocGeneratorDmo** al método [**init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) del filtro contenedor de DMO.</span><span class="sxs-lookup"><span data-stu-id="b98a8-112">Pass **CLSID\_CTocGeneratorDmo** to the [**Init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) method of your DMO wrapper filter.</span></span> <span data-ttu-id="b98a8-113">Esto crea un generador de TDC DMO y lo encapsula en el filtro de contenedor de DMO.</span><span class="sxs-lookup"><span data-stu-id="b98a8-113">This creates a TOC Generator DMO and wraps it in your DMO wrapper filter.</span></span>
4.  <span data-ttu-id="b98a8-114">Llame al método [**addFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) de la interfaz [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) para agregar el generador de TDC encapsulado DMO al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="b98a8-114">Call the [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to add the wrapped TOC Generator DMO to the filter graph.</span></span>
    > [!Note]  
    > <span data-ttu-id="b98a8-115">[**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) hereda de [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span><span class="sxs-lookup"><span data-stu-id="b98a8-115">[**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) inherits from [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span></span>

     

5.  <span data-ttu-id="b98a8-116">Llame al método [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) de la interfaz [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) para crear un filtro de un propio y agregarlo al gráfico.</span><span class="sxs-lookup"><span data-stu-id="b98a8-116">Call the [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to create a souce filter and add it to the graph.</span></span>
6.  <span data-ttu-id="b98a8-117">Enumere los pin en el filtro de contenedor de DMO y el filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="b98a8-117">Enumerate pins on the DMO wrapper filter and the source filter.</span></span> <span data-ttu-id="b98a8-118">Esto implica la obtención de interfaces de [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) y de [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="b98a8-118">This involves obtaining [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) interfaces and [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) interfaces.</span></span>
7.  <span data-ttu-id="b98a8-119">Conecte el filtro de origen y el filtro de contenedor mediante una llamada al método [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) de la interfaz [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="b98a8-119">Connect the source filter and the wrapper filter by calling the [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
8.  <span data-ttu-id="b98a8-120">Complete el gráfico llamando al método [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) de la interfaz [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="b98a8-120">Complete the graph by calling the [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
9.  <span data-ttu-id="b98a8-121">Ejecute el gráfico ([**IMediaControl:: Run**](/windows/win32/api/control/nf-control-imediacontrol-run)) y espere a que se complete ([**IMediaEvent:: WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span><span class="sxs-lookup"><span data-stu-id="b98a8-121">Run the graph ([**IMediaControl::Run**](/windows/win32/api/control/nf-control-imediacontrol-run)), and wait for it to complete ([**IMediaEvent::WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span></span>
10. <span data-ttu-id="b98a8-122">Obtenga una interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) en el contenedor de filtros de DMO y obtenga el valor de la propiedad [**MFPKEY \_ TOCGENERATOR \_ TOCREADY**](/previous-versions/ee264297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b98a8-122">Obtain an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface on your DMO filter wrapper, and get the value of the [**MFPKEY\_TOCGENERATOR\_TOCREADY**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="b98a8-123">Repita el procedimiento si es necesario hasta que la tabla de contenido esté lista.</span><span class="sxs-lookup"><span data-stu-id="b98a8-123">Repeat if necessary until the table of contents is ready.</span></span>
11. <span data-ttu-id="b98a8-124">Use la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obtener el valor de la propiedad [**MFPKEY de \_ TOCGENERATOR \_ TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b98a8-124">Use your [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to get the value of the [**MFPKEY\_TOCGENERATOR\_TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="b98a8-125">Esta propiedad es una interfaz [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) que representa la tabla de contenido generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b98a8-125">This property is an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface that represents the automatically generated table of contents.</span></span>

<span data-ttu-id="b98a8-126">En el código siguiente se muestra el procedimiento para generar automáticamente una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="b98a8-126">The following code demonstrates the procedure for generating a table of contents automatically.</span></span> <span data-ttu-id="b98a8-127">El código usa tres funciones auxiliares ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md)y [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) que se muestran en otras páginas de esta documentación.</span><span class="sxs-lookup"><span data-stu-id="b98a8-127">The code uses three helper functions ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md), and [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) that are shown on other pages of this documentation.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b98a8-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b98a8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b98a8-129">Función BuildGraph para generar una tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="b98a8-129">BuildGraph Function for Generating a Table of Contents</span></span>](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="b98a8-130">Función GetToc para generar una tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="b98a8-130">GetToc Function for Generating a Table of Contents</span></span>](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="b98a8-131">Función RunGraphAndWait para generar una tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="b98a8-131">RunGraphAndWait Function for Generating a Table of Contents</span></span>](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="b98a8-132">Guía de programación del analizador de tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="b98a8-132">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 
