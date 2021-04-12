---
title: Conservar el estado de la cinta
description: Windows Ribon Framework (cinta) ofrece la posibilidad de conservar el estado de una variedad de configuraciones y preferencias de usuario en las sesiones de la aplicación.
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a3b704151b657bdfe95845c8473a0fd197e87b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359183"
---
# <a name="persisting-ribbon-state"></a>Conservar el estado de la cinta

Windows Ribon Framework (cinta) ofrece la posibilidad de conservar el estado de una variedad de configuraciones y preferencias de usuario en las sesiones de la aplicación.

-   [Introducción](#introduction)
-   [Una experiencia predecible](#a-predictable-experience)
-   [Guardar la configuración de la cinta](#save-ribbon-settings)
-   [Cargar la configuración de la cinta](#load-ribbon-settings)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Varios aspectos de una cinta de opciones, incluidas las preferencias de configuración e interacción, pueden personalizarse por un usuario en tiempo de ejecución para mejorar la facilidad de uso y la productividad. El marco de la cinta de opciones proporciona la funcionalidad para conservar esta configuración en las sesiones de aplicación a través de dos métodos definidos en la implementación de la interfaz [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) : [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) y [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).

## <a name="a-predictable-experience"></a>Una experiencia predecible

Las [instrucciones](https://msdn.microsoft.com/library/cc872782.aspx) para la experiencia del usuario de la cinta de opciones aconsejan que, para proporcionar la mejor experiencia de usuario posible, las aplicaciones de cinta deberían conservar el estado de la cinta de opciones (aparte de la última pestaña seleccionada) a medida que se cierra la aplicación. De esta manera, cuando se inicia la misma aplicación, se pueden restaurar la configuración y las personalizaciones de la sesión anterior, y el usuario puede esperar que continúe interactuando con la aplicación de la misma manera en que la dejó.

La configuración de la cinta de opciones que se puede modificar en tiempo de ejecución y conservar en las sesiones de aplicación se muestra en el menú contextual. Incluyen:

-   Comandos agregados a la lista de comandos de la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md) por el usuario. Especificado por un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) a través de la clave de la propiedad PKEY de la [interfaz de usuario \_ \_](windowsribbon-reference-properties-uipkey-itemssource.md) .

    En la captura de pantalla siguiente se muestra el comando de menú contextual **Agregar a la barra de herramientas de acceso rápido** .

    ![captura de pantalla del menú contextual de la cinta de opciones de Microsoft Paint.](images/controls/qat-contextmenu-add.png)

-   El estado de acoplamiento de la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md) preferido. Lo especifica el [**valor \_ CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) de la interfaz de usuario de la clave de la propiedad [ \_ PKEY \_ QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) de la interfaz de usuario.

    En esta captura de pantalla se muestra la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md) en su ubicación predeterminada de la barra de título de la aplicación y la **barra de herramientas Mostrar acceso rápido debajo del** comando de menú contextual de la cinta.

    ![captura de pantalla del menú contextual de la cinta de opciones de Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    Esta captura de pantalla muestra la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md) debajo de la cinta de opciones.

    ![captura de pantalla de la barra de herramientas de acceso rápido acoplada debajo de la cinta de opciones.](images/controls/qat-dockbottom.png)

-   El estado minimizado de la cinta de opciones según lo especificado por el valor booleano de la clave de la propiedad [ \_ PKEY \_ minimizada](windowsribbon-reference-properties-uipkey-minimized.md) de la interfaz de usuario.

    > [!Note]  
    > El estado minimizado de la cinta de opciones no es equivalente al estado contraído de la cinta de opciones. Cuando se encuentra en estado contraído, la cinta de opciones está totalmente oculta y no se puede interactuar con ella. El marco de trabajo invoca este estado automáticamente si se reduce el tamaño de la ventana de la aplicación, ya sea horizontal o verticalmente, hasta el punto en que la cinta oculta el área de trabajo de la aplicación. El marco restaura la cinta de opciones cuando aumenta el tamaño de la ventana de la aplicación.

     

    En esta captura de pantalla se muestra el comando de menú contextual **minimizar la cinta de** opciones.

    ![captura de pantalla del menú contextual de la cinta de opciones de Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    Esta captura de pantalla muestra una cinta minimizada.

    ![captura de pantalla de la cinta de opciones minimizada de Microsoft Paint.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a>Guardar la configuración de la cinta

El método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) escribe una representación binaria del estado de la cinta de opciones persistente (descrita en la sección anterior) en un objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) . A continuación, la aplicación guarda el contenido del objeto IStream en un archivo o en el registro de Windows.

En el ejemplo siguiente se muestra el código básico necesario para escribir el estado de la cinta de opciones en un objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) mediante el método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .


```C++
// pRibbon        - Pointer to the IUIRibbon interface
// ppStatusStream - Pointer to the location of a newly created IStream object
HRESULT CApplication::SaveRibbonStatusToStream(
                        __in IUIRibbon *pRibbon, 
                        __out IStream **ppStatusStream)
{
  HRESULT hr = E_FAIL; 

  *ppStatusStream = NULL;
  IStream* pStream;
  if (SUCCEEDED(hr = CreateStreamOnHGlobal(
                       NULL,  // Internally allocate a new shared memory.
                       FALSE, // Free hGlobal after IStream object released.
                       &pStream)))
  {
    if (SUCCEEDED(hr = pRibbon->SaveSettingsToStream(*ppStatusStream)))
    {                  
      pStream->AddRef();
      *ppStatusStream = pStream;
    }
    pStream->Release();
  }
  return hr;
}
```



## <a name="load-ribbon-settings"></a>Cargar la configuración de la cinta

El método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) se usa para recuperar la información de estado de la cinta de opciones persistente almacenada como un objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) por el método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) . La información del objeto IStream se aplica a la interfaz de usuario de la cinta de opciones cuando se inicializa la aplicación.

En el ejemplo siguiente se muestra el código básico necesario para cargar el estado de la cinta de opciones desde un objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) con el método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .


```C++
// pRibbon       - Pointer to the IUIRibbon interface
// pStatusStream - Pointer to the IStream object that contains the Ribbon state information
HRESULT CApplication::LoadRibbonStatusFromStream(
                        __in IUIRibbon *pRibbon, 
                        __in IStream *pStatusStream)
{     
  HRESULT hr = E_FAIL;
  if (pStatusStream)
  {
    // Set the stream position to the beginning first.
    LARGE_INTEGER liStart = {0, 0};
    ULARGE_INTEGER ulActual;
    pStatusStream->Seek(liStart, STREAM_SEEK_SET, &ulActual);
    hr = pRibbon->LoadSettingsFromStream(pStatusStream);
  }
  return hr;
}
```



Para obtener un rendimiento óptimo, se debe llamar al método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) desde la función de devolución de llamada [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) durante la fase de inicialización del marco, tal y como se muestra en el ejemplo siguiente.


```C++
IFACEMETHODIMP CMyRibbonApplication::OnViewChanged(
                                       UINT nViewID, 
                                       __in UI_VIEWTYPE typeID, 
                                       __in IUnknown* pView, 
                                       UI_VIEWVERB verb, 
                                       INT iReasonCode)
{
  HRESULT hr = E_NOTIMPL;
  if (UI_VIEWVERB_CREATE == verb)
  {
    IUIRibbon* pRibbon = NULL;
    hr = pView->QueryInterface(IID_PPV_ARGS(&pRibbon));

    if (SUCCEEDED(hr))
    {
      hr = _LoadRibbonSettings(pRibbon);
      pRibbon->Release();
    }
  }
  return hr;
}

HRESULT CMyRibbonApplication::_LoadRibbonSettings(IUIRibbon* pRibbon)
{
  ...
  pRibbon->LoadSettingsFromStream(pStream);
  ...
}
```



Varias instancias de la misma aplicación de marco de cinta pueden administrar cada estado de la cinta de opciones independientemente como objetos [IStream](/windows/win32/api/objidl/nn-objidl-istream) independientes o como un grupo a través de un único objeto IStream.

Al sincronizar el estado de la cinta de opciones en un grupo de instancias de la aplicación, cada ventana de nivel superior debe escuchar una notificación de [ \_ activación de WM](../inputdev/wm-activate.md) . La ventana de nivel superior que se va a desactivar guarda su estado de cinta mediante el método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) y la ventana de nivel superior que se está activando carga su estado de cinta mediante el método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 