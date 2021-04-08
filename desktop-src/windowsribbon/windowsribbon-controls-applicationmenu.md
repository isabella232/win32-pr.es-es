---
title: Menú de la aplicación
description: El menú aplicación es el menú principal de una aplicación que implementa el marco de la cinta de opciones de Windows.
ms.assetid: 5be93a5b-277b-44c1-be24-a0598a140bfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f57045daa35149e5fa074cb59e2f538c589b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904612"
---
# <a name="application-menu"></a>Menú de la aplicación

El menú aplicación es el menú principal de una aplicación que implementa el marco de la cinta de opciones de Windows.

-   [Introducción](#introduction)
-   [Componentes del menú aplicación](#components-of-the-application-menu)
    -   [Menú de aplicación MenuGroup](#application-menu-menugroup)
-   [Ajustar el tamaño del menú de la aplicación](#sizing-the-application-menu)
-   [Propiedades del menú de la aplicación](#application-menu-properties)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

El menú aplicación se compone de un control de botón desplegable que muestra un menú que contiene comandos que exponen la funcionalidad relacionada con un proyecto completo, como un documento, una imagen o una película completos. Entre los ejemplos se incluyen los comandos **nuevos**, **abrir**, **Guardar** y **salir** .

En la captura de pantalla siguiente se muestra el menú de la aplicación.

![captura de pantalla del menú aplicación y la lista elementos recientes de la cinta de opciones Paint for Windows 7.](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a>Componentes del menú aplicación

El menú aplicación es un elemento obligatorio en cualquier aplicación de la cinta de opciones. El punto de entrada en el menú de la aplicación es un botón distintivo que aparece como el primer elemento de la fila de [pestañas](windowsribbon-controls-tab.md) , como se muestra en la siguiente captura de pantalla.

> [!Note]  
> Windows 8 y versiones más recientes: imagen del botón de menú de la aplicación cambiada a etiqueta: **archivo**. Se recomienda no usar archivo como etiqueta para ninguna de sus propias pestañas.

 

![captura de pantalla del botón de menú aplicación de WordPad para Windows 7.](images/overviews/applicationmenu-button.png)

Al hacer clic en este botón, se muestra el menú enriquecido que se muestra en la siguiente captura de pantalla (menú aplicación de WordPad para Windows 7).

![captura de pantalla del menú de menú de la aplicación de WordPad para Windows 7.](images/overviews/applicationmenu-menu.png)

> [!Note]  
> No se produce ningún impacto en el conjunto de pestañas cuando se hace clic en el botón de menú de la aplicación. en su lugar, el foco entra en el menú.

 

El menú aplicación contiene dos paneles: una lista de comandos representados por uno o varios elementos [**MenuGroup**](windowsribbon-element-menugroup.md) y una lista de [elementos recientes](windowsribbon-controls-recentitems.md) representada por un elemento [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .

### <a name="application-menu-menugroup"></a>Menú de aplicación MenuGroup

El elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) debe contener al menos un elemento secundario [**MenuGroup**](windowsribbon-element-menugroup.md) que exponga una lista de comandos de nivel de aplicación. Si se declaran varios elementos **MenuGroup** , se dibuja una línea divisoria entre los grupos, tal y como se muestra en la siguiente captura de pantalla.

![captura de pantalla de un menú de aplicación menugroup.](images/overviews/applicationmenu-menugroup.png)

A continuación se muestra una lista de restricciones para un elemento [**MenuGroup**](windowsribbon-element-menugroup.md) de un menú de la aplicación:

-   Todos los elementos [**MenuGroup**](windowsribbon-element-menugroup.md) se deben declarar con un valor de atributo de *clase* de `MajorItems` .
-   Un menú de aplicación  [**MenuGroup**](windowsribbon-element-menugroup.md) solo admite el [botón](windowsribbon-controls-button.md), [botón](windowsribbon-controls-togglebutton.md)de alternancia [, botón](windowsribbon-controls-dropdownbutton.md)desplegable, [botón de expansión](windowsribbon-controls-splitbutton.md), [Galería desplegable](windowsribbon-controls-dropdowngallery.md)y controles de la [Galería de botones de expansión](windowsribbon-controls-splitbuttongallery.md) .
    > \[! Aún\]  
    > Las galerías de comandos son el único tipo de galería que se admiten en el menú de la aplicación. Vea [trabajar con galerías](./ribbon-controls-galleries.md)para obtener más información sobre los controles de la galería.

     

Cuando se usa un [botón o un](windowsribbon-controls-button.md) botón de [alternancia](windowsribbon-controls-togglebutton.md) en un [**MenuGroup**](windowsribbon-element-menugroup.md), el valor de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) se muestra en el menú y los valores de [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) y [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) se muestran como la información sobre herramientas, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de un control de botón en un menú de la aplicación.](images/overviews/applicationmenu-menubutton.png)

Cuando se usa un [botón](windowsribbon-controls-dropdownbutton.md)desplegable, un [botón de expansión](windowsribbon-controls-splitbutton.md), una [Galería](windowsribbon-controls-dropdowngallery.md)desplegable o una galería de [botones de expansión](windowsribbon-controls-splitbuttongallery.md) en el menú aplicación, la parte del menú se muestra como un control flotante que cubre y oculta el panel **elementos recientes** .

En el caso de los controles de botón de [expansión](windowsribbon-controls-splitbutton.md) y de [botón](windowsribbon-controls-dropdownbutton.md) desplegable, el valor de [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) se muestra en línea en el menú flotante para ayudar visualmente a los usuarios a detectar la funcionalidad del comando. El valor mostrado de **Command. LabelDescription** se divide mediante programación en un intervalo de dos líneas, y se realiza un intento de ajustar el valor exactamente encima del panel **elementos recientes** de. Si el valor de **Command. LabelDescription** no cabe, el control flotante se expandirá para alojar el valor del comando más largo [**. Comment**](windowsribbon-element-command-comment.md) en el [**MenuGroup**](windowsribbon-element-menugroup.md).

En la siguiente captura de pantalla se muestran estos comportamientos en un control flotante de [botón de expansión](windowsribbon-controls-splitbutton.md) .

![captura de pantalla de un control flotante de control de lista en un menú de la aplicación.](images/overviews/applicationmenu-menuflyout.png)

Con una [Galería desplegable](windowsribbon-controls-dropdowngallery.md) y una [Galería de botones de división](windowsribbon-controls-splitbuttongallery.md), solo se muestran una etiqueta y una imagen.

## <a name="sizing-the-application-menu"></a>Ajustar el tamaño del menú de la aplicación

El marco de la cinta de opciones controla el tamaño del menú de la aplicación. Si se proporcionan cadenas muy largas para el valor de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md), o si se usa una larga lista de comandos, el menú ajustará su tamaño para dar cabida al contenido. Algunas formas de ajuste incluyen expandir el tamaño de los controles flotantes o paneles de menús, y agregar visores de desplazamiento cuando es necesario desplazarse.

## <a name="application-menu-properties"></a>Propiedades del menú de la aplicación

El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de menú de la aplicación.

Normalmente, una propiedad de menú de la aplicación se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . El evento de invalidación se controla y las actualizaciones de las propiedades se definen mediante el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y no se consulta la aplicación para obtener un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad. Por ejemplo, el marco de trabajo requiere la propiedad cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones o cuando se muestra una información sobre herramientas.



| Clave de propiedad                                                                                     | Notas                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Solo se puede actualizar a través de la invalidación. |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Solo se puede actualizar a través de la invalidación. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Biblioteca de controles de Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado ApplicationMenu**](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 