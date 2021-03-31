---
title: Barra de herramientas de acceso rápido
description: La barra de herramientas de acceso rápido (QAT) es una pequeña barra de herramientas personalizable que muestra un conjunto de comandos especificados por la aplicación o seleccionados por el usuario.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a50d562477e5c626d2d2bffa8ee5e0ecc84919
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077769"
---
# <a name="quick-access-toolbar"></a><span data-ttu-id="6976c-103">Barra de herramientas de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="6976c-103">Quick Access Toolbar</span></span>

<span data-ttu-id="6976c-104">La barra de herramientas de acceso rápido (QAT) es una pequeña barra de herramientas personalizable que muestra un conjunto de comandos especificados por la aplicación o seleccionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="6976c-104">The Quick Access Toolbar (QAT) is a small, customizable toolbar that exposes a set of Commands that are specified by the application or selected by the user.</span></span>

- [<span data-ttu-id="6976c-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="6976c-105">Introduction</span></span>](#introduction)
- [<span data-ttu-id="6976c-106">Implementar la barra de herramientas de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="6976c-106">Implement the Quick Access Toolbar</span></span>](#implement-the-quick-access-toolbar)
  - [<span data-ttu-id="6976c-107">marcado</span><span class="sxs-lookup"><span data-stu-id="6976c-107">Markup</span></span>](#markup)
  - [<span data-ttu-id="6976c-108">Código</span><span class="sxs-lookup"><span data-stu-id="6976c-108">Code</span></span>](#code)
- [<span data-ttu-id="6976c-109">Persistencia de QAT</span><span class="sxs-lookup"><span data-stu-id="6976c-109">QAT Persistence</span></span>](#qat-persistence)
- [<span data-ttu-id="6976c-110">Propiedades de la barra de herramientas de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="6976c-110">Quick Access Toolbar Properties</span></span>](#quick-access-toolbar-properties)
- [<span data-ttu-id="6976c-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6976c-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="6976c-112">Introducción</span><span class="sxs-lookup"><span data-stu-id="6976c-112">Introduction</span></span>

<span data-ttu-id="6976c-113">De forma predeterminada, la barra de herramientas de acceso rápido (QAT) se encuentra en la barra de título de la ventana de la aplicación, pero se puede configurar para que se muestre debajo de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="6976c-113">By default, the Quick Access Toolbar (QAT) is located in the title bar of the application window but can be configured to display below the ribbon.</span></span> <span data-ttu-id="6976c-114">Además de exponer comandos, la barra de herramientas de acceso rápido (QAT) también incluye un menú desplegable personalizable que contiene el conjunto completo de comandos predeterminados de la barra de herramientas de acceso rápido (QAT) (ya sea oculto o mostrado en la barra de herramientas de acceso rápido (QAT)) y un conjunto de opciones de la barra de herramientas de acceso rápido (QAT).</span><span class="sxs-lookup"><span data-stu-id="6976c-114">In addition to exposing Commands, the Quick Access Toolbar (QAT) also includes a customizable drop-down menu that contains the complete set of default Quick Access Toolbar (QAT) Commands (whether hidden or displayed in the Quick Access Toolbar (QAT)) and a set of Quick Access Toolbar (QAT) and ribbon options.</span></span>

<span data-ttu-id="6976c-115">En la captura de pantalla siguiente se muestra un ejemplo de la barra de herramientas de acceso rápido de la cinta de opciones (QAT).</span><span class="sxs-lookup"><span data-stu-id="6976c-115">The following screen shot shows an example of the Ribbon Quick Access Toolbar (QAT).</span></span>

![captura de pantalla de Qat en la cinta de opciones de Microsoft Paint.](images/markup/qat-and-menu.png)

<span data-ttu-id="6976c-117">La barra de herramientas de acceso rápido (QAT) consta de una combinación de hasta 20 comandos especificados por la aplicación (conocida como lista de valores predeterminados de la aplicación) o seleccionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="6976c-117">The Quick Access Toolbar (QAT) consists of a combination of up to 20 Commands either specified by the application (known as the application defaults list) or selected by the user.</span></span> <span data-ttu-id="6976c-118">La barra de herramientas de acceso rápido (QAT) puede contener comandos únicos que no están disponibles en ningún otro lugar de la interfaz de usuario de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="6976c-118">The Quick Access Toolbar (QAT) can contain unique Commands that are not available elsewhere in the ribbon UI.</span></span>

> [!Note]
> <span data-ttu-id="6976c-119">Aunque casi todos los controles de la cinta de opciones permiten agregar su comando asociado a la barra de herramientas de acceso rápido (QAT) a través del menú contextual que se muestra en la siguiente captura de pantalla, los comandos expuestos en una [ventana emergente de contexto](windowsribbon-controls-contextpopup.md) no proporcionan este menú contextual.</span><span class="sxs-lookup"><span data-stu-id="6976c-119">While almost all ribbon controls allow their associated Command to be added to the Quick Access Toolbar (QAT) through the context menu shown in the following screen shot, Commands exposed in a [Context Popup](windowsribbon-controls-contextpopup.md) do not provide this context menu.</span></span>
>
> ![captura de pantalla del menú contextual de la cinta de opciones de Microsoft Paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a><span data-ttu-id="6976c-121">Implementar la barra de herramientas de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="6976c-121">Implement the Quick Access Toolbar</span></span>

<span data-ttu-id="6976c-122">Al igual que con todos los controles de marco de cinta de Windows, sacar el máximo partido de la barra de herramientas de acceso rápido (QAT) requiere un componente de marcado que controle su presentación dentro de la cinta de opciones y un componente de código que rija su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="6976c-122">As with all Windows Ribbon framework controls, taking full advantage of the Quick Access Toolbar (QAT) requires both a markup component that controls its presentation within the ribbon and a code component that governs its functionality.</span></span>

### <a name="markup"></a><span data-ttu-id="6976c-123">marcado</span><span class="sxs-lookup"><span data-stu-id="6976c-123">Markup</span></span>

<span data-ttu-id="6976c-124">El control de barra de herramientas de acceso rápido (QAT) se declara y se asocia a un identificador de comando, en el marcado mediante el elemento [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="6976c-124">The Quick Access Toolbar (QAT) control is declared, and associated with a Command ID, in markup through the [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span> <span data-ttu-id="6976c-125">El identificador de comando se usa para identificar y enlazar la barra de herramientas de acceso rápido (QAT) a un controlador de comandos definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6976c-125">The Command ID is used to identify and bind the Quick Access Toolbar (QAT) to a Command handler defined by the application.</span></span>

<span data-ttu-id="6976c-126">Además del controlador de comandos básico para la funcionalidad principal de la barra de herramientas de acceso rápido (QAT), al declarar el atributo de elemento [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) de *CustomizeCommandName* opcional, el marco de trabajo agrega un elemento **más comandos** a la lista de comandos del menú desplegable de la barra de herramientas de acceso rápido (Qat) que requiere la definición de un controlador de comandos secundario.</span><span class="sxs-lookup"><span data-stu-id="6976c-126">In addition to the basic Command handler for primary Quick Access Toolbar (QAT) functionality, declaring the optional *CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element attribute causes the framework to add a **More Commands** item to the Command list of the Quick Access Toolbar (QAT) drop-down menu that requires a secondary Command handler be defined.</span></span>

<span data-ttu-id="6976c-127">Para mantener la coherencia entre las aplicaciones de la cinta, se recomienda que el controlador de comandos *CustomizeCommandName* inicie un cuadro de diálogo de personalización de la barra de herramientas de acceso rápido (Qat).</span><span class="sxs-lookup"><span data-stu-id="6976c-127">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a Quick Access Toolbar (QAT) customization dialog.</span></span> <span data-ttu-id="6976c-128">Dado que el marco de cinta solo proporciona el punto de inicio en la interfaz de usuario, la aplicación es la única responsable de proporcionar la implementación del cuadro de diálogo de personalización cuando se recibe la notificación de devolución de llamada para este comando.</span><span class="sxs-lookup"><span data-stu-id="6976c-128">Because the Ribbon framework only provides the launching point in the UI, the application is solely responsible for providing the customization dialog implementation when the callback notification for this Command is received.</span></span>

<span data-ttu-id="6976c-129">En la captura de pantalla siguiente se muestra un menú desplegable de la barra de herramientas de acceso rápido (QAT) con el elemento de comando **más comandos** .</span><span class="sxs-lookup"><span data-stu-id="6976c-129">The following screen shot shows a Quick Access Toolbar (QAT) drop-down menu with the **More Commands** Command item.</span></span>

![captura de pantalla de un menú Qat con los comandos más... elemento de comando.](images/markup/qat-customizecommandname.png)

<span data-ttu-id="6976c-131">La lista de valores predeterminados de aplicación de la barra de herramientas de acceso rápido (QAT) se especifica mediante la propiedad [QuickAccessToolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) , que identifica una lista predeterminada de comandos recomendados, todos ellos en el menú desplegable barra de herramientas de acceso rápido (Qat).</span><span class="sxs-lookup"><span data-stu-id="6976c-131">The application defaults list for the Quick Access Toolbar (QAT) is specified through the [QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) property which identifies a default list of recommended Commands, all of which are listed in the Quick Access Toolbar (QAT) drop-down menu.</span></span>

<span data-ttu-id="6976c-132">Para mostrar los comandos de la lista de valores predeterminados de la aplicación en la barra de herramientas de acceso rápido (QAT), el atributo *ApplicationDefaults. isChecked* de cada elemento del control debe tener un valor de `true` .</span><span class="sxs-lookup"><span data-stu-id="6976c-132">To display Commands from the application defaults list in the Quick Access Toolbar (QAT) toolbar, the *ApplicationDefaults.IsChecked* attribute of each control element must have a value of `true`.</span></span> <span data-ttu-id="6976c-133">En las imágenes anteriores se muestran los resultados de establecer este atributo en `true` para los comandos **Guardar**, **Deshacer** y **rehacer** .</span><span class="sxs-lookup"><span data-stu-id="6976c-133">The preceding images show the results of setting this attribute to `true` for the **Save**, **Undo**, and **Redo** Commands.</span></span>

<span data-ttu-id="6976c-134">[QuickAccessToolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) admite tres tipos de controles de la cinta de opciones: [botón](windowsribbon-controls-button.md), [botón de alternancia](windowsribbon-controls-togglebutton.md)y [casilla](windowsribbon-controls-checkbox.md).</span><span class="sxs-lookup"><span data-stu-id="6976c-134">[QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) supports three types of Ribbon controls: [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), and [Check Box](windowsribbon-controls-checkbox.md).</span></span>

> [!Note]
> <span data-ttu-id="6976c-135">Windows 8 y versiones más recientes: se admiten todos los controles basados en la galería ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)y [DropDownGallery](windowsribbon-element-dropdowngallery.md)).</span><span class="sxs-lookup"><span data-stu-id="6976c-135">Windows 8 and newer: All gallery-based controls are supported ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md), and [DropDownGallery](windowsribbon-element-dropdowngallery.md)).</span></span>
>
> <span data-ttu-id="6976c-136">Los elementos de un control de Galería pueden admitir el resaltado al mantener el mouse.</span><span class="sxs-lookup"><span data-stu-id="6976c-136">Items in a gallery control can support highlighting on hover.</span></span> <span data-ttu-id="6976c-137">Para admitir el resaltado del mouse, la Galería debe ser una galería de elementos y utilizar un [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) de tipo [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).</span><span class="sxs-lookup"><span data-stu-id="6976c-137">To support hover highlighting, the gallery must be an items gallery and use a [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) of type [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).</span></span>

<span data-ttu-id="6976c-138">En el ejemplo siguiente se muestra el marcado básico de un elemento [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="6976c-138">The following example demonstrates the basic markup for a [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

<span data-ttu-id="6976c-139">En esta sección de código se muestran las declaraciones de comando para un elemento de [barra de herramientas de acceso rápido (Qat)](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="6976c-139">This section of code shows the Command declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

<span data-ttu-id="6976c-140">En esta sección de código se muestran las declaraciones de control para un elemento de [barra de herramientas de acceso rápido (Qat)](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="6976c-140">This section of code shows the control declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```

### <a name="code"></a><span data-ttu-id="6976c-141">Código</span><span class="sxs-lookup"><span data-stu-id="6976c-141">Code</span></span>

<span data-ttu-id="6976c-142">La aplicación de marco de cinta debe proporcionar un método de devolución de llamada del controlador de comandos para manipular la barra de herramientas de acceso rápido (QAT).</span><span class="sxs-lookup"><span data-stu-id="6976c-142">The Ribbon framework application must provide a Command handler callback method to manipulate the Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="6976c-143">Este controlador funciona de manera similar a los controladores de la galería de comandos, salvo que la barra de herramientas de acceso rápido (QAT) no admite categorías.</span><span class="sxs-lookup"><span data-stu-id="6976c-143">This handler works in a similar fashion to Command gallery handlers, except that the Quick Access Toolbar (QAT) does not support categories.</span></span> <span data-ttu-id="6976c-144">Para obtener más información, vea [trabajar con galerías](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="6976c-144">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="6976c-145">La colección de comandos de la barra de herramientas de acceso rápido (QAT) se recupera como un objeto [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) a través de la clave de la propiedad de la [interfaz de usuario \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) .</span><span class="sxs-lookup"><span data-stu-id="6976c-145">The Quick Access Toolbar (QAT) Command collection is retrieved as an [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span> <span data-ttu-id="6976c-146">Agregar comandos a la barra de herramientas de acceso rápido (QAT) en tiempo de ejecución se consigue agregando un objeto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) a **IUICollection**.</span><span class="sxs-lookup"><span data-stu-id="6976c-146">Adding Commands to the Quick Access Toolbar (QAT) at run time is accomplished by adding an [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object to the **IUICollection**.</span></span>

<span data-ttu-id="6976c-147">A diferencia de las galerías de comandos, una propiedad de tipo de comando ([UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) no es necesaria para el objeto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) de la barra de herramientas de acceso rápido (Qat).</span><span class="sxs-lookup"><span data-stu-id="6976c-147">Unlike Command galleries, a command type property ([UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) is not required for the Quick Access Toolbar (QAT) [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object.</span></span> <span data-ttu-id="6976c-148">Sin embargo, el comando debe existir en la cinta o en la lista de valores predeterminados de la aplicación de la barra de herramientas de acceso rápido (QAT). no se puede crear un nuevo comando en tiempo de ejecución y agregarlo a la barra de herramientas de acceso rápido (QAT).</span><span class="sxs-lookup"><span data-stu-id="6976c-148">However, the Command must exist in the ribbon or Quick Access Toolbar (QAT) application defaults list; a new Command cannot be created at run time and added to the Quick Access Toolbar (QAT).</span></span>

> [!Note]  
> <span data-ttu-id="6976c-149">La aplicación de cinta no puede reemplazar la barra de herramientas de acceso rápido (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) por un objeto de colección personalizado derivado de IEnumUnknown.</span><span class="sxs-lookup"><span data-stu-id="6976c-149">The Ribbon application cannot replace the Quick Access Toolbar (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) with a custom collection object derived from IEnumUnknown.</span></span>

<span data-ttu-id="6976c-150">En el ejemplo siguiente se muestra una implementación básica del controlador de comandos de la barra de herramientas de acceso rápido (QAT).</span><span class="sxs-lookup"><span data-stu-id="6976c-150">The following example demonstrates a basic Quick Access Toolbar (QAT) Command handler implementation.</span></span>

```C++
/* QAT COMMAND HANDLER IMPLEMENTATION */
class CQATCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
  public:
    BEGIN_COM_MAP(CQATCommandHandler)
      COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    // QAT command handler's Execute method
    STDMETHODIMP Execute(UINT nCmdID,
                         UI_EXECUTIONVERB verb, 
                         const PROPERTYKEY* key,
                         const PROPVARIANT* ppropvarValue,
                         IUISimplePropertySet* pCommandExecutionProperties)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(verb);
      UNREFERENCED_PARAMETER(ppropvarValue);
      UNREFERENCED_PARAMETER(pCommandExecutionProperties);

      // Do not expect Execute callback for a QAT command
      return E_NOTIMPL;
    }

    // QAT command handler's UpdateProperty method
    STDMETHODIMP UpdateProperty(UINT nCmdID,
                                REFPROPERTYKEY key,
                                const PROPVARIANT* ppropvarCurrentValue,
                                PROPVARIANT* ppropvarNewValue)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(ppropvarNewValue);

      HRESULT hr = E_NOTIMPL;

      if (key == UI_PKEY_ItemsSource)
      {
        ATLASSERT(ppropvarCurrentValue->vt == VT_UNKNOWN);

        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        UINT nCount;
        if (SUCCEEDED(hr = spCollection->GetCount(&nCount)))
        {
          if (nCount == 0)
          {
            // If the current Qat list is empty, then we will add a few items here.
            UINT commands[] =  { cmdSave, cmdUndo};

            int count = _countof(commands);

            for (int i = 0; i < count; i++)
            {
              PROPERTYKEY keys[1] = {UI_PKEY_CommandId};
              CComObject<CItemProperties> *pItem = NULL;
              if (SUCCEEDED(CComObject<CItemProperties>::CreateInstance(&pItem)))
              {
                PROPVARIANT vars[1];

                InitPropVariantFromUInt32(commands[i], &vars[0]);

                pItem->Initialize(NULL, _countof(vars), keys, vars);

                CComPtr<IUnknown> spUnknown;
                pItem->QueryInterface(&spUnknown);
                spCollection->Add(spUnknown);
                            
                FreePropVariantArray(_countof(vars), vars);
              }
            }
          }
          else
          {
            // Do nothing if the Qat list is not empty.
            // Return S_FALSE to indicate the callback succeeded.
            return S_FALSE; 
          }
        }
      }
    return hr;
  }
};
```

## <a name="qat-persistence"></a><span data-ttu-id="6976c-151">Persistencia de QAT</span><span class="sxs-lookup"><span data-stu-id="6976c-151">QAT Persistence</span></span>

<span data-ttu-id="6976c-152">Los elementos de comando y la configuración de la barra de herramientas de acceso rápido (QAT) pueden persistir en las sesiones de la aplicación mediante las funciones [IUIRibbon:: SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) y [IUIRibbon:: LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="6976c-152">Quick Access Toolbar (QAT) Command items and settings can be persisted across application sessions using the [IUIRibbon::SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) and [IUIRibbon::LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) functions.</span></span> <span data-ttu-id="6976c-153">Para obtener más información, consulte [conservar el estado de la cinta](ribbon-statepersistence.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="6976c-153">For more information, see [Persisting Ribbon State](ribbon-statepersistence.md).</span></span>

## <a name="quick-access-toolbar-properties"></a><span data-ttu-id="6976c-154">Propiedades de la barra de herramientas de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="6976c-154">Quick Access Toolbar Properties</span></span>

<span data-ttu-id="6976c-155">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de barra de herramientas de acceso rápido (Qat).</span><span class="sxs-lookup"><span data-stu-id="6976c-155">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Quick Access Toolbar (QAT) control.</span></span>

<span data-ttu-id="6976c-156">Normalmente, se actualiza una propiedad de barra de herramientas de acceso rápido (QAT) en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [IUIFramework:: InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="6976c-156">Typically, a Quick Access Toolbar (QAT) property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [IUIFramework::InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="6976c-157">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [IUICommandHandler:: UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="6976c-157">The invalidation event is handled, and the property updates defined, by the [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="6976c-158">No se ejecuta el método de devolución de llamada [IUICommandHandler:: UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="6976c-158">The [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="6976c-159">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="6976c-159">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="6976c-160">En algunos casos, una propiedad se puede recuperar a través del método [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [IUIFramework:: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="6976c-160">In some cases, a property can be retrieved through the [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

<span data-ttu-id="6976c-161">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de la barra de herramientas de acceso rápido (QAT).</span><span class="sxs-lookup"><span data-stu-id="6976c-161">The following table lists the property keys that are associated with the Quick Access Toolbar (QAT) control.</span></span>

| <span data-ttu-id="6976c-162">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="6976c-162">Property Key</span></span> | <span data-ttu-id="6976c-163">Notas</span><span class="sxs-lookup"><span data-stu-id="6976c-163">Notes</span></span> |
|---|---|
| [<span data-ttu-id="6976c-164">UI \_ PKEY \_ ItemsSource</span><span class="sxs-lookup"><span data-stu-id="6976c-164">UI\_PKEY\_ItemsSource</span></span>](windowsribbon-reference-properties-uipkey-itemssource.md) | <span data-ttu-id="6976c-165">Admite [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (no es compatible con [IUIFramework:: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) devuelve un puntero a un objeto IUICollection que representa los comandos de Qat.</span><span class="sxs-lookup"><span data-stu-id="6976c-165">Supports [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (does not support [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)).[IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) returns a pointer to an IUICollection object that represents the commands in the QAT.</span></span> <span data-ttu-id="6976c-166">Cada comando se identifica mediante su identificador de comando, que se obtiene llamando al método [IUISimplePropertySet:: GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) y pasando la interfaz de usuario de la clave de propiedad [ \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md).</span><span class="sxs-lookup"><span data-stu-id="6976c-166">Each Command is identified by its Command ID, which is obtained by calling the [IUISimplePropertySet::GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method and passing in the property key [UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md).</span></span> |

<span data-ttu-id="6976c-167">No hay claves de propiedad asociadas con el elemento de comando **más comandos** del menú desplegable de la barra de herramientas de acceso rápido (Qat)</span><span class="sxs-lookup"><span data-stu-id="6976c-167">There are no property keys associated with the **More Commands** Command item of the Quick Access Toolbar (QAT) drop-down menu</span></span>

## <a name="related-topics"></a><span data-ttu-id="6976c-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6976c-168">Related topics</span></span>

- [<span data-ttu-id="6976c-169">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="6976c-169">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
- [<span data-ttu-id="6976c-170">Elemento de marcado QuickAccessToolbar</span><span class="sxs-lookup"><span data-stu-id="6976c-170">QuickAccessToolbar markup element</span></span>](windowsribbon-element-quickaccesstoolbar.md)