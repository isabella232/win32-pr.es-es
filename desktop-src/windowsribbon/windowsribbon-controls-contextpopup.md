---
title: Cuadro emergente de contexto
description: Un elemento emergente de contexto es el control principal en la vista ContextPopup del marco de la cinta de opciones de Windows.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77441cc3cdcc9212d27d2230d76d2618f1831ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676423"
---
# <a name="context-popup"></a>Cuadro emergente de contexto

Un elemento emergente de contexto es el control principal en la [**vista ContextPopup**](windowsribbon-element-contextpopup.md) del marco de la cinta de opciones de Windows. Se trata de un sistema de menús contextuales enriquecido que solo expone el marco de trabajo como una extensión a una implementación de la cinta de opciones; el marco no expone el elemento emergente de contexto como control independiente.

-   [Componentes del elemento emergente de contexto](#context-popup)
-   [Implementar el elemento emergente de contexto](#implement-the-context-popup)
    -   [marcado](#markup)
    -   [Código](#code)
-   [Propiedades de elemento emergente de contexto](#context-popup-properties)
-   [Temas relacionados](#related-topics)

## <a name="components-of-the-context-popup"></a>Componentes del elemento emergente de contexto

El elemento emergente de contexto es un contenedor lógico para el menú contextual y Mini-Toolbar los subcontrols que se exponen a través de los elementos de marcado [**ContextMenu**](windowsribbon-element-contextmenu.md) y [**MiniToolbar**](windowsribbon-element-minitoolbar.md) , respectivamente:

-   El [**ContextMenu**](windowsribbon-element-contextmenu.md) expone un menú de comandos y galerías.
-   [**MiniToolbar**](windowsribbon-element-minitoolbar.md) expone una barra de herramientas flotante de varios comandos, galerías y controles complejos, como el [control de fuente](windowsribbon-controls-fontcontrol.md) y el [cuadro combinado](windowsribbon-controls-combobox.md).

Cada subcontrol puede aparecer como máximo una vez en una ventana emergente de contexto.

La siguiente captura de pantalla muestra el contexto emergente y sus subcontrols constituyentes.

![captura de pantalla con llamadas que muestran los componentes de interfaz de usuario contextual de la cinta.](images/controls/contextpopup.png)

El elemento emergente de contexto es puramente conceptual y no expone ninguna funcionalidad de la interfaz de usuario, como la posición o el ajuste de tamaño.

> [!Note]  
> La ventana emergente contextual se muestra normalmente al hacer clic con el botón secundario en el mouse (o mediante el método abreviado de teclado Mayús + F10) en un objeto de interés. Sin embargo, la aplicación define los pasos necesarios para mostrar el elemento emergente de contexto.

 

## <a name="implement-the-context-popup"></a>Implementar el elemento emergente de contexto

De forma similar a otros controles de marcos de cinta de Windows, el elemento emergente de contexto se implementa a través de un componente de marcado que especifica los detalles de presentación y un componente de código que rige su funcionalidad.

En la tabla siguiente se enumeran los controles que admite cada subcontrol emergente de contexto.



| Control                                                                  | Mini-Toolbar | Menú contextual |
|--------------------------------------------------------------------------|--------------|--------------|
| [Botón](windowsribbon-controls-button.md)                              | x            | x            |
| [Casilla de verificación](windowsribbon-controls-checkbox.md)                         | x            | x            |
| [Cuadro combinado](windowsribbon-controls-combobox.md)                         | x            |              |
| [Botón desplegable](windowsribbon-controls-dropdownbutton.md)            | x            | x            |
| [Selector de colores desplegables](windowsribbon-controls-dropdowncolorpicker.md) | x            | x            |
| [Galería desplegable](windowsribbon-controls-dropdowngallery.md)          | x            | x            |
| [Control de fuente](windowsribbon-controls-fontcontrol.md)                   | x            |              |
| [Botón ayuda](windowsribbon-controls-helpbutton.md)                     |              |              |
| [En la galería de la cinta de opciones](windowsribbon-controls-inribbongallery.md)          |              |              |
| [Spinner](windowsribbon-controls-spinner.md)                            |              |              |
| [Botón de expansión](windowsribbon-controls-splitbutton.md)                   | x            | x            |
| [Galería de botones de expansión](windowsribbon-controls-splitbuttongallery.md)    | x            | x            |
| [Botón de alternancia](windowsribbon-controls-togglebutton.md)                 | x            | x            |



 

### <a name="markup"></a>marcado

Cada subcontrol emergente de contexto debe declararse individualmente en el marcado.

### <a name="mini-toolbar"></a>Mini-Toolbar

Al agregar controles a una minibarra de herramientas emergente de contexto, se deben tener en cuenta las dos recomendaciones siguientes:

-   Los controles deben ser muy reconocibles y proporcionar una funcionalidad obvia. La familiaridad es la clave, ya que las etiquetas e información sobre herramientas no se exponen para los controles de Mini-Toolbar.
-   Cada comando expuesto por un control se debe presentar en otro lugar de la interfaz de usuario de la cinta de opciones. La Mini-Toolbar no admite la navegación con el teclado.

En el ejemplo siguiente se muestra el marcado básico de un elemento [**MiniToolbar**](windowsribbon-element-minitoolbar.md) que contiene tres controles [Button](windowsribbon-controls-button.md) .

> [!Note]  
> Se especifica un elemento [**MenuGroup**](windowsribbon-element-menugroup.md) para cada fila de controles de la minibarra de herramientas.

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a>Menú contextual

En el ejemplo siguiente se muestra el marcado básico para un elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) que contiene tres controles de [botón](windowsribbon-controls-button.md) .

> [!Note]  
> Cada conjunto de controles del elemento [**MenuGroup**](windowsribbon-element-menugroup.md) está separado por una barra horizontal en el menú contextual.

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



Aunque un elemento emergente de contexto puede contener como máximo uno de cada subcontrol, son válidos varias declaraciones de elementos [**ContextMenu**](windowsribbon-element-contextmenu.md) y [**MiniToolbar**](windowsribbon-element-minitoolbar.md) en el marcado de la cinta de opciones. Esto permite que una aplicación admita varias combinaciones de controles de menú contextual y Mini-Toolbar, en función de los criterios definidos por la aplicación, como el contexto del área de trabajo.

Para obtener más información, vea el elemento [**ContextMap**](windowsribbon-element-contextmap.md) .

En el ejemplo siguiente se muestra el marcado básico para el elemento [**ContextPopup**](windowsribbon-element-contextpopup.md) .


```C++
<ContextPopup>
  <ContextPopup.MiniToolbars>
    <MiniToolbar Name="MiniToolbar">
      <MenuGroup>
        <Button CommandName="cmdButton1" />
        <Button CommandName="cmdButton2" />
        <Button CommandName="cmdButton3" />
      </MenuGroup>
    </MiniToolbar>
  </ContextPopup.MiniToolbars>
  <ContextPopup.ContextMenus>
    <ContextMenu Name="ContextMenu">
      <MenuGroup>
        <Button CommandName="cmdCut" />
        <Button CommandName="cmdCopy" />
        <Button CommandName="cmdPaste" />
      </MenuGroup>
    </ContextMenu>
  </ContextPopup.ContextMenus>
  <ContextPopup.ContextMaps>
    <ContextMap CommandName="cmdContextMap" ContextMenu="ContextMenu" MiniToolbar="MiniToolbar"/>
  </ContextPopup.ContextMaps>
</ContextPopup>
```



### <a name="code"></a>Código

Para invocar un elemento emergente de contexto, se llama al método [**IUIContextualUI:: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) cuando la ventana de nivel superior de la aplicación de cinta recibe una notificación de CONTEXTMENU de WM \_ .

En este ejemplo se muestra cómo controlar la \_ notificación de CONTEXTMENU de WM en el método WndProc () de la aplicación de cinta.


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



En el ejemplo siguiente se muestra cómo una aplicación de la cinta de opciones puede mostrar el elemento emergente de contexto en una ubicación de pantalla específica mediante el método [**IUIContextualUI:: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) .

GetCurrentContext () tiene un valor de `cmdContextMap` tal y como se define en el ejemplo de marcación anterior.

g \_ pApplication es una referencia a la interfaz [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) .


```C++
HRESULT ShowContextualUI(POINT& ptLocation, HWND hWnd)
{
  GetDisplayLocation(ptLocation, hWnd);

  HRESULT hr = E_FAIL;

  IUIContextualUI* pContextualUI = NULL;
 
  if (SUCCEEDED(g_pFramework->GetView(
                                g_pApplication->GetCurrentContext(), 
                                IID_PPV_ARGS(&pContextualUI))))
  {
    hr = pContextualUI->ShowAtLocation(ptLocation.x, ptLocation.y);
    pContextualUI->Release();
  }

  return hr;
}
```



La referencia a [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) se puede liberar antes de que se descarte el elemento emergente de contexto, tal como se muestra en el ejemplo anterior. Sin embargo, se debe liberar la referencia en algún momento para evitar pérdidas de memoria.

> [!Caution]  
> El Mini-Toolbar tiene un efecto de atenuación integrado que se basa en la proximidad del puntero del mouse. Por esta razón, se recomienda que el Mini-Toolbar se muestre lo más cerca posible del puntero del mouse. De lo contrario, debido a los mecanismos de presentación conflictivos, es posible que el Mini-Toolbar no se represente de la manera esperada.

 

## <a name="context-popup-properties"></a>Propiedades de elemento emergente de contexto

No hay claves de propiedad asociadas al control emergente de contexto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Biblioteca de controles de Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[Ejemplo de ContextPopup](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 