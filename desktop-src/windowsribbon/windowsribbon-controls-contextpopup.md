---
title: Elemento emergente de contexto
description: Un elemento Popup de contexto es el control principal en la vista ContextPopup del marco Windows cinta de opciones.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15424aa8b2b82580218eb3663e4b157bce321fdde027e03101ce2cf38626aac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964423"
---
# <a name="context-popup"></a>Elemento emergente de contexto

Un elemento Popup de contexto es el control principal en [**la vista ContextPopup**](windowsribbon-element-contextpopup.md) del marco Windows cinta de opciones. Se trata de un sistema de menús contextuales enriquecido que el marco solo expone como una extensión a una implementación de cinta de opciones; el marco no expone el elemento emergente de contexto como control independiente.

-   [Componentes del elemento emergente de contexto](#context-popup)
-   [Implementar el elemento emergente de contexto](#implement-the-context-popup)
    -   [marcado](#markup)
    -   [Código](#code)
-   [Propiedades emergentes de contexto](#context-popup-properties)
-   [Temas relacionados](#related-topics)

## <a name="components-of-the-context-popup"></a>Componentes del elemento emergente de contexto

Context Popup es un contenedor lógico para el menú contextual y Mini-Toolbar secundarios que se exponen a través de los elementos de marcado [**ContextMenu**](windowsribbon-element-contextmenu.md) y [**MiniToolbar,**](windowsribbon-element-minitoolbar.md) respectivamente:

-   [**ContextMenu**](windowsribbon-element-contextmenu.md) expone un menú de comandos y galerías.
-   [**MiniToolbar expone**](windowsribbon-element-minitoolbar.md) una barra de herramientas flotante de varios comandos, galerías y controles complejos, como el [control](windowsribbon-controls-fontcontrol.md) de fuentes y el [cuadro combinado](windowsribbon-controls-combobox.md).

Cada subcontrol puede aparecer como máximo una vez en un elemento emergente de contexto.

En la captura de pantalla siguiente se muestra el elemento emergente de contexto y sus subdominios constituyentes.

![captura de pantalla con llamadas que muestran los componentes contextuales de la interfaz de usuario de la cinta de opciones.](images/controls/contextpopup.png)

Context Popup es puramente conceptual y no expone ninguna funcionalidad de interfaz de usuario propiamente dicha, como el posicionamiento o el tamaño.

> [!Note]  
> La ventana emergente de contexto se muestra normalmente haciendo clic con el botón derecho en el mouse (o a través del método abreviado de teclado MAYÚS+F10) en un objeto de interés. Sin embargo, la aplicación define los pasos necesarios para mostrar el elemento emergente de contexto.

 

## <a name="implement-the-context-popup"></a>Implementar el elemento emergente de contexto

De forma similar a otros controles del marco de Windows Ribbon, context popup se implementa a través de un componente de marcado que especifica sus detalles de presentación y un componente de código que rige su funcionalidad.

En la tabla siguiente se enumeran los controles admitidos por cada subcontrol emergente de contexto.



| Control                                                                  | Mini-Toolbar | Menú contextual |
|--------------------------------------------------------------------------|--------------|--------------|
| [Botón](windowsribbon-controls-button.md)                              | x            | x            |
| [Casilla](windowsribbon-controls-checkbox.md)                         | x            | x            |
| [Cuadro combinado](windowsribbon-controls-combobox.md)                         | x            |              |
| [Botón desplegable](windowsribbon-controls-dropdownbutton.md)            | x            | x            |
| [Lista desplegable Selector de colores](windowsribbon-controls-dropdowncolorpicker.md) | x            | x            |
| [Galería desplegable](windowsribbon-controls-dropdowngallery.md)          | x            | x            |
| [Control de fuentes](windowsribbon-controls-fontcontrol.md)                   | x            |              |
| [Botón Ayuda](windowsribbon-controls-helpbutton.md)                     |              |              |
| [Galería en la cinta de opciones](windowsribbon-controls-inribbongallery.md)          |              |              |
| [Spinner](windowsribbon-controls-spinner.md)                            |              |              |
| [Botón De división](windowsribbon-controls-splitbutton.md)                   | x            | x            |
| [Galería de botones de división](windowsribbon-controls-splitbuttongallery.md)    | x            | x            |
| [Botón De alternancia](windowsribbon-controls-togglebutton.md)                 | x            | x            |



 

### <a name="markup"></a>marcado

Cada subcontrol emergente de contexto debe declararse individualmente en el marcado.

### <a name="mini-toolbar"></a>Mini-Toolbar

Al agregar controles a una mini barra de herramientas emergente de contexto, se deben tener en cuenta las dos recomendaciones siguientes:

-   Los controles deben ser muy reconocibles y proporcionar una funcionalidad obvia. La familiaridad es clave, ya que las etiquetas y la información sobre herramientas no se exponen para Mini-Toolbar controles.
-   Cada comando expuesto por un control debe presentarse en otra parte de la interfaz de usuario de la cinta de opciones. El Mini-Toolbar no admite la navegación mediante el teclado.

En el ejemplo siguiente se muestra el marcado básico para un [**elemento MiniToolbar**](windowsribbon-element-minitoolbar.md) que contiene tres [controles Button.](windowsribbon-controls-button.md)

> [!Note]  
> Se [**especifica un elemento MenuGroup**](windowsribbon-element-menugroup.md) para cada fila de controles de la barra de herramientas pequeña.

 


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

En el ejemplo siguiente se muestra el marcado básico para un [**elemento ContextMenu**](windowsribbon-element-contextmenu.md) que contiene tres [controles Button.](windowsribbon-controls-button.md)

> [!Note]  
> Cada conjunto de controles del [**elemento MenuGroup**](windowsribbon-element-menugroup.md) está separado por una barra horizontal en el menú contextual.

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



Aunque un elemento Popup de contexto puede contener como máximo uno de cada subcontrol, varias declaraciones de elementos [**ContextMenu**](windowsribbon-element-contextmenu.md) y [**MiniToolbar**](windowsribbon-element-minitoolbar.md) en el marcado de la cinta de opciones son válidas. Esto permite que una aplicación admita varias combinaciones de menú contextual y controles Mini-Toolbar, en función de los criterios definidos por la aplicación, como el contexto del área de trabajo.

Para obtener más información, vea el [**elemento ContextMap.**](windowsribbon-element-contextmap.md)

En el ejemplo siguiente se muestra el marcado básico para el [**elemento ContextPopup.**](windowsribbon-element-contextpopup.md)


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

Para invocar un elemento Popup de contexto, se llama al método [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) cuando la ventana de nivel superior de la aplicación ribbon recibe una notificación \_ CONTEXTMENU de WM.

En este ejemplo se muestra cómo controlar la notificación WM CONTEXTMENU en el \_ método WndProc() de la aplicación Ribbon.


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



En el ejemplo siguiente se muestra cómo una aplicación de cinta de opciones puede mostrar context popup en una ubicación de pantalla específica mediante el [**método IUIContextualUI::ShowAtLocation.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation)

GetCurrentContext() tiene un valor de `cmdContextMap` tal como se define en el ejemplo de marcado anterior.

g \_ pApplication es una referencia a la [**interfaz IUIFramework.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)


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



La referencia a [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) se puede liberar antes de que se descarte context popup, como se muestra en el ejemplo anterior. Sin embargo, la referencia debe liberarse en algún momento para evitar pérdidas de memoria.

> [!Caution]  
> El Mini-Toolbar tiene un efecto de atenuación integrado que se basa en la proximidad del puntero del mouse. Por este motivo, se recomienda que el Mini-Toolbar se muestre lo más cerca posible del puntero del mouse. De lo contrario, debido a los mecanismos de visualización en conflicto, Mini-Toolbar no se representará según lo previsto.

 

## <a name="context-popup-properties"></a>Propiedades emergentes de contexto

No hay claves de propiedad asociadas al control Context Popup.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)
</dt> <dt>

[Ejemplo contextPopup](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 