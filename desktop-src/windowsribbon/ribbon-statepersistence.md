---
title: Estado de la cinta de opciones persistente
description: El Windows de aplicaciones (cinta de opciones) proporciona la capacidad de conservar el estado de una variedad de configuraciones de usuario y preferencias en las sesiones de la aplicación.
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e506d1cc8138f569dc21b491cc11ed58411131c0dd80532c19043c5974995e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707949"
---
# <a name="persisting-ribbon-state"></a>Estado de la cinta de opciones persistente

El Windows de aplicaciones (cinta de opciones) proporciona la capacidad de conservar el estado de una variedad de configuraciones de usuario y preferencias en las sesiones de la aplicación.

-   [Introducción](#introduction)
-   [Una experiencia predecible](#a-predictable-experience)
-   [Guardar la cinta de opciones Configuración](#save-ribbon-settings)
-   [Carga de la cinta Configuración](#load-ribbon-settings)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Un usuario puede personalizar varios aspectos de una cinta de opciones, incluidas las preferencias de configuración e interacción, en tiempo de ejecución para mejorar la facilidad de uso y la productividad. El marco de la cinta de opciones proporciona la funcionalidad para conservar esta configuración entre sesiones de aplicación mediante dos métodos definidos en la implementación de la interfaz [**IUIRibbon:**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) e [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).

## <a name="a-predictable-experience"></a>Una experiencia predecible

Las [](https://msdn.microsoft.com/library/cc872782.aspx) directrices de la experiencia del usuario de la cinta de opciones aconsejan que, para proporcionar la experiencia de usuario más predecible posible, las aplicaciones de la cinta de opciones deben conservar el estado de la cinta de opciones (aparte de la última pestaña seleccionada) a medida que se cierra la aplicación. De este modo, cuando se inicia la misma aplicación, se puede restaurar la configuración y las personalizaciones de la sesión anterior y el usuario puede esperar seguir interactuando con la aplicación de la misma manera que lo dejó.

La configuración de la cinta de opciones que se puede modificar en tiempo de ejecución y conservarse en las sesiones de la aplicación se muestra en el menú contextual Comando. Incluyen:

-   Comandos agregados por el usuario a la lista Comandos de [la barra](windowsribbon-controls-quickaccesstoolbar.md) de herramientas de acceso rápido. Especificado por un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) a través de la clave de [ \_ propiedad \_ ItemsSource de PKEY de](windowsribbon-reference-properties-uipkey-itemssource.md) la interfaz de usuario.

    En la siguiente captura de pantalla se muestra el menú contextual Agregar **a la barra** de herramientas de acceso rápido Comando.

    ![captura de pantalla del menú contextual del comando en la cinta de microsoft paint.](images/controls/qat-contextmenu-add.png)

-   Estado de acoplamiento preferido [de la barra de](windowsribbon-controls-quickaccesstoolbar.md) herramientas de acceso rápido. Especificado por el valor [**\_ CONTROLDOCK de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) interfaz de usuario [ \_ PKEY \_ QuickAccessToolbarDock clave](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) de propiedad.

    En esta captura de pantalla se muestra [la barra](windowsribbon-controls-quickaccesstoolbar.md) de herramientas de acceso rápido en la ubicación predeterminada de la barra de título de la aplicación y la barra de herramientas Mostrar acceso rápido debajo del menú **contextual** de la cinta Comando.

    ![captura de pantalla del menú contextual del comando en la cinta de microsoft paint.](images/controls/qat-contextmenu-add.png)

    Esta captura de pantalla muestra la [barra de herramientas de acceso rápido debajo](windowsribbon-controls-quickaccesstoolbar.md) de la cinta de opciones.

    ![captura de pantalla de la barra de herramientas de acceso rápido acoplada debajo de la cinta de opciones.](images/controls/qat-dockbottom.png)

-   El estado minimizado de la cinta de opciones según lo especificado por el valor booleano de la clave de [ \_ propiedad PKEY \_ minimizada](windowsribbon-reference-properties-uipkey-minimized.md) de la interfaz de usuario.

    > [!Note]  
    > El estado minimizado de la cinta de opciones no es equivalente al estado contraído de la cinta de opciones. Cuando está en estado contraído, la cinta de opciones está completamente oculta y no se puede interactuar con ella. El marco invoca este estado automáticamente si se reduce el tamaño de la ventana de la aplicación, ya sea horizontal o verticalmente, hasta el punto de que la cinta de opciones oculta el área de trabajo de la aplicación. El marco restaura la cinta de opciones cuando aumenta el tamaño de la ventana de la aplicación.

     

    En esta captura de pantalla se muestra **el menú contextual Minimizar la** cinta de opciones Comando.

    ![captura de pantalla del menú contextual del comando en la cinta de microsoft paint.](images/controls/qat-contextmenu-add.png)

    Esta captura de pantalla muestra una cinta de opciones minimizada.

    ![captura de pantalla de la cinta de opciones de pintura de Microsoft minimizada.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a>Guardar la cinta de opciones Configuración

El [**método IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) escribe una representación binaria del estado de la cinta de opciones persistente (descrito en la sección anterior) en un [objeto IStream.](/windows/win32/api/objidl/nn-objidl-istream) A continuación, la aplicación guarda el contenido del objeto IStream en un archivo o en Windows registro.

En el ejemplo siguiente se muestra el código básico necesario para escribir el estado de la cinta de opciones en un [objeto IStream](/windows/win32/api/objidl/nn-objidl-istream) mediante el [**método IUIRibbon::SaveSettingsToStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream)


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



## <a name="load-ribbon-settings"></a>Carga de la cinta Configuración

El [**método IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) se usa para recuperar la información de estado de la cinta de opciones persistente almacenada como un [objeto IStream](/windows/win32/api/objidl/nn-objidl-istream) por el [**método IUIRibbon::SaveSettingsToStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) La información del objeto IStream se aplica a la interfaz de usuario de la cinta de opciones cuando se inicializa la aplicación.

En el ejemplo siguiente se muestra el código básico necesario para cargar el estado de la cinta de opciones desde un [objeto IStream](/windows/win32/api/objidl/nn-objidl-istream) con el [**método IUIRibbon::LoadSettingsFromStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream)


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



Para obtener un rendimiento óptimo, se debe llamar al método [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) desde la función de devolución de llamada [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) durante la fase de inicialización del marco, como se muestra en el ejemplo siguiente.


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



Varias instancias de la misma aplicación de marco de la cinta de opciones pueden administrar cada estado de la cinta de opciones independientemente como objetos [IStream](/windows/win32/api/objidl/nn-objidl-istream) independientes o como un grupo a través de un único objeto IStream.

Al sincronizar el estado de la cinta de opciones en un grupo de instancias de aplicación, cada ventana de nivel superior debe escuchar una [notificación WM \_ ACTIVATE.](../inputdev/wm-activate.md) La ventana de nivel superior que se desactiva guarda su estado de la cinta de opciones mediante el método [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) y la ventana de nivel superior que se activa carga su estado de cinta mediante el método [**IUIRibbon::LoadSettingsFromStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 