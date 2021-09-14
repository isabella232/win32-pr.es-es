---
description: Registro de un DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Registro de un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246440"
---
# <a name="registering-a-dmo"></a>Registro de un DMO

Para que los clientes usen la DMO, el CLSID debe estar registrado en el sistema del usuario. Esto se realiza a través de la **función DllRegisterServer del** archivo DLL. Si usa el Active Template Library (ATL), el asistente atl genera automáticamente esta función.

También puede registrar la aplicación DMO una o varias categorías de DMO estándar. Esto permite a los clientes detectar DMO mediante la [**función DMOEnum.**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) Las categorías se definen mediante GUID y se enumeran en la sección DMO [GUID.](dmo-guids.md)

El registro de DMO en una categoría es opcional. Para ello, llame a la función [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) y especifique el nombre descriptivo del DMO, clsid y categoría. Opcionalmente, también puede registrar un conjunto de tipos de medios que admiten las DDO. Para obtener más información, [vea DMO tipos de medios .](dmo-media-types.md)

En el ejemplo siguiente se muestra cómo registrar un efecto de audio DMO que admite la entrada y salida de audio PCM. En este caso, los tipos de entrada y salida son los mismos.


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



En este ejemplo se da por supuesto que ATL se usó para crear el proyecto; La última línea de la función llama al método ATL estándar para registrar el servidor COM. Si no usa ATL, la función tendrá un aspecto diferente.

**Anular el registro de un DMO**

La **función DllUnregisterServer** debe quitar todas las entradas del Registro que cree la función **DllRegisterServer.** Si llama a **DMORegister** al registrar la DMO, debe [**registrar DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) con la misma categoría al anular el registro DMO.

En el ejemplo siguiente se quitan las entradas del Registro creadas en el ejemplo anterior:


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



**DirectShow Valores de mezcciones**

Para la creación de gráficos de filtro, DirectShow asigna un valor de meritorio predeterminado a las DDO. Puede invalidar este valor agregando una entrada del Registro a la clave del Registro DMO la clave del Registro de HKEY \_ CLASSES \_ ROOT \\ CLSID. Incluya un **valor DWORD** denominado `Merit` cuyo valor especifica el resultado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



