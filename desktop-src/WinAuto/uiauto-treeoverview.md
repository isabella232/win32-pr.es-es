---
title: Información general sobre el árbol de la UI Automation
description: Los productos de tecnología de asistencia y scripts de prueba navegan por el árbol de automatización de la interfaz de usuario de Microsoft para recopilar información sobre la interfaz de usuario y sus elementos.
ms.assetid: f3afe258-baa7-41b5-a27e-cdc94b467d73
keywords:
- Automatización de la interfaz de usuario, información general del árbol
- Automatización de la interfaz de usuario, vista de árbol
- Automatización de la interfaz de usuario, vista sin formato del árbol
- Automatización de la interfaz de usuario, vista de control de árbol
- Automatización de la interfaz de usuario, vista de contenido de árbol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76bc9aa6568a3f4d63194d35ff0c7d8f59510c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903371"
---
# <a name="ui-automation-tree-overview"></a>Información general sobre el árbol de la UI Automation

Los productos de tecnología de asistencia y scripts de prueba navegan por el árbol de automatización de la interfaz de usuario de Microsoft para recopilar información sobre la interfaz de usuario y sus elementos.

En el árbol de automatización de la interfaz de usuario es un elemento raíz que representa la ventana del escritorio de Windows ("el escritorio") y cuyos elementos secundarios representan ventanas de la aplicación. Cada uno de estos elementos secundarios puede contener elementos que representan partes de la interfaz de usuario, como menús, botones, barras de herramientas y cuadros de lista. Estos elementos pueden contener elementos, como elementos de lista.

El árbol de automatización de la interfaz de usuario no es una estructura fija. Rara vez se percibe en su totalidad, ya que podría contener miles de elementos. Las partes del árbol de automatización de la interfaz de usuario se compilan como un cliente las necesita y la estructura del árbol cambia a medida que se agregan, se mueven o se quitan elementos.

Los proveedores de UI Automation admiten el árbol de automatización de la interfaz de usuario implementando la navegación entre los elementos de un fragmento. Un fragmento es un subárbol completo de elementos de un marco de trabajo determinado y tiene un elemento raíz (llamado *raíz de fragmento*) que normalmente se hospeda en una ventana.

Los proveedores no están preocupados por la navegación de un control a otro. Lo administra el núcleo de automatización de la interfaz de usuario, que utiliza información de los proveedores de ventanas predeterminados.

En este tema se incluyen las siguientes secciones.

-   [Vistas del árbol de automatización de la interfaz de usuario](#views-of-the-ui-automation-tree)
    -   [Vista sin formato](#raw-view)
    -   [Vista de control](#control-view)
    -   [Vista de contenido](#content-view)
-   [Temas relacionados](#related-topics)

## <a name="views-of-the-ui-automation-tree"></a>Vistas del árbol de automatización de la interfaz de usuario

El árbol de automatización de la interfaz de usuario se puede filtrar para crear vistas que contienen solo los elementos de automatización de la interfaz de usuario que son pertinentes para un cliente determinado. Este enfoque permite a los clientes personalizar la estructura que se presenta a través de la automatización de la interfaz de usuario para sus necesidades concretas.

El cliente puede personalizar la vista mediante el ámbito y el filtrado. El ámbito define el alcance de la vista, empezando por un elemento base. Por ejemplo, la aplicación podría querer encontrar solo elementos secundarios directos del escritorio o todos los descendientes de una ventana de la aplicación. El filtrado define los tipos de elementos que se incluyen en la vista.

Los proveedores de automatización de la interfaz de usuario admiten el filtrado mediante la definición de propiedades en los elementos, incluidas las propiedades [**IUIAutomationElement:: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) y [**IUIAutomationElement:: IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) .

La automatización de la interfaz de usuario proporciona tres vistas predeterminadas: vista sin formato, vista de control y vista de contenido. Estas vistas se definen mediante el tipo de filtrado realizado. La aplicación define el ámbito de cualquier vista. La aplicación puede aplicar otros filtros en las propiedades; por ejemplo, para incluir solo los controles habilitados en una vista de control.

### <a name="raw-view"></a>Vista sin formato

La vista sin formato del árbol de automatización de la interfaz de usuario es el árbol completo de elementos de automatización para los que el escritorio es la raíz. La vista sin formato sigue estrechamente la estructura de programación nativa de una aplicación y es la vista más detallada disponible. También es la base sobre la que se crean las otras vistas del árbol. Dado que esta vista depende del marco de interfaz de usuario subyacente, la vista sin formato de un botón Windows Presentation Foundation (WPF) tiene una vista sin formato diferente de la de un botón de Microsoft Win32.

La vista sin formato se obtiene buscando elementos sin especificar propiedades o usando [**IUIAutomation:: RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker) para obtener una interfaz [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) para navegar por el árbol.

### <a name="control-view"></a>Vista de control

La vista de control es un subconjunto de la vista sin formato. Incluye solo los elementos de la interfaz de usuario que tienen la propiedad [**IUIAutomationElement:: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) establecida en **true**.

La vista de control incluye los elementos de la interfaz de usuario que proporcionan información al usuario o permiten al usuario realizar una acción. Estos son los elementos de interfaz de usuario que son más interesantes para las aplicaciones de pruebas automatizadas.

La vista de control también incluye elementos de interfaz de usuario no interactivos que contribuyen a la estructura lógica de la interfaz de usuario. Estos incluyen contenedores de elementos, como encabezados de vista de lista, barras de herramientas, menús y la barra de estado. Otros elementos no interactivos que aparecen en la vista de control son gráficos con información y texto estático en un cuadro de diálogo.

Los elementos no interactivos que se usan solo con fines de diseño o decorativos, como los paneles que se usan para colocar controles en un cuadro de diálogo, no aparecen en la vista de control.

La vista de control del árbol de automatización de la interfaz de usuario se asigna estrechamente a la estructura de la interfaz de usuario que percibe un usuario final. Esto hace que el producto de tecnología de ayuda sea más fácil para describir la interfaz de usuario para el usuario final y ayudar a que el usuario final interactúe con la aplicación.

La vista de control se obtiene buscando elementos que tengan la propiedad [**IUIAutomationElement:: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) establecida en true o usando [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) para obtener una interfaz [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) para navegar por el árbol.

### <a name="content-view"></a>Vista de contenido

La vista de contenido del árbol de automatización de la interfaz de usuario es un subconjunto de la vista de control. Incluye solo los elementos de la interfaz de usuario que tienen la propiedad [**IUIAutomationElement:: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) y [**IUIAutomationElement:: IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) establecida en **true**.

La vista de contenido contiene elementos de interfaz de usuario que transmiten la información real en una interfaz de usuario, incluidos los elementos de la interfaz de usuario que pueden recibir el foco del teclado y algún texto que no es una etiqueta en un elemento de la interfaz de usuario. Estos son los elementos de interfaz de usuario que son más interesantes para una aplicación de lector de pantalla. Por ejemplo, los valores de un cuadro combinado desplegable aparecen en la vista de contenido porque los valores representan información utilizada por un usuario final.

En la vista de contenido, un cuadro combinado y un cuadro de lista se representan como una colección de elementos de la interfaz de usuario donde se puede seleccionar uno o varios elementos. El hecho de que un elemento esté siempre abierto y un elemento puede expandirse y contraerse es irrelevante en la vista de contenido porque está diseñado para mostrar los datos, o el contenido, que se presentan al usuario.

La vista de contenido se obtiene mediante la búsqueda de elementos que tienen la propiedad [**IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) y la propiedad [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) establecida en **true**, o bien mediante [**IUIAutomation:: ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) para obtener una interfaz [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) para navegar por el árbol.

En las siguientes imágenes se muestran las diferencias entre la vista de control y la vista de contenido. La primera imagen muestra un cuadro combinado simple con tres elementos en la lista desplegable. La segunda imagen muestra cómo aparecen los elementos de la interfaz de usuario del cuadro combinado en las vistas de control y contenido de la aplicación UISpy.exe.

![captura de pantalla de un cuadro combinado simple con tres elementos desplegables](images/combobox.png)

![captura de pantalla de la aplicación de UISpy con las vistas de control y contenido de los elementos del cuadro combinado](images/treeviews.jpg)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Crear el objeto CUIAutomation](uiauto-creatingcuiautomation.md)
</dt> <dt>

[Obtener elementos de UI Automation](uiauto-obtainingelements.md)
</dt> <dt>

[Fundamentos de UI Automation](entry-uiautocore-overview.md)
</dt> </dl>

 

 




