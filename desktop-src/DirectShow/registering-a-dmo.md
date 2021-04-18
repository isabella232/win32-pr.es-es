---
description: Registro de DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Registro de DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686322"
---
# <a name="registering-a-dmo"></a>Registro de DMO

Para que los clientes puedan usar DMO, el CLSID debe estar registrado en el sistema del usuario. Esto se realiza a través de la función **DllRegisterServer** del archivo dll. Si utiliza el Active Template Library (ATL), el Asistente para ATL generará automáticamente esta función.

También puede registrar su DMO en una o varias categorías estándar de DMO. Esto permite a los clientes detectar su DMO mediante la función [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) . Las categorías se definen mediante GUID y se enumeran en la sección [identificadores GUID de DMO](dmo-guids.md).

El registro de un DMO en una categoría es opcional. Para ello, llame a la función [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) y especifique el nombre descriptivo de DMO, el CLSID y la categoría. Opcionalmente, también puede registrar un conjunto de tipos de medios que admita su DMOs. Para obtener más información, consulte [tipos de medios de DMO](dmo-media-types.md).

En el ejemplo siguiente se muestra cómo registrar un efecto de audio DMO que admite entrada y salida de audio PCM. En este caso, los tipos de entrada y de salida son los mismos.


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



En este ejemplo se da por supuesto que ATL se ha usado para crear el proyecto; la última línea de la función llama al método ATL estándar para registrar el servidor COM. Si no usa ATL, la función tendrá un aspecto diferente.

**Anulación del registro de DMO**

La función **DllUnregisterServer** debe quitar las entradas del registro que crea la función **DllRegisterServer** . Si llama a **DMORegister** al registrar DMO, debe [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) con la misma categoría al anular el registro de DMO.

En el ejemplo siguiente se quitan las entradas del registro creadas en el ejemplo anterior:


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



**Valores de méritos de DirectShow**

A efectos de la generación de gráficos de filtros, DirectShow asigna un valor de mérito predeterminado a DMOs. Puede invalidar este valor agregando una entrada del registro a la clave del registro de DMO en el \_ CLSID raíz de las clases HKEY \_ \\ . Incluya un valor **DWORD** denominado `Merit` cuyo valor especifique el mérito.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritura de DMO](writing-a-dmo.md)
</dt> </dl>

 

 



