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
# <a name="persisting-ribbon-state"></a><span data-ttu-id="56d68-103">Conservar el estado de la cinta</span><span class="sxs-lookup"><span data-stu-id="56d68-103">Persisting Ribbon State</span></span>

<span data-ttu-id="56d68-104">Windows Ribon Framework (cinta) ofrece la posibilidad de conservar el estado de una variedad de configuraciones y preferencias de usuario en las sesiones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56d68-104">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

-   [<span data-ttu-id="56d68-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="56d68-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="56d68-106">Una experiencia predecible</span><span class="sxs-lookup"><span data-stu-id="56d68-106">A Predictable Experience</span></span>](#a-predictable-experience)
-   [<span data-ttu-id="56d68-107">Guardar la configuración de la cinta</span><span class="sxs-lookup"><span data-stu-id="56d68-107">Save Ribbon Settings</span></span>](#save-ribbon-settings)
-   [<span data-ttu-id="56d68-108">Cargar la configuración de la cinta</span><span class="sxs-lookup"><span data-stu-id="56d68-108">Load Ribbon Settings</span></span>](#load-ribbon-settings)
-   [<span data-ttu-id="56d68-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56d68-109">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="56d68-110">Introducción</span><span class="sxs-lookup"><span data-stu-id="56d68-110">Introduction</span></span>

<span data-ttu-id="56d68-111">Varios aspectos de una cinta de opciones, incluidas las preferencias de configuración e interacción, pueden personalizarse por un usuario en tiempo de ejecución para mejorar la facilidad de uso y la productividad.</span><span class="sxs-lookup"><span data-stu-id="56d68-111">Various aspects of a ribbon, including configuration and interaction preferences, can be customized by a user at run time to improve usability and productivity.</span></span> <span data-ttu-id="56d68-112">El marco de la cinta de opciones proporciona la funcionalidad para conservar esta configuración en las sesiones de aplicación a través de dos métodos definidos en la implementación de la interfaz [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) : [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) y [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span><span class="sxs-lookup"><span data-stu-id="56d68-112">The Ribbon framework provides the functionality to preserve these settings across application sessions through two methods defined in the implementation of the [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) interface: [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) and [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span></span>

## <a name="a-predictable-experience"></a><span data-ttu-id="56d68-113">Una experiencia predecible</span><span class="sxs-lookup"><span data-stu-id="56d68-113">A Predictable Experience</span></span>

<span data-ttu-id="56d68-114">Las [instrucciones](https://msdn.microsoft.com/library/cc872782.aspx) para la experiencia del usuario de la cinta de opciones aconsejan que, para proporcionar la mejor experiencia de usuario posible, las aplicaciones de cinta deberían conservar el estado de la cinta de opciones (aparte de la última pestaña seleccionada) a medida que se cierra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56d68-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) advise that, to provide the most predictable user experience possible, Ribbon applications should preserve the state of the ribbon (aside from the last selected tab) as the application is closed.</span></span> <span data-ttu-id="56d68-115">De esta manera, cuando se inicia la misma aplicación, se pueden restaurar la configuración y las personalizaciones de la sesión anterior, y el usuario puede esperar que continúe interactuando con la aplicación de la misma manera en que la dejó.</span><span class="sxs-lookup"><span data-stu-id="56d68-115">In this way, when the same application is launched, the settings and customizations from the previous session can be restored and the user can expect to continue interacting with the application in the same way as they left it.</span></span>

<span data-ttu-id="56d68-116">La configuración de la cinta de opciones que se puede modificar en tiempo de ejecución y conservar en las sesiones de aplicación se muestra en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="56d68-116">Ribbon settings that can be modified at run time and preserved across application sessions are listed in the Command context menu.</span></span> <span data-ttu-id="56d68-117">Incluyen:</span><span class="sxs-lookup"><span data-stu-id="56d68-117">They include:</span></span>

-   <span data-ttu-id="56d68-118">Comandos agregados a la lista de comandos de la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md) por el usuario.</span><span class="sxs-lookup"><span data-stu-id="56d68-118">Commands added to the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) Command list by the user.</span></span> <span data-ttu-id="56d68-119">Especificado por un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) a través de la clave de la propiedad PKEY de la [interfaz de usuario \_ \_](windowsribbon-reference-properties-uipkey-itemssource.md) .</span><span class="sxs-lookup"><span data-stu-id="56d68-119">Specified by an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span>

    <span data-ttu-id="56d68-120">En la captura de pantalla siguiente se muestra el comando de menú contextual **Agregar a la barra de herramientas de acceso rápido** .</span><span class="sxs-lookup"><span data-stu-id="56d68-120">The following screen shot shows the **Add to Quick Access Toolbar** context menu Command.</span></span>

    ![captura de pantalla del menú contextual de la cinta de opciones de Microsoft Paint.](images/controls/qat-contextmenu-add.png)

-   <span data-ttu-id="56d68-122">El estado de acoplamiento de la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md) preferido.</span><span class="sxs-lookup"><span data-stu-id="56d68-122">The preferred [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) docking state.</span></span> <span data-ttu-id="56d68-123">Lo especifica el [**valor \_ CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) de la interfaz de usuario de la clave de la propiedad [ \_ PKEY \_ QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="56d68-123">Specified by the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) value of the [UI\_PKEY\_QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) property key.</span></span>

    <span data-ttu-id="56d68-124">En esta captura de pantalla se muestra la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md) en su ubicación predeterminada de la barra de título de la aplicación y la **barra de herramientas Mostrar acceso rápido debajo del** comando de menú contextual de la cinta.</span><span class="sxs-lookup"><span data-stu-id="56d68-124">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) in its default application title bar location and the **Show Quick Access Toolbar below the Ribbon** context menu Command.</span></span>

    ![captura de pantalla del menú contextual de la cinta de opciones de Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="56d68-126">Esta captura de pantalla muestra la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md) debajo de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="56d68-126">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) below the ribbon.</span></span>

    ![captura de pantalla de la barra de herramientas de acceso rápido acoplada debajo de la cinta de opciones.](images/controls/qat-dockbottom.png)

-   <span data-ttu-id="56d68-128">El estado minimizado de la cinta de opciones según lo especificado por el valor booleano de la clave de la propiedad [ \_ PKEY \_ minimizada](windowsribbon-reference-properties-uipkey-minimized.md) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="56d68-128">The ribbon minimized state as specified by the boolean value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key.</span></span>

    > [!Note]  
    > <span data-ttu-id="56d68-129">El estado minimizado de la cinta de opciones no es equivalente al estado contraído de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="56d68-129">The ribbon minimized state is not equivalent to the ribbon collapsed state.</span></span> <span data-ttu-id="56d68-130">Cuando se encuentra en estado contraído, la cinta de opciones está totalmente oculta y no se puede interactuar con ella.</span><span class="sxs-lookup"><span data-stu-id="56d68-130">When in collapsed state, the ribbon is completely hidden and cannot be interacted with.</span></span> <span data-ttu-id="56d68-131">El marco de trabajo invoca este estado automáticamente si se reduce el tamaño de la ventana de la aplicación, ya sea horizontal o verticalmente, hasta el punto en que la cinta oculta el área de trabajo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56d68-131">The framework invokes this state automatically if the application window is reduced in size, either horizontally or vertically, to the point that the ribbon obscures the application workspace.</span></span> <span data-ttu-id="56d68-132">El marco restaura la cinta de opciones cuando aumenta el tamaño de la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56d68-132">The framework restores the ribbon when the size of the application window is increased.</span></span>

     

    <span data-ttu-id="56d68-133">En esta captura de pantalla se muestra el comando de menú contextual **minimizar la cinta de** opciones.</span><span class="sxs-lookup"><span data-stu-id="56d68-133">This screen shot shows the **Minimize the Ribbon** context menu Command.</span></span>

    ![captura de pantalla del menú contextual de la cinta de opciones de Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="56d68-135">Esta captura de pantalla muestra una cinta minimizada.</span><span class="sxs-lookup"><span data-stu-id="56d68-135">This screen shot shows a minimized ribbon.</span></span>

    ![captura de pantalla de la cinta de opciones minimizada de Microsoft Paint.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a><span data-ttu-id="56d68-137">Guardar la configuración de la cinta</span><span class="sxs-lookup"><span data-stu-id="56d68-137">Save Ribbon Settings</span></span>

<span data-ttu-id="56d68-138">El método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) escribe una representación binaria del estado de la cinta de opciones persistente (descrita en la sección anterior) en un objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="56d68-138">The [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method writes a binary representation of the persistent ribbon state (outlined in the previous section) to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span> <span data-ttu-id="56d68-139">A continuación, la aplicación guarda el contenido del objeto IStream en un archivo o en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="56d68-139">The application then saves the content of the IStream object to a file or the Windows registry.</span></span>

<span data-ttu-id="56d68-140">En el ejemplo siguiente se muestra el código básico necesario para escribir el estado de la cinta de opciones en un objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) mediante el método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .</span><span class="sxs-lookup"><span data-stu-id="56d68-140">The following example demonstrates the basic code required to write the ribbon state to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span>


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



## <a name="load-ribbon-settings"></a><span data-ttu-id="56d68-141">Cargar la configuración de la cinta</span><span class="sxs-lookup"><span data-stu-id="56d68-141">Load Ribbon Settings</span></span>

<span data-ttu-id="56d68-142">El método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) se usa para recuperar la información de estado de la cinta de opciones persistente almacenada como un objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) por el método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .</span><span class="sxs-lookup"><span data-stu-id="56d68-142">The [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method is used to retrieve the persistent ribbon state information stored as an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object by the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span> <span data-ttu-id="56d68-143">La información del objeto IStream se aplica a la interfaz de usuario de la cinta de opciones cuando se inicializa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56d68-143">The information in the IStream object is applied to the ribbon UI when the application initializes.</span></span>

<span data-ttu-id="56d68-144">En el ejemplo siguiente se muestra el código básico necesario para cargar el estado de la cinta de opciones desde un objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) con el método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="56d68-144">The following example demonstrates the basic code required to load the ribbon state from an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object with the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>


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



<span data-ttu-id="56d68-145">Para obtener un rendimiento óptimo, se debe llamar al método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) desde la función de devolución de llamada [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) durante la fase de inicialización del marco, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="56d68-145">For optimal performance, the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method should be called from the [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) callback function during the framework initialization phase, as shown in the following example.</span></span>


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



<span data-ttu-id="56d68-146">Varias instancias de la misma aplicación de marco de cinta pueden administrar cada estado de la cinta de opciones independientemente como objetos [IStream](/windows/win32/api/objidl/nn-objidl-istream) independientes o como un grupo a través de un único objeto IStream.</span><span class="sxs-lookup"><span data-stu-id="56d68-146">Multiple instances of the same Ribbon framework application can manage each ribbon state independently as separate [IStream](/windows/win32/api/objidl/nn-objidl-istream) objects or as a group through a single IStream object.</span></span>

<span data-ttu-id="56d68-147">Al sincronizar el estado de la cinta de opciones en un grupo de instancias de la aplicación, cada ventana de nivel superior debe escuchar una notificación de [ \_ activación de WM](../inputdev/wm-activate.md) .</span><span class="sxs-lookup"><span data-stu-id="56d68-147">When synchronizing ribbon state across a group of application instances, each top-level window must listen for a [WM\_ACTIVATE](../inputdev/wm-activate.md) notification.</span></span> <span data-ttu-id="56d68-148">La ventana de nivel superior que se va a desactivar guarda su estado de cinta mediante el método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) y la ventana de nivel superior que se está activando carga su estado de cinta mediante el método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="56d68-148">The top-level window being deactivated saves its ribbon state using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method, and the top-level window being activated loads its ribbon state using the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56d68-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56d68-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56d68-150">Barra de herramientas de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="56d68-150">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 