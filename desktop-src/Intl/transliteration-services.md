---
description: Los servicios de transliteración de ELS asignan texto UTF-16 de un sistema de escritura a otro sistema de escritura.
ms.assetid: 32e46c52-5c3c-4e22-8f4e-05286ee213ba
title: Servicios de transliteración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc00b96d56e6b05e70b352c81da0280e9ef35043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156581"
---
# <a name="transliteration-services"></a><span data-ttu-id="a39d2-103">Servicios de transliteración</span><span class="sxs-lookup"><span data-stu-id="a39d2-103">Transliteration Services</span></span>

<span data-ttu-id="a39d2-104">Los servicios de transliteración de ELS asignan texto UTF-16 de un sistema de escritura a otro sistema de escritura.</span><span class="sxs-lookup"><span data-stu-id="a39d2-104">The ELS transliteration services map UTF-16 text from one writing system to another writing system.</span></span> <span data-ttu-id="a39d2-105">En realidad, cada servicio se aplica a un conjunto específico de scripts Unicode de entrada y salida, y la transliteración real es interna de la plataforma ELS.</span><span class="sxs-lookup"><span data-stu-id="a39d2-105">Each service is really data applying to a specific set of input and output Unicode scripts, and the actual transliteration is internal to the ELS platform.</span></span> <span data-ttu-id="a39d2-106">Opcionalmente, la aplicación puede enumerar los servicios disponibles para los scripts de entrada y salida específicos y seleccionar el servicio que requiera.</span><span class="sxs-lookup"><span data-stu-id="a39d2-106">The application can optionally enumerate the available services for specific input and output scripts and select the service that it requires.</span></span>

<span data-ttu-id="a39d2-107">La plataforma mantiene los metadatos de los servicios de transliteración de ELS.</span><span class="sxs-lookup"><span data-stu-id="a39d2-107">The platform maintains metadata for the ELS transliteration services.</span></span> <span data-ttu-id="a39d2-108">Los metadatos de cada servicio proporcionan una descripción del servicio y enumeran los scripts de entrada y salida que admite el servicio.</span><span class="sxs-lookup"><span data-stu-id="a39d2-108">Metadata for each service provides a description of the service and lists the input and output scripts that the service supports.</span></span> <span data-ttu-id="a39d2-109">Los metadatos se representan mediante una estructura de [**\_ \_ información del servicio de asignación**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) recuperada por la función [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) .</span><span class="sxs-lookup"><span data-stu-id="a39d2-109">The metadata is represented by a [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure retrieved by the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function.</span></span>

## <a name="input-to-a-transliteration-service"></a><span data-ttu-id="a39d2-110">Entrada a un servicio transliteral</span><span class="sxs-lookup"><span data-stu-id="a39d2-110">Input to a Transliteration Service</span></span>

<span data-ttu-id="a39d2-111">La entrada a un servicio transliteral es texto UTF-16 en un sistema de escritura.</span><span class="sxs-lookup"><span data-stu-id="a39d2-111">The input to a transliteration service is UTF-16 text in one writing system.</span></span>

## <a name="output-of-a-transliteration-service"></a><span data-ttu-id="a39d2-112">Salida de un servicio transliteral</span><span class="sxs-lookup"><span data-stu-id="a39d2-112">Output of a Transliteration Service</span></span>

<span data-ttu-id="a39d2-113">La salida de un servicio transliteral es UTF-16 texto asignada a un segundo sistema de escritura.</span><span class="sxs-lookup"><span data-stu-id="a39d2-113">The output of a transliteration service is UTF-16 text mapped to a second writing system.</span></span> <span data-ttu-id="a39d2-114">Si no hay ninguna asignación de transliteración adecuada disponible para un fragmento determinado del texto de entrada, el fragmento permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="a39d2-114">If no appropriate transliteration mapping is available for any given chunk of the input text, the chunk remains unchanged.</span></span>

## <a name="transliteration-service-operation"></a><span data-ttu-id="a39d2-115">Operación de servicio transliteral</span><span class="sxs-lookup"><span data-stu-id="a39d2-115">Transliteration Service Operation</span></span>

<span data-ttu-id="a39d2-116">Un servicio transliteral asigna texto Unicode de un script de entrada a un script de salida, carácter por carácter o término por término, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="a39d2-116">A transliteration service maps Unicode text from an input script to an output script, character by character or term by term, as appropriate.</span></span> <span data-ttu-id="a39d2-117">La aplicación puede optar por obtener el servicio de transliteración específico de interés especificando los scripts de entrada y salida al llamar a [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)o proporcionando el GUID de servicio.</span><span class="sxs-lookup"><span data-stu-id="a39d2-117">The application can choose to obtain the specific transliteration service of interest by specifying input and output scripts when calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), or by providing the service GUID.</span></span> <span data-ttu-id="a39d2-118">Otra opción para la aplicación es enumerar todos los servicios de transliteración disponibles mediante la especificación de la categoría de servicio "transliteración" al llamar a **MappingGetServices**.</span><span class="sxs-lookup"><span data-stu-id="a39d2-118">Another option for the application is to enumerate all available transliteration services by specifying the service category "Transliteration" when calling **MappingGetServices**.</span></span> <span data-ttu-id="a39d2-119">En este caso, la aplicación llama a cada servicio y compara los resultados con el texto original para ver si los resultados han sido modificados por la operación de un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="a39d2-119">In this case, the application calls each service and compares the results with the original text to see if the results have been changed by the operation of a particular service.</span></span>

<span data-ttu-id="a39d2-120">La aplicación puede solicitar el reconocimiento de texto para un servicio de transliteración de ELS con una llamada a [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span><span class="sxs-lookup"><span data-stu-id="a39d2-120">The application can request text recognition for an ELS transliteration service with a call to [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span></span> <span data-ttu-id="a39d2-121">Cuando recibe la solicitud, el servicio transliteral asigna un búfer para que contenga los datos transliterales y, a continuación, realiza el reconocimiento de texto para cada punto de código de la cadena de entrada proporcionada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a39d2-121">When it receives the request, the transliteration service allocates a buffer to contain the transliterated data, and then performs text recognition for each code point in the input string supplied by the application.</span></span>

> [!Note]  
> <span data-ttu-id="a39d2-122">El texto original y el texto transliterado pueden tener longitudes diferentes.</span><span class="sxs-lookup"><span data-stu-id="a39d2-122">The original text and the transliterated text might have different lengths.</span></span>

 

## <a name="transliteration-service-guids"></a><span data-ttu-id="a39d2-123">GUID de servicio de transliteración</span><span class="sxs-lookup"><span data-stu-id="a39d2-123">Transliteration Service GUIDs</span></span>

<span data-ttu-id="a39d2-124">Los GUID de los servicios de transliteración se declaran en Elssrvc. h, tal como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="a39d2-124">The GUIDs for the transliteration services are declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {A3A8333B-F4FC-42f6-A0C4-0462FE7317CB}
static const GUID ELS_GUID_TRANSLITERATION_HANT_TO_HANS =
    { 0xA3A8333B, 0xF4FC, 0x42f6, { 0xA0, 0xC4, 0x04, 0x62, 0xFE, 0x73, 0x17, 0xCB } };

// {3CACCDC8-5590-42dc-9A7B-B5A6B5B3B63B}
static const GUID ELS_GUID_TRANSLITERATION_HANS_TO_HANT =
    { 0x3CACCDC8, 0x5590, 0x42dc, { 0x9A, 0x7B, 0xB5, 0xA6, 0xB5, 0xB3, 0xB6, 0x3B } };

// {D8B983B1-F8BF-4a2b-BCD5-5B5EA20613E1}
static const GUID ELS_GUID_TRANSLITERATION_MALAYALAM_TO_LATIN =
    { 0xD8B983B1, 0xF8BF, 0x4a2b, { 0xBC, 0xD5, 0x5B, 0x5E, 0xA2, 0x06, 0x13, 0xE1 } };

// {C4A4DCFE-2661-4d02-9835-F48187109803}
static const GUID ELS_GUID_TRANSLITERATION_DEVANAGARI_TO_LATIN =
    { 0xC4A4DCFE, 0x2661, 0x4d02, { 0x98, 0x35, 0xF4, 0x81, 0x87, 0x10, 0x98, 0x03 } };

// {3DD12A98-5AFD-4903-A13F-E17E6C0BFE01}
static const GUID ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN =
    { 0x3DD12A98, 0x5AFD, 0x4903, { 0xA1, 0x3F, 0xE1, 0x7E, 0x6C, 0x0B, 0xFE, 0x01 } };

// {F4DFD825-91A4-489f-855E-9AD9BEE55727}
static const GUID ELS_GUID_TRANSLITERATION_BENGALI_TO_LATIN =
    { 0xF4DFD825, 0x91A4, 0x489f, { 0x85, 0x5E, 0x9A, 0xD9, 0xBE, 0xE5, 0x57, 0x27 } };
```



## <a name="related-topics"></a><span data-ttu-id="a39d2-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a39d2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a39d2-126">Acerca de los servicios lingüísticos extendidos</span><span class="sxs-lookup"><span data-stu-id="a39d2-126">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



