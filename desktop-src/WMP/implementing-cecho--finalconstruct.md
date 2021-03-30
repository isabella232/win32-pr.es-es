---
title: Implementación de CEcho FinalConstruct
description: Implementación de CEcho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Complementos de Windows Media Player, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo echo
- Complementos de procesamiento de señal digital, páginas de propiedades de ejemplo de eco
- Complementos DSP, páginas de propiedades de ejemplo echo
- Ejemplo de complemento de DSP de eco, páginas de propiedades
- Ejemplo de complemento DSP de eco, método CEcho FinalConstruct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876db9f2479644800c42354a041ad3b1909b526b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148797"
---
# <a name="implementing-cechofinalconstruct"></a>Implementación de CEcho:: FinalConstruct

El método CEcho:: FinalConstruct se implementa en echo. cpp. Contiene código para leer los valores de propiedad del registro cuando Windows Media Player crea instancias del objeto de complemento DSP. Esto es importante porque permite que la configuración del usuario se mantenga entre las instancias del objeto, así como entre las sesiones. El código de ejemplo del Asistente para complementos proporciona implementación para leer una única propiedad del registro. Puede modificar este código para controlar la propiedad de tiempo de retraso y, a continuación, agregar código para leer el valor de propiedad de combinación húmeda.

En el código de ejemplo siguiente se lee cada valor de propiedad del registro y se almacena cada en la variable miembro correcta:


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



Observe que el valor DWORD de la combinación húmeda se convierte en un valor de punto flotante. Tenga en cuenta también que el código calcula el valor correcto para m \_ fDryMix.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modificar la página de propiedades de ejemplo echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




