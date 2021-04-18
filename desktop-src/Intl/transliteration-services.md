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
# <a name="transliteration-services"></a>Servicios de transliteración

Los servicios de transliteración de ELS asignan texto UTF-16 de un sistema de escritura a otro sistema de escritura. En realidad, cada servicio se aplica a un conjunto específico de scripts Unicode de entrada y salida, y la transliteración real es interna de la plataforma ELS. Opcionalmente, la aplicación puede enumerar los servicios disponibles para los scripts de entrada y salida específicos y seleccionar el servicio que requiera.

La plataforma mantiene los metadatos de los servicios de transliteración de ELS. Los metadatos de cada servicio proporcionan una descripción del servicio y enumeran los scripts de entrada y salida que admite el servicio. Los metadatos se representan mediante una estructura de [**\_ \_ información del servicio de asignación**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) recuperada por la función [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) .

## <a name="input-to-a-transliteration-service"></a>Entrada a un servicio transliteral

La entrada a un servicio transliteral es texto UTF-16 en un sistema de escritura.

## <a name="output-of-a-transliteration-service"></a>Salida de un servicio transliteral

La salida de un servicio transliteral es UTF-16 texto asignada a un segundo sistema de escritura. Si no hay ninguna asignación de transliteración adecuada disponible para un fragmento determinado del texto de entrada, el fragmento permanece inalterado.

## <a name="transliteration-service-operation"></a>Operación de servicio transliteral

Un servicio transliteral asigna texto Unicode de un script de entrada a un script de salida, carácter por carácter o término por término, según corresponda. La aplicación puede optar por obtener el servicio de transliteración específico de interés especificando los scripts de entrada y salida al llamar a [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)o proporcionando el GUID de servicio. Otra opción para la aplicación es enumerar todos los servicios de transliteración disponibles mediante la especificación de la categoría de servicio "transliteración" al llamar a **MappingGetServices**. En este caso, la aplicación llama a cada servicio y compara los resultados con el texto original para ver si los resultados han sido modificados por la operación de un servicio determinado.

La aplicación puede solicitar el reconocimiento de texto para un servicio de transliteración de ELS con una llamada a [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext). Cuando recibe la solicitud, el servicio transliteral asigna un búfer para que contenga los datos transliterales y, a continuación, realiza el reconocimiento de texto para cada punto de código de la cadena de entrada proporcionada por la aplicación.

> [!Note]  
> El texto original y el texto transliterado pueden tener longitudes diferentes.

 

## <a name="transliteration-service-guids"></a>GUID de servicio de transliteración

Los GUID de los servicios de transliteración se declaran en Elssrvc. h, tal como se muestra en el código siguiente.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los servicios lingüísticos extendidos](about-extended-linguistic-services.md)
</dt> </dl>

 

 



