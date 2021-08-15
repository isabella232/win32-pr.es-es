---
title: Implementación de CEcho FinalConstruct
description: Implementación de CEcho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Reproductor de Windows Media complementos, páginas de propiedades de ejemplo de eco
- complementos, páginas de propiedades de ejemplo de eco
- complementos de procesamiento de señales digitales, páginas de propiedades de ejemplo de eco
- Complementos DE DSP, páginas de propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, páginas de propiedades
- Ejemplo de complemento DSP de eco, método FinalConstruct de CEcho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeceeb9c0a7622ada62e98000ad4bfbc2e3faf08c22439039160810771cde8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748152"
---
# <a name="implementing-cechofinalconstruct"></a>Implementación de CEcho::FinalConstruct

El método CEcho::FinalConstruct se implementa en Echo.cpp. Contiene código para leer los valores de propiedad del Registro cuando Reproductor de Windows Media crea una instancia del objeto de complemento DSP. Esto es importante porque permite que la configuración del usuario persista entre instancias del objeto, así como entre sesiones. El código de ejemplo del asistente para complementos proporciona implementación para leer una sola propiedad del Registro. Puede modificar este código para controlar la propiedad de tiempo de retraso y, a continuación, agregar código para leer el valor de la propiedad de combinación con mezcla.

El código de ejemplo siguiente lee cada valor de propiedad del Registro y almacena cada uno en la variable miembro correcta:


```CSharp
CRegKey key;
LONG    lResult;
DWORD   dwValue;

lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
if (ERROR_SUCCESS == lResult)
{
    // Read the delay time from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
    if (ERROR_SUCCESS == lResult)
    {
        m_dwDelayTime = dwValue;
    }

    // Read the wet mix value from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsWetmix );
    if (ERROR_SUCCESS == lResult)
    {
        // Convert the DWORD to a double.
        m_fWetMix = (double)dwValue / 100;
        // Calculate the dry mix value.
        m_fDryMix = 1.0 - m_fWetMix;
    }

}

return S_OK;
```



Tenga en cuenta que el valor DWORD de la mezcla de mezcla con humedad se convierte en un valor de punto flotante. Tenga en cuenta también que el código calcula el valor correcto para m \_ fDryMix.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modificar la página de propiedades Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




