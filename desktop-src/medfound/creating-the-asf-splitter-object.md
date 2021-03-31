---
description: Crear el objeto divisor de ASF
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Crear el objeto divisor de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42c8033a0861102f6d66b22e43516a616d6428b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907572"
---
# <a name="creating-the-asf-splitter-object"></a><span data-ttu-id="88343-103">Crear el objeto divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="88343-103">Creating the ASF Splitter Object</span></span>

<span data-ttu-id="88343-104">El objeto de *separador* ASF es un objeto de capa WMContainer que analiza el objeto de datos ASF de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="88343-104">The ASF *splitter* object is a WMContainer layer object that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="88343-105">Para crear una nueva instancia del objeto divisor ASF, llame a la función [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="88343-105">To create a new instance of the ASF splitter object, call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function.</span></span> <span data-ttu-id="88343-106">Esta función devuelve un puntero a la interfaz [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) que representa un objeto divisor vacío.</span><span class="sxs-lookup"><span data-stu-id="88343-106">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface that represents an empty splitter object.</span></span>

<span data-ttu-id="88343-107">Antes de que el divisor pueda comenzar el análisis, la aplicación debe inicializar el divisor con información del objeto de encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="88343-107">Before the splitter can begin parsing, the application must initialize the splitter with information from the ASF Header Object.</span></span> <span data-ttu-id="88343-108">Para inicializar el divisor, llame al método [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) .</span><span class="sxs-lookup"><span data-stu-id="88343-108">To initialize the splitter, call the [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) method.</span></span> <span data-ttu-id="88343-109">Este método toma un puntero al [objeto ContentInfo de ASF](asf-contentinfo-object.md) que contiene la información de encabezado del archivo ASF que se va a analizar.</span><span class="sxs-lookup"><span data-stu-id="88343-109">This method takes a pointer to the [ASF ContentInfo Object](asf-contentinfo-object.md) that contains header information of the ASF file to parse.</span></span> <span data-ttu-id="88343-110">La aplicación debe inicializar el objeto ContentInfo antes de pasarlo al divisor para que la aplicación Conozca las características del archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="88343-110">The application must initialize the ContentInfo object before passing it to the splitter so that the characteristics of the media file are known to the application.</span></span> <span data-ttu-id="88343-111">El método **Initialize** del divisor extrae información de secuencia del objeto ContentInfo, como los números de secuencia, por lo que el divisor puede analizar los paquetes de datos.</span><span class="sxs-lookup"><span data-stu-id="88343-111">The splitter's **Initialize** method extracts stream information from the ContentInfo object, such as stream numbers, so the splitter can parse the data packets.</span></span>

### <a name="example"></a><span data-ttu-id="88343-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88343-112">Example</span></span>

<span data-ttu-id="88343-113">En el ejemplo de código siguiente se muestra cómo crear un divisor e inicializarlo con un objeto ContentInfo existente.</span><span class="sxs-lookup"><span data-stu-id="88343-113">The following code example shows how to create a splitter and initialize it with an existing ContentInfo object.</span></span>


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="88343-114">En este ejemplo se usa la función [SafeRelease](saferelease.md) para liberar punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="88343-114">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="88343-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88343-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88343-116">Divisor ASF</span><span class="sxs-lookup"><span data-stu-id="88343-116">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 



