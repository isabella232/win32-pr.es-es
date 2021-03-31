---
title: Mostrar la cinta de opciones
description: El marco de la cinta de opciones de Windows expone un conjunto de propiedades que permiten a una aplicación especificar cómo se muestra la interfaz de usuario de la cinta en tiempo de ejecución.
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Cinta de Windows, personalizar colores
- Cinta, personalizar colores
- personalizar los colores de la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090c77c5b47afd673bc7132a87e3de336683d876
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078044"
---
# <a name="displaying-the-ribbon"></a>Mostrar la cinta de opciones

El marco de la cinta de opciones de Windows expone un conjunto de propiedades que permiten a una aplicación especificar cómo se muestra la interfaz de usuario de la cinta en tiempo de ejecución.

-   [Introducción](#introduction)
-   [Minimizar la cinta de opciones](#minimize-the-ribbon)
-   [Ocultar la cinta de opciones](#hide-the-ribbon)
-   [Ejemplo](#example)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Para maximizar el área disponible para el espacio del documento (o el puerto de vista) de una aplicación de marco de cinta, una aplicación puede especificar si la interfaz de usuario de la cinta de opciones está visible u oculta y, cuando está visible, si la cinta de opciones se encuentra en un estado expandido o contraído.

Las [claves de propiedad de marco](windowsribbon-reference-properties-framework.md) enumeradas en la tabla siguiente se usan para establecer explícitamente las características de presentación de la interfaz de usuario de la cinta en una aplicación de marco de cinta. Estas propiedades no tienen ningún efecto en la presentación del control [emergente de contexto](windowsribbon-controls-contextpopup.md) .



| Estado de presentación         | Tecla de propiedad de la cinta                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| Expandido o contraído | [PKEY de IU \_ \_ minimizada](windowsribbon-reference-properties-uipkey-minimized.md) |
| Visible u oculto     | [PKEY de IU \_ \_ visible](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a>Minimizar la cinta de opciones

Una aplicación de marco de cinta puede establecer dinámicamente el estado minimizado de la barra de comandos de la cinta de opciones estableciendo el valor de la clave de la propiedad [ \_ PKEY \_ minimizada](windowsribbon-reference-properties-uipkey-minimized.md) de la interfaz de usuario en **true** o **false**.



| Estado de presentación | Valor de clave de propiedad |
|---------------|--------------------|
| Expandido      | **false**          |
| Collapsed     | **true**           |



 

Cuando la interfaz de usuario de la cinta de opciones se encuentra en un estado minimizado, la fila de la pestaña de la cinta permanece visible y es totalmente funcional.

En la captura de pantalla siguiente se muestra la cinta de opciones en el estado minimizado.

![captura de pantalla que muestra la interfaz de usuario de la cinta minimizada.](images/overviews/ribbon-minimized.png)

> [!Note]  
> El marco de la cinta de opciones expone esta funcionalidad al usuario final a través de la selección de "minimizar la cinta" del menú contextual de la cinta de opciones.

 

## <a name="hide-the-ribbon"></a>Ocultar la cinta de opciones

Una aplicación de marco de cinta puede establecer dinámicamente el estado visible de la barra de comandos de la cinta de opciones estableciendo el valor de la clave de propiedad [ \_ PKEY \_ visible](windowsribbon-reference-properties-uipkey-viewable.md) de la interfaz de usuario en **true** o **false**.



| Estado de presentación | Valor de clave de propiedad |
|---------------|--------------------|
| Visible       | **false**          |
| Hidden        | **true**           |



 

A diferencia de la propiedad PKEY de la interfaz de usuario [ \_ \_ minimizada](windowsribbon-reference-properties-uipkey-minimized.md) , el establecimiento de la [UI \_ PKEY \_ visible](windowsribbon-reference-properties-uipkey-viewable.md) en **false** representa la interfaz de usuario de la cinta de opciones invisible y totalmente inutilizable para un usuario final.

En la captura de pantalla siguiente se muestra la cinta de opciones en estado oculto.

![captura de pantalla que muestra la interfaz de usuario de la cinta oculta.](images/overviews/ribbon-viewable.png)

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo establecer el estado de la interfaz de usuario de la cinta de opciones en tiempo de ejecución.

En este caso, la función [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) se usa para expandir o contraer la interfaz de usuario de la cinta de opciones según el estado de alternancia de un [botón de alternancia](windowsribbon-controls-togglebutton.md).


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a Command is executed 
//           by the user. 
//           This example demonstrates a handler for a Toggle Button
//           that sets the minimized state of the ribbon UI.
//
//  NOTES: g_pFramework is a global pointer to an IUIFramework object 
//         that is assigned when the Ribbon framework is initialized.
//
//         g_pRibbon is a global pointer to the IUIRibbon object
//         that is assigned when the Ribbon framework is initialized.
//
STDMETHODIMP CCommandHandler::Execute(
    UINT nCmdID,
    UI_EXECUTIONVERB verb,
    __in_opt const PROPERTYKEY* key,
    __in_opt const PROPVARIANT* ppropvarValue,
    __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
    HRESULT hr = E_FAIL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        switch (nCmdID)
        {
            // Minimize ribbon Command handler.
            case IDR_CMD_MINIMIZE:
                if (g_pFramework)
                {
                    IPropertyStore *pPropertyStore = NULL;
                    hr = g_pRibbon->QueryInterface(__uuidof(IPropertyStore), 
                                                   (void**)&pPropertyStore);
                    if (SUCCEEDED(hr))
                    {
                        if (ppropvarValue != NULL)
                        {
                            // Is the ToggleButton state on or off?
                            BOOL fToggled;
                            hr = UIPropertyToBoolean(*key, *ppropvarValue, &fToggled);

                            if (SUCCEEDED(hr))
                            {
                                // Set the ribbon display state based on the toggle state.
                                PROPVARIANT propvar;
                                PropVariantInit(&propvar);
                                UIInitPropertyFromBoolean(UI_PKEY_Minimized, 
                                                          fToggled, 
                                                          &propvar);
                                hr = pPropertyStore->SetValue(UI_PKEY_Minimized, 
                                                              propvar);
                                pPropertyStore->Commit();
                            }
                            pPropertyStore->Release();
                        }
                    }
                }
                break;
        }
    }
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de la cinta](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 