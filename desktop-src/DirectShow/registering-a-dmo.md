---
description: Registro de un DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Registro de un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5635f7b05edb13da80adb62104db5c412fa55608ec2f9b5214380b7d9a095e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904545"
---
# <a name="registering-a-dmo"></a>Registro de un DMO

Para que los clientes usen su DMO, el CLSID debe estar registrado en el sistema del usuario. Esto se realiza a través de la función **DllRegisterServer del** archivo DLL. Si usa el Active Template Library ATL, el asistente atl genera automáticamente esta función.

También puede registrar sus DMO en una o varias categorías de DMO estándar. Esto permite a los clientes detectar DMO mediante la [**función DMOEnum.**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) Las categorías se definen mediante GUID y se enumeran en la sección DMO [GUID.](dmo-guids.md)

El registro de DMO en una categoría es opcional. Para ello, llame a la función [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) y especifique el nombre descriptivo del DMO, el CLSID y la categoría. Opcionalmente, también puede registrar un conjunto de tipos de medios que admiten las DDO. Para obtener más información, [vea DMO tipos de medios .](dmo-media-types.md)

En el ejemplo siguiente se muestra cómo registrar un efecto de audio DMO admite la entrada y salida de audio PCM. En este caso, los tipos de entrada y de salida son los mismos.


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



En este ejemplo se supone que se usó ATL para crear el proyecto; la última línea de la función llama al método ATL estándar para registrar el servidor COM. Si no usa ATL, la función tendrá un aspecto diferente.

**Anulación del registro de un DMO**

La **función DllUnregisterServer** debe quitar todas las entradas del Registro que cree la función **DllRegisterServer.** Si llama a **DMORegister** al registrar la DMO, debe [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) con la misma categoría al anular el registro de DMO.

En el ejemplo siguiente se quitan las entradas del Registro creadas en el ejemplo anterior:


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



**DirectShow Valores de los valores de los valores de**

Para la creación de gráficos de filtro, DirectShow asigna un valor de merececión predeterminado a las DDO. Puede invalidar este valor agregando una entrada del Registro a la DMO del Registro de HKEY \_ CLASSES \_ ROOT \\ CLSID. Incluya un **valor DWORD** `Merit` denominado cuyo valor especifica el valor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



