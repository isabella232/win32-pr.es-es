---
title: Implementación de CEcho FinalConstruct
description: Implementación de CEcho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Reproductor de Windows Media complementos, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo de eco
- complementos de procesamiento de señales digitales, páginas de propiedades de ejemplo de eco
- Complementos de DSP, páginas de propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, páginas de propiedades
- Ejemplo de complemento DSP de eco, método FinalConstruct de CEcho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876db9f2479644800c42354a041ad3b1909b526b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068428"
---
# <a name="implementing-cechofinalconstruct"></a>Implementación de CEcho::FinalConstruct

El método CEcho::FinalConstruct se implementa en Echo.cpp. Contiene código para leer los valores de propiedad del Registro cuando Reproductor de Windows Media crea una instancia del objeto de complemento DSP. Esto es importante porque permite que la configuración del usuario persista entre instancias del objeto, así como entre sesiones. El código de ejemplo del asistente para complementos proporciona la implementación para leer una sola propiedad del Registro. Puede modificar este código para controlar la propiedad delay time y, a continuación, agregar código para leer el valor de la propiedad de mezcla con humedad.

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



Tenga en cuenta que el valor DWORD de la mezcla con mezcla se convierte en un valor de punto flotante. Tenga en cuenta también que el código calcula el valor correcto para m \_ fDryMix.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modificar la página de propiedades Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




