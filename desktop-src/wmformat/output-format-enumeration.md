---
title: Enumeración del formato de salida
description: Enumeración del formato de salida
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- SDK de Windows Media Format, enumeraciones de formato de salida
- Formato de sistemas avanzados (ASF), enumeraciones de formato de salida
- ASF (formato de sistemas avanzados), enumeraciones de formato de salida
- SDK de Windows Media Format, interfaz IWMReaderTypeNegotiation
- Advanced Systems Format (ASF), IWMReaderTypeNegotiation (interfaz)
- ASF (formato de sistemas avanzados), interfaz IWMReaderTypeNegotiation
- enumeraciones de formato de salida
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077270"
---
# <a name="output-format-enumeration"></a><span data-ttu-id="b7298-111">Enumeración del formato de salida</span><span class="sxs-lookup"><span data-stu-id="b7298-111">Output Format Enumeration</span></span>

<span data-ttu-id="b7298-112">Tanto el objeto lector como el objeto lector sincrónico se comunican con los códecs para enumerar los posibles formatos de salida de las secuencias comprimidas.</span><span class="sxs-lookup"><span data-stu-id="b7298-112">Both the reader object and the synchronous reader object communicate with the codecs to enumerate the possible output formats for compressed streams.</span></span> <span data-ttu-id="b7298-113">Cuando lee un archivo que contiene contenido comprimido con uno o varios de los códecs de Windows Media, puede examinar los posibles formatos de salida para elegir el que mejor se adapte a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="b7298-113">When you read a file containing content compressed with one or more of the Windows Media codecs, you can examine the possible output formats to choose the one that best suits your needs.</span></span> <span data-ttu-id="b7298-114">Para mayor comodidad, cada códec tiene un formato de salida predeterminado que se establece en el formato que se usa con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="b7298-114">For convenience, each codec has a default output format which is set to the most commonly used format.</span></span> <span data-ttu-id="b7298-115">Para obtener más información sobre la enumeración de salida, vea [trabajar con salidas](working-with-outputs.md).</span><span class="sxs-lookup"><span data-stu-id="b7298-115">For more information about output enumeration, see [Working with Outputs](working-with-outputs.md).</span></span>

<span data-ttu-id="b7298-116">Puede realizar determinados cambios en un formato de salida en función del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b7298-116">You can make certain changes to an output format depending upon the media type.</span></span> <span data-ttu-id="b7298-117">En el caso de las secuencias de vídeo, por ejemplo, puede cambiar el tamaño del marco y la profundidad de color.</span><span class="sxs-lookup"><span data-stu-id="b7298-117">For video streams, for example, you can change the frame size and color depth.</span></span> <span data-ttu-id="b7298-118">Los objetos de lectura admiten una interfaz para probar los cambios que realice en el formato de salida, denominado [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).</span><span class="sxs-lookup"><span data-stu-id="b7298-118">The reading objects both support an interface to test changes you make to the output format, called [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7298-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b7298-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7298-120">**Características de lectura de archivos**</span><span class="sxs-lookup"><span data-stu-id="b7298-120">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




