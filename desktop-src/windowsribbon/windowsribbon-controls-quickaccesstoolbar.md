---
title: Barra de herramientas de acceso rápido
description: La barra de herramientas de acceso rápido (QAT) es una barra de herramientas pequeña y personalizable que expone un conjunto de comandos especificados por la aplicación o seleccionados por el usuario.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a50d562477e5c626d2d2bffa8ee5e0ecc84919
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251733"
---
# <a name="quick-access-toolbar"></a>Barra de herramientas de acceso rápido

La barra de herramientas de acceso rápido (QAT) es una barra de herramientas pequeña y personalizable que expone un conjunto de comandos especificados por la aplicación o seleccionados por el usuario.

- [Introducción](#introduction)
- [Implementación de la barra de herramientas de acceso rápido](#implement-the-quick-access-toolbar)
  - [marcado](#markup)
  - [Código](#code)
- [Persistencia de QAT](#qat-persistence)
- [Propiedades de la barra de herramientas de acceso rápido](#quick-access-toolbar-properties)
- [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

De forma predeterminada, la barra de herramientas de acceso rápido (QAT) se encuentra en la barra de título de la ventana de la aplicación, pero se puede configurar para mostrarse debajo de la cinta de opciones. Además de exponer comandos, la barra de herramientas de acceso rápido (QAT) también incluye un menú desplegable personalizable que contiene el conjunto completo de comandos predeterminados de la barra de herramientas de acceso rápido (QAT) (ya sea oculto o mostrado en la barra de herramientas de acceso rápido (QAT)) y un conjunto de opciones de barra de herramientas de acceso rápido (QAT) y cinta de opciones.

En la siguiente captura de pantalla se muestra un ejemplo de la barra de herramientas de acceso rápido (QAT) de la cinta de opciones.

![captura de pantalla del qat en la cinta de microsoft paint.](images/markup/qat-and-menu.png)

La barra de herramientas de acceso rápido (QAT) consta de una combinación de hasta 20 comandos especificados por la aplicación (conocidos como la lista de valores predeterminados de la aplicación) o seleccionados por el usuario. La barra de herramientas de acceso rápido (QAT) puede contener comandos únicos que no están disponibles en otra parte de la interfaz de usuario de la cinta de opciones.

> [!Note]
> Aunque casi todos los controles de la cinta de opciones permiten agregar su comando asociado [a](windowsribbon-controls-contextpopup.md) la barra de herramientas de acceso rápido (QAT) a través del menú contextual que se muestra en la siguiente captura de pantalla, los comandos expuestos en un elemento emergente de contexto no proporcionan este menú contextual.
>
> ![captura de pantalla del menú contextual del comando en la cinta de microsoft paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a>Implementación de la barra de herramientas de acceso rápido

Como con todos los controles del marco de Windows Ribbon, aprovechar al máximo la barra de herramientas de acceso rápido (QAT) requiere un componente de marcado que controla su presentación dentro de la cinta de opciones y un componente de código que rige su funcionalidad.

### <a name="markup"></a>marcado

El control Barra de herramientas de acceso rápido (QAT) se declara y se asocia a un identificador de comando en el marcado a través [del elemento QuickAccessToolbar.](windowsribbon-element-quickaccesstoolbar.md) El identificador de comando se usa para identificar y enlazar la barra de herramientas de acceso rápido (QAT) a un controlador de comandos definido por la aplicación.

Además del controlador de comandos básico para la funcionalidad principal de la barra de herramientas de acceso rápido (QAT), declarar el atributo opcional del elemento *CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) hace que el marco agregue un elemento Más comandos **a** la lista de comandos del menú desplegable Barra de herramientas de acceso rápido (QAT) que requiere que se defina un controlador de comandos secundario.

Para mantener la coherencia entre las aplicaciones de la cinta de opciones, se recomienda que el controlador de comandos *CustomizeCommandName* inicie un cuadro de diálogo de personalización de la barra de herramientas de acceso rápido (QAT). Dado que el marco de la cinta de opciones solo proporciona el punto de inicio en la interfaz de usuario, la aplicación es la única responsable de proporcionar la implementación del cuadro de diálogo de personalización cuando se recibe la notificación de devolución de llamada para este comando.

En la siguiente captura de pantalla se muestra un menú desplegable barra de herramientas de acceso rápido (QAT) con el **elemento Comando** Más comandos.

![captura de pantalla de un menú qat con más comandos... elemento de comando.](images/markup/qat-customizecommandname.png)

La lista de valores predeterminados de la aplicación para la barra de herramientas de acceso rápido (QAT) se especifica a través de la propiedad [QuickAccessToolbar.ApplicationDefaults,](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) que identifica una lista predeterminada de comandos recomendados, todos los cuales aparecen en el menú desplegable Barra de herramientas de acceso rápido (QAT).

Para mostrar comandos de la lista de valores predeterminados de la aplicación en la barra de herramientas de la barra de herramientas de acceso rápido (QAT), el atributo *ApplicationDefaults.IsChecked* de cada elemento de control debe tener un valor de `true` . En las imágenes anteriores se muestran los resultados de establecer este atributo en para los comandos `true` **Guardar,** Deshacer **y Rehacer.** 

[QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) admite tres tipos de controles de cinta: [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md)y [Check Box](windowsribbon-controls-checkbox.md).

> [!Note]
> Windows 8 y versiones más recientes: se admiten todos los controles basados en la galería[(ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery,](windowsribbon-element-inribbongallery.md) [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)y [DropDownGallery).](windowsribbon-element-dropdowngallery.md)
>
> Los elementos de un control de galería pueden admitir el resaltado al mantener el puntero. Para admitir el resaltado del mouse, la galería debe ser una galería de elementos y usar [flowMenuLayout](windowsribbon-element-flowmenulayout.md) de tipo [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).

En el ejemplo siguiente se muestra el marcado básico para [un elemento QuickAccessToolbar.](windowsribbon-element-quickaccesstoolbar.md)

En esta sección de código se muestran las declaraciones de comando para un elemento de la barra de herramientas de acceso rápido [(QAT).](windowsribbon-element-quickaccesstoolbar.md)

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

En esta sección de código se muestran las declaraciones de control para un elemento de la barra de herramientas de acceso rápido [(QAT).](windowsribbon-element-quickaccesstoolbar.md)

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

### <a name="code"></a>Código

La aplicación de marco de la cinta de opciones debe proporcionar un método de devolución de llamada de controlador de comandos para manipular la barra de herramientas de acceso rápido (QAT). Este controlador funciona de forma similar a los controladores de la galería de comandos, salvo que la barra de herramientas de acceso rápido (QAT) no admite categorías. Para obtener más información, [vea Trabajar con galerías](ribbon-controls-galleries.md).

La colección Comandos de la barra de herramientas de acceso rápido (QAT) se recupera como un [objeto IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) a través de la clave de [propiedad \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) de la interfaz de usuario. Para agregar comandos a la barra de herramientas de acceso rápido (QAT) en tiempo de ejecución, se agrega un objeto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) a **IUICollection**.

A diferencia de las galerías de comandos, no se requiere una propiedad de tipo de comando[(UI \_ PKEY \_ CommandType)](windowsribbon-reference-properties-uipkey-commandtype.md)para el objeto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) de la barra de herramientas de acceso rápido (QAT). Sin embargo, el comando debe existir en la cinta de opciones o en la lista de valores predeterminados de la aplicación Barra de herramientas de acceso rápido (QAT); No se puede crear un nuevo comando en tiempo de ejecución y agregarlo a la barra de herramientas de acceso rápido (QAT).

> [!Note]  
> La aplicación ribbon no puede reemplazar la [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) de la barra de herramientas de acceso rápido (QAT) por un objeto de colección personalizado derivado de IEnumUnknown.

En el ejemplo siguiente se muestra una implementación básica del controlador de comandos de la barra de herramientas de acceso rápido (QAT).

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

## <a name="qat-persistence"></a>Persistencia de QAT

La configuración y los elementos de comandos de la barra de herramientas de acceso rápido (QAT) se pueden conservar en las sesiones de aplicación mediante las funciones [IUIRibbon::SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e [IUIRibbon::LoadSettingsFromStream.](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) Para obtener más información, vea [Persisting Ribbon State](ribbon-statepersistence.md).

## <a name="quick-access-toolbar-properties"></a>Propiedades de la barra de herramientas de acceso rápido

El marco de la cinta de opciones define una colección de [claves de propiedad para](windowsribbon-reference-properties.md) el control Barra de herramientas de acceso rápido (QAT).

Normalmente, una propiedad barra de herramientas de acceso rápido (QAT) se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [IUIFramework::InvalidateUICommand.](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) El método de devolución de llamada [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) controla el evento de invalidación y las actualizaciones de propiedad definidas.

El método de devolución de llamada [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación consulta un valor de propiedad actualizado, hasta que el marco de trabajo requiera la propiedad . Por ejemplo, cuando se activa una pestaña y se muestra un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar mediante el método [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [IUIFramework::SetUICommandProperty.](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

En la tabla siguiente se enumeran las claves de propiedad asociadas al control barra de herramientas de acceso rápido (QAT).

| Clave de propiedad | Notas |
|---|---|
| [UI \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) | Admite [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (no admite [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) devuelve un puntero a un objeto IUICollection que representa los comandos del QAT. Cada comando se identifica mediante su identificador de comando, que se obtiene llamando al método [IUISimplePropertySet::GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) y pasando la clave de propiedad [ \_ UI PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md). |

No hay claves de propiedad **asociadas** al elemento Comando Más comandos del menú desplegable Barra de herramientas de acceso rápido (QAT).

## <a name="related-topics"></a>Temas relacionados

- [Windows Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)
- [Elemento de marcado QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md)