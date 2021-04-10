---
title: Implementación de CEchoPropPage Apply
description: Implementación de CEchoPropPage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Complementos de Windows Media Player, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo echo
- Complementos de procesamiento de señal digital, páginas de propiedades de ejemplo de eco
- Complementos DSP, páginas de propiedades de ejemplo echo
- Ejemplo de complemento de DSP de eco, páginas de propiedades
- Ejemplo de complemento DSP de eco, método CEchoPropPage Apply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdca8a771d3e3e26923567f25bf7d19e968595e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903559"
---
# <a name="implementing-cechoproppageapply"></a>Implementación de CEchoPropPage:: Apply

El método CEchoPropPage:: Apply se implementa en EchoPropPage. cpp. Se ejecuta cuando el usuario hace clic en **aplicar** en el cuadro de diálogo Página de propiedades de Windows Media Player. El código de ejemplo del Asistente para complementos proporciona una implementación para controlar una sola propiedad. Puede modificar este código para una de las propiedades de ejemplo de eco y, a continuación, agregar código para almacenar el otro valor de propiedad.

## <a name="declaring-the-apply-method-variables"></a>Declarar las variables de método Apply

En primer lugar, debe quitar la declaración de fScaleFactor. A continuación, agregue las declaraciones de variable que necesitará. En el ejemplo siguiente se muestran las declaraciones de variables completadas:


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a>Recuperación de los valores de la página de propiedades

Debe implementar el código para recuperar y validar los datos proporcionados por el usuario. En el ejemplo de código siguiente se recupera el valor de tiempo de retraso del \_ cuadro de edición IDC DELAYTIME y, a continuación, se comprueba si el valor está dentro de un intervalo especificado:


```
// Get the delay time value from the dialog box.
GetDlgItemText(IDC_DELAYTIME, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwDelayTime = atoi(szStr);

// Make sure delay time is valid.
if ((dwDelayTime < 10) || (dwDelayTime > 2000))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_DELAYRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



Si la entrada del usuario no está en el intervalo especificado, el código muestra un cuadro de mensaje. Observe el uso del recurso de cadena que creó anteriormente para el mensaje de error.

En el ejemplo siguiente se recupera el nivel de efecto del \_ cuadro de edición IDC WETMIX y, a continuación, se comprueba que el valor está dentro de un intervalo especificado:


```
// Get the effects level value from the dialog box.
GetDlgItemText(IDC_WETMIX, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwWetmix = atoi(szStr);

// Make sure wet mix value is valid.
if ((dwWetmix < 0) || (dwWetmix > 100))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_MIXRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



## <a name="storing-the-property-values-in-the-registry"></a>Almacenar los valores de propiedad en el registro

A continuación, el código debe conservar los nuevos valores de propiedad en el registro. El código siguiente almacena ambos valores de propiedad:


```
// update the registry
CRegKey key;
LONG    lResult;

// Write the delay time value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwDelayTime , kszPrefsDelayTime );
}

// Write the wet mix value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwWetmix , kszPrefsWetmix );
}
```



## <a name="updating-the-echo-plug-in-property-values"></a>Actualizar los valores de las propiedades de los complementos de eco

El método **Apply** debe informar al complemento echo de que los valores de propiedad han cambiado. El código siguiente llama al método put de propiedad para cada propiedad mediante el puntero de interfaz recuperado en CEchoPropPage:: SetObjects:


```
// update the plug-in
if (m_spEcho)
{
    m_spEcho->put_delay(dwDelayTime);

    // Convert the wet mix value from DWORD to double.
    fWetmix = (double)dwWetmix / 100;
    m_spEcho->put_wetmix(fWetmix);
}
```



Observe que el valor de la combinación húmeda se convierte en el punto flotante antes de pasarse al complemento.

## <a name="disabling-the-apply-button"></a>Deshabilitar el botón aplicar

Como paso final, el código debe deshabilitar aplicar en el cuadro de diálogo Página de propiedades como una señal al usuario de que los valores se han actualizado correctamente. Esto requiere la siguiente línea de código:


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modificar la página de propiedades de ejemplo echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




