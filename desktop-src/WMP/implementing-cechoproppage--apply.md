---
title: Implementación de CEchoPropPage Apply
description: Implementación de CEchoPropPage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Reproductor de Windows Media complementos, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo de eco
- complementos de procesamiento de señales digitales, páginas de propiedades de ejemplo de eco
- Complementos de DSP, páginas de propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, páginas de propiedades
- Ejemplo de complemento DE DSP de eco, método CEchoPropPage Apply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a53d05bee90908f766034c300c99bcfa8d529b06e6713c803bd99bcf042b579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135628"
---
# <a name="implementing-cechoproppageapply"></a>Implementación de CEchoPropPage::Apply

El método CEchoPropPage::Apply se implementa en EchoPropPage.cpp. Se ejecuta cuando el usuario hace clic en **Aplicar en** el cuadro de diálogo de la página de propiedades Reproductor de Windows Media. El código de ejemplo del asistente para complementos proporciona una implementación para controlar una sola propiedad. Puede modificar este código para una de las propiedades de ejemplo Echo y, a continuación, agregar código para almacenar el otro valor de propiedad.

## <a name="declaring-the-apply-method-variables"></a>Declarar las variables del método Apply

En primer lugar, debe quitar la declaración de fScaleFactor. A continuación, agregue las declaraciones de variable que necesitará. En el ejemplo siguiente se muestran las declaraciones de variable completadas:


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a>Recuperar los valores de la página de propiedades

Debe implementar código para recuperar y validar la entrada del usuario. En el ejemplo de código siguiente se recupera el valor de tiempo de retraso del cuadro de edición DELAYTIME de IDC y, a continuación, se comprueba que el valor está dentro de \_ un intervalo especificado:


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

En el ejemplo siguiente se recupera el nivel de efecto del cuadro de edición IDC WETMIX y, a continuación, se comprueba que el valor está dentro de \_ un intervalo especificado:


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



## <a name="storing-the-property-values-in-the-registry"></a>Almacenar los valores de propiedad en el Registro

A continuación, el código debe conservar los nuevos valores de propiedad en el Registro. El código siguiente almacena ambos valores de propiedad:


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



## <a name="updating-the-echo-plug-in-property-values"></a>Actualización de los valores de propiedad del complemento de eco

El **método Apply** debe informar al complemento Echo de que los valores de propiedad han cambiado. El código siguiente llama al método put de la propiedad para cada propiedad mediante el puntero de interfaz recuperado en CEchoPropPage::SetObjects:


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



Tenga en cuenta que el valor de mezcla con humedad se convierte en punto flotante antes de pasarse al complemento.

## <a name="disabling-the-apply-button"></a>Deshabilitar el botón Aplicar

Como último paso, el código debe deshabilitar Aplicar en el cuadro de diálogo de la página de propiedades como una señal al usuario de que los valores se han actualizado correctamente. Esto requiere la siguiente línea de código única:


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modificar la página de propiedades Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




