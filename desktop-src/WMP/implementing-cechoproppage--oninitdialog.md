---
title: Implementación de CEchoPropPage OnInitDialog
description: Implementación de CEchoPropPage OnInitDialog
ms.assetid: 568989b0-bc07-480f-8b5c-41bbada713f8
keywords:
- Complementos de Windows Media Player, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo echo
- Complementos de procesamiento de señal digital, páginas de propiedades de ejemplo de eco
- Complementos DSP, páginas de propiedades de ejemplo echo
- Ejemplo de complemento de DSP de eco, páginas de propiedades
- Ejemplo de complemento DSP de eco, CEchoPropPage OnInitDialog (método)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0874c750914b5caecf86ffa61a0c42d38bb1c02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695260"
---
# <a name="implementing-cechoproppageoninitdialog"></a>Implementar CEchoPropPage:: OnInitDialog

El método **CEchoPropPage:: OnInitDialog** se implementa en EchoPropPage. cpp. Se ejecuta cuando se invoca el cuadro de diálogo de la página de propiedades. El código de este método debe recuperar los valores de propiedad actuales y mostrarlos en el cuadro de edición correcto. El código de ejemplo del Asistente para complementos proporciona una implementación para una sola propiedad. Puede modificar este código para una de las propiedades de ejemplo de eco y, a continuación, agregar código para recuperar el segundo valor de propiedad.

## <a name="declaring-the-oninitdialog-method-variables"></a>Declarar las variables del método OnInitDialog

En primer lugar, debe quitar la declaración de fScaleFactor y reemplazarla por las siguientes declaraciones de variable:


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a>Recuperar los valores actuales del complemento

El código debe intentar después recuperar los valores de propiedad actuales del complemento de eco. En el ejemplo siguiente se intenta recuperar cada propiedad:


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



En el cuadro de diálogo se muestra el valor de nivel de efectos para el usuario como un entero, pero el complemento almacena el valor como un número de punto flotante. Por lo tanto, el código convierte el valor de punto flotante en un valor **DWORD** .

## <a name="retrieving-the-current-values-from-the-registry"></a>Recuperación de los valores actuales del registro

Si la página de propiedades no puede recuperar los valores actuales del complemento, debe intentar leerlos desde el registro. El código siguiente lee cada valor de propiedad:


```
else // Otherwise, read values from registry
{
    CRegKey key;
    LONG    lResult;

    lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
    if (ERROR_SUCCESS == lResult)
    {
        DWORD   dwValue = 0;

        // Read the delay time.
        lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
        if (ERROR_SUCCESS == lResult)
        {
            dwDelayTime = dwValue;
        }

        // Read the wet mix value.
        lResult = key.QueryValue(dwValue, kszPrefsWetmix );
        if (ERROR_SUCCESS == lResult)
        {
            dwWetmix = dwValue;
        }
    }
}
```



Observe el uso de las constantes del registro que creó anteriormente.

## <a name="displaying-the-values-to-the-user"></a>Mostrar los valores al usuario

Por último, la página de propiedades debe mostrar los valores en los controles de cuadro de edición correctos. En el código de ejemplo siguiente se muestra esto:


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modificar la página de propiedades de ejemplo echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




