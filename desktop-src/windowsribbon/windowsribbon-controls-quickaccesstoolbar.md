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
# <a name="quick-access-toolbar"></a>Barra de herramientas de acceso rápido

La barra de herramientas de acceso rápido (QAT) es una pequeña barra de herramientas personalizable que muestra un conjunto de comandos especificados por la aplicación o seleccionados por el usuario.

- [Introducción](#introduction)
- [Implementar la barra de herramientas de acceso rápido](#implement-the-quick-access-toolbar)
  - [marcado](#markup)
  - [Código](#code)
- [Persistencia de QAT](#qat-persistence)
- [Propiedades de la barra de herramientas de acceso rápido](#quick-access-toolbar-properties)
- [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

De forma predeterminada, la barra de herramientas de acceso rápido (QAT) se encuentra en la barra de título de la ventana de la aplicación, pero se puede configurar para que se muestre debajo de la cinta de opciones. Además de exponer comandos, la barra de herramientas de acceso rápido (QAT) también incluye un menú desplegable personalizable que contiene el conjunto completo de comandos predeterminados de la barra de herramientas de acceso rápido (QAT) (ya sea oculto o mostrado en la barra de herramientas de acceso rápido (QAT)) y un conjunto de opciones de la barra de herramientas de acceso rápido (QAT).

En la captura de pantalla siguiente se muestra un ejemplo de la barra de herramientas de acceso rápido de la cinta de opciones (QAT).

![captura de pantalla de Qat en la cinta de opciones de Microsoft Paint.](images/markup/qat-and-menu.png)

La barra de herramientas de acceso rápido (QAT) consta de una combinación de hasta 20 comandos especificados por la aplicación (conocida como lista de valores predeterminados de la aplicación) o seleccionados por el usuario. La barra de herramientas de acceso rápido (QAT) puede contener comandos únicos que no están disponibles en ningún otro lugar de la interfaz de usuario de la cinta de opciones.

> [!Note]
> Aunque casi todos los controles de la cinta de opciones permiten agregar su comando asociado a la barra de herramientas de acceso rápido (QAT) a través del menú contextual que se muestra en la siguiente captura de pantalla, los comandos expuestos en una [ventana emergente de contexto](windowsribbon-controls-contextpopup.md) no proporcionan este menú contextual.
>
> ![captura de pantalla del menú contextual de la cinta de opciones de Microsoft Paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a>Implementar la barra de herramientas de acceso rápido

Al igual que con todos los controles de marco de cinta de Windows, sacar el máximo partido de la barra de herramientas de acceso rápido (QAT) requiere un componente de marcado que controle su presentación dentro de la cinta de opciones y un componente de código que rija su funcionalidad.

### <a name="markup"></a>marcado

El control de barra de herramientas de acceso rápido (QAT) se declara y se asocia a un identificador de comando, en el marcado mediante el elemento [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) . El identificador de comando se usa para identificar y enlazar la barra de herramientas de acceso rápido (QAT) a un controlador de comandos definido por la aplicación.

Además del controlador de comandos básico para la funcionalidad principal de la barra de herramientas de acceso rápido (QAT), al declarar el atributo de elemento [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) de *CustomizeCommandName* opcional, el marco de trabajo agrega un elemento **más comandos** a la lista de comandos del menú desplegable de la barra de herramientas de acceso rápido (Qat) que requiere la definición de un controlador de comandos secundario.

Para mantener la coherencia entre las aplicaciones de la cinta, se recomienda que el controlador de comandos *CustomizeCommandName* inicie un cuadro de diálogo de personalización de la barra de herramientas de acceso rápido (Qat). Dado que el marco de cinta solo proporciona el punto de inicio en la interfaz de usuario, la aplicación es la única responsable de proporcionar la implementación del cuadro de diálogo de personalización cuando se recibe la notificación de devolución de llamada para este comando.

En la captura de pantalla siguiente se muestra un menú desplegable de la barra de herramientas de acceso rápido (QAT) con el elemento de comando **más comandos** .

![captura de pantalla de un menú Qat con los comandos más... elemento de comando.](images/markup/qat-customizecommandname.png)

La lista de valores predeterminados de aplicación de la barra de herramientas de acceso rápido (QAT) se especifica mediante la propiedad [QuickAccessToolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) , que identifica una lista predeterminada de comandos recomendados, todos ellos en el menú desplegable barra de herramientas de acceso rápido (Qat).

Para mostrar los comandos de la lista de valores predeterminados de la aplicación en la barra de herramientas de acceso rápido (QAT), el atributo *ApplicationDefaults. isChecked* de cada elemento del control debe tener un valor de `true` . En las imágenes anteriores se muestran los resultados de establecer este atributo en `true` para los comandos **Guardar**, **Deshacer** y **rehacer** .

[QuickAccessToolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) admite tres tipos de controles de la cinta de opciones: [botón](windowsribbon-controls-button.md), [botón de alternancia](windowsribbon-controls-togglebutton.md)y [casilla](windowsribbon-controls-checkbox.md).

> [!Note]
> Windows 8 y versiones más recientes: se admiten todos los controles basados en la galería ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)y [DropDownGallery](windowsribbon-element-dropdowngallery.md)).
>
> Los elementos de un control de Galería pueden admitir el resaltado al mantener el mouse. Para admitir el resaltado del mouse, la Galería debe ser una galería de elementos y utilizar un [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) de tipo [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).

En el ejemplo siguiente se muestra el marcado básico de un elemento [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) .

En esta sección de código se muestran las declaraciones de comando para un elemento de [barra de herramientas de acceso rápido (Qat)](windowsribbon-element-quickaccesstoolbar.md) .

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

En esta sección de código se muestran las declaraciones de control para un elemento de [barra de herramientas de acceso rápido (Qat)](windowsribbon-element-quickaccesstoolbar.md) .

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

La aplicación de marco de cinta debe proporcionar un método de devolución de llamada del controlador de comandos para manipular la barra de herramientas de acceso rápido (QAT). Este controlador funciona de manera similar a los controladores de la galería de comandos, salvo que la barra de herramientas de acceso rápido (QAT) no admite categorías. Para obtener más información, vea [trabajar con galerías](ribbon-controls-galleries.md).

La colección de comandos de la barra de herramientas de acceso rápido (QAT) se recupera como un objeto [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) a través de la clave de la propiedad de la [interfaz de usuario \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) . Agregar comandos a la barra de herramientas de acceso rápido (QAT) en tiempo de ejecución se consigue agregando un objeto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) a **IUICollection**.

A diferencia de las galerías de comandos, una propiedad de tipo de comando ([UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) no es necesaria para el objeto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) de la barra de herramientas de acceso rápido (Qat). Sin embargo, el comando debe existir en la cinta o en la lista de valores predeterminados de la aplicación de la barra de herramientas de acceso rápido (QAT). no se puede crear un nuevo comando en tiempo de ejecución y agregarlo a la barra de herramientas de acceso rápido (QAT).

> [!Note]  
> La aplicación de cinta no puede reemplazar la barra de herramientas de acceso rápido (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) por un objeto de colección personalizado derivado de IEnumUnknown.

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

Los elementos de comando y la configuración de la barra de herramientas de acceso rápido (QAT) pueden persistir en las sesiones de la aplicación mediante las funciones [IUIRibbon:: SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) y [IUIRibbon:: LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) . Para obtener más información, consulte [conservar el estado de la cinta](ribbon-statepersistence.md)de opciones.

## <a name="quick-access-toolbar-properties"></a>Propiedades de la barra de herramientas de acceso rápido

El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de barra de herramientas de acceso rápido (Qat).

Normalmente, se actualiza una propiedad de barra de herramientas de acceso rápido (QAT) en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [IUIFramework:: InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [IUICommandHandler:: UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

No se ejecuta el método de devolución de llamada [IUICommandHandler:: UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad. Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar a través del método [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [IUIFramework:: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de la barra de herramientas de acceso rápido (QAT).

| Clave de propiedad | Notas |
|---|---|
| [UI \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) | Admite [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (no es compatible con [IUIFramework:: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) devuelve un puntero a un objeto IUICollection que representa los comandos de Qat. Cada comando se identifica mediante su identificador de comando, que se obtiene llamando al método [IUISimplePropertySet:: GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) y pasando la interfaz de usuario de la clave de propiedad [ \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md). |

No hay claves de propiedad asociadas con el elemento de comando **más comandos** del menú desplegable de la barra de herramientas de acceso rápido (Qat)

## <a name="related-topics"></a>Temas relacionados

- [Biblioteca de controles de Windows Ribbon Framework](windowsribbon-controls-entry.md)
- [Elemento de marcado QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md)