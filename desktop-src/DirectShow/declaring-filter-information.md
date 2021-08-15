---
description: Declarar información de filtro
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Declarar información de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c22fb13b524bed56e8cc9d51e573f2729f843e56565db2793d1a8b4568af52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953204"
---
# <a name="declaring-filter-information"></a>Declarar información de filtro

El primer paso es declarar la información del filtro, si es necesario. DirectShow define las siguientes estructuras para describir filtros, pines y tipos de medios:



| Estructura                                               | Descripción             |
|---------------------------------------------------------|-------------------------|
| [**FILTRO DE \_ AMOVIESETUP**](amoviesetup-filter.md)       | Describe un filtro.     |
| [**PIN de \_ AMOVIESETUP**](amoviesetup-pin.md)             | Describe un pin.        |
| [**MEDIATYPE DE \_ AMOVIESETUP**](amoviesetup-mediatype.md) | Describe un tipo de medio. |



 

Estas estructuras están anidadas. La estructura FILTER de **AMOVEIESETUP \_** tiene un puntero a una matriz de estructuras pin de **\_ AMOVIESETUP** y cada una de ellas tiene un puntero a una matriz de estructuras **\_ MEDIATYPE de AMOVEIESETUP.** Juntas, estas estructuras proporcionan suficiente información para que la [**interfaz IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) busque un filtro. No son una descripción completa de un filtro. Por ejemplo, si el filtro crea varias instancias del mismo pin, debe declarar solo una estructura de PIN de [**AMOVIESETUP \_**](amoviesetup-pin.md) para ese pin. Además, no se requiere un filtro para admitir todas las combinaciones de tipos de medios que registra; ni es necesario registrar todos los tipos de medios que admite.

Declare las estructuras de configuración como variables globales dentro del archivo DLL. En el ejemplo siguiente se muestra un filtro con un pin de salida:


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



El nombre del filtro se declara como una variable global estática, porque se volverá a usar en otro lugar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de filtros DirectShow filtros](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



