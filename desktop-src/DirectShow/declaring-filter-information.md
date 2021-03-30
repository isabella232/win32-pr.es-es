---
description: Declarar información de filtro
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Declarar información de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8975217f1b7746b26dc5dd16ce9f4e7f694f44bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806709"
---
# <a name="declaring-filter-information"></a>Declarar información de filtro

El primer paso consiste en declarar la información de filtro, si es necesario. DirectShow define las siguientes estructuras para describir los filtros, los pin y los tipos de medios:



| Estructura                                               | Descripción             |
|---------------------------------------------------------|-------------------------|
| [**filtro de AMOVIESETUP \_**](amoviesetup-filter.md)       | Describe un filtro.     |
| [**AMOVIESETUP \_ PIN**](amoviesetup-pin.md)             | Describe un código PIN.        |
| [**AMOVIESETUP \_ MEDIATYPE**](amoviesetup-mediatype.md) | Describe un tipo de medio. |



 

Estas estructuras están anidadas. La estructura de **\_ filtro AMOVEIESETUP** tiene un puntero a una matriz de estructuras **AMOVIESETUP \_ PIN** y cada una de ellas tiene un puntero a una matriz de estructuras **AMOVEIESETUP \_ MEDIATYPE** . En conjunto, estas estructuras proporcionan información suficiente para que la interfaz [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) busque un filtro. No se trata de una descripción completa de un filtro. Por ejemplo, si el filtro crea varias instancias del mismo pin, debe declarar solo una estructura de [**\_ PIN AMOVIESETUP**](amoviesetup-pin.md) para ese pin. Además, no es necesario que un filtro admita cada combinación de tipos de medios que registra. no es necesario para registrar todos los tipos de medios que admite.

Declare las estructuras de configuración como variables globales en el archivo DLL. En el ejemplo siguiente se muestra un filtro con un PIN de salida:


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



El nombre del filtro se declara como una variable global estática, porque se utilizará de nuevo en otro lugar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



