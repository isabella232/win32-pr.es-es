---
title: Información general sobre el árbol de la UI Automation
description: Los productos de tecnología de asistencia y los scripts de prueba navegan por el árbol Automatización de la interfaz de usuario Microsoft para recopilar información sobre la interfaz de usuario y sus elementos.
ms.assetid: f3afe258-baa7-41b5-a27e-cdc94b467d73
keywords:
- Automatización de la interfaz de usuario,información general sobre el árbol
- Automatización de la interfaz de usuario,vista del árbol
- Automatización de la interfaz de usuario vista sin formato del árbol
- Automatización de la interfaz de usuario,vista de control del árbol
- Automatización de la interfaz de usuario,vista de contenido del árbol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76bc9aa6568a3f4d63194d35ff0c7d8f59510c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465986"
---
# <a name="ui-automation-tree-overview"></a>Información general sobre el árbol de la UI Automation

Los productos de tecnología de asistencia y los scripts de prueba navegan por el árbol Automatización de la interfaz de usuario Microsoft para recopilar información sobre la interfaz de usuario y sus elementos.

En el Automatización de la interfaz de usuario principal hay un elemento raíz que representa la ventana Windows escritorio ("el escritorio") y cuyos elementos secundarios representan ventanas de aplicación. Cada uno de estos elementos secundarios puede contener elementos que representan partes de la interfaz de usuario, como menús, botones, barras de herramientas y cuadros de lista. Estos elementos pueden contener elementos, como elementos de lista.

El Automatización de la interfaz de usuario no es una estructura fija. Rara vez se ve en su total porque podría contener miles de elementos. Las partes del Automatización de la interfaz de usuario se construyen a medida que un cliente las necesita y la estructura del árbol cambia a medida que se agregan, se mueven o se quitan elementos.

Automatización de la interfaz de usuario proveedores admiten el Automatización de la interfaz de usuario de datos mediante la implementación de la navegación entre los elementos de un fragmento. Un fragmento es un subárbol completo de elementos de un marco determinado y tiene un elemento raíz (denominado raíz del *fragmento)* que normalmente se hospeda en una ventana.

Los proveedores no se refieren a la navegación de un control a otro. Esto se administra mediante el Automatización de la interfaz de usuario principal, que usa información de los proveedores de ventana predeterminados.

En este tema se incluyen las siguientes secciones.

-   [Vistas del árbol de Automatización de la interfaz de usuario datos](#views-of-the-ui-automation-tree)
    -   [Vista sin formato](#raw-view)
    -   [Vista de control](#control-view)
    -   [Vista de contenido](#content-view)
-   [Temas relacionados](#related-topics)

## <a name="views-of-the-ui-automation-tree"></a>Vistas del árbol de Automatización de la interfaz de usuario datos

El Automatización de la interfaz de usuario se puede filtrar para crear vistas que contengan solo los Automatización de la interfaz de usuario que son relevantes para un cliente determinado. Este enfoque permite a los clientes personalizar la estructura que se presenta a través Automatización de la interfaz de usuario a sus necesidades concretas.

El cliente puede personalizar la vista mediante el ámbito y el filtrado. El ámbito define la extensión de la vista, empezando por un elemento base. Por ejemplo, es posible que la aplicación quiera buscar solo elementos secundarios directos del escritorio o todos los descendientes de una ventana de aplicación. El filtrado define los tipos de elementos que se incluyen en la vista.

Automatización de la interfaz de usuario proveedores admiten el filtrado mediante la definición de propiedades en elementos, incluidas las propiedades [**IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) e [**IUIAutomationElement::IsContentElement.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement)

Automatización de la interfaz de usuario proporciona tres vistas predeterminadas: vista sin formato, vista de control y vista de contenido. Estas vistas se definen mediante el tipo de filtrado realizado. La aplicación define el ámbito de cualquier vista. La aplicación puede aplicar otros filtros en las propiedades; por ejemplo, para incluir solo controles habilitados en una vista de control.

### <a name="raw-view"></a>Vista sin formato

La vista sin formato del Automatización de la interfaz de usuario es el árbol completo de elementos de automatización para los que el escritorio es la raíz. La vista sin formato sigue estrechamente la estructura de programación nativa de una aplicación y es la vista más detallada disponible. También es la base sobre la que se crean las otras vistas del árbol. Dado que esta vista depende del marco de interfaz de usuario subyacente, la vista sin formato de un botón Windows Presentation Foundation (WPF) tiene una vista sin formato diferente que un botón de Microsoft Win32.

La vista sin formato se obtiene buscando elementos sin especificar propiedades o usando [**IUIAutomation::RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker) para obtener una interfaz [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) para navegar por el árbol.

### <a name="control-view"></a>Vista de control

La vista de control es un subconjunto de la vista sin formato. Incluye solo los elementos de interfaz de usuario que tienen la propiedad [**IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) establecida en **TRUE.**

La vista de control incluye los elementos de la interfaz de usuario que proporcionan información al usuario o permiten al usuario realizar una acción. Estos son los elementos de la interfaz de usuario que son más interesantes para las aplicaciones de prueba automatizada.

La vista de control también incluye elementos de interfaz de usuario no inactivos que contribuyen a la estructura lógica de la interfaz de usuario. Estos incluyen contenedores de elementos, como encabezados de vista de lista, barras de herramientas, menús y la barra de estado. Otros elementos no inactivos que aparecen en la vista de control son gráficos con información y texto estático en un cuadro de diálogo.

Los elementos no inactivos que solo se usan con fines de diseño o de decoración, como los paneles usados para configurar controles en un cuadro de diálogo, no aparecen en la vista de control.

La vista de control del Automatización de la interfaz de usuario se asigna estrechamente a la estructura de interfaz de usuario que percibe un usuario final. Esto facilita que el producto de tecnología de asistencia describa la interfaz de usuario al usuario final y ayude a ese usuario final a interactuar con la aplicación.

La vista de control se obtiene mediante la búsqueda de elementos que tienen la propiedad [**IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) establecida en true o mediante [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) para obtener una interfaz [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) para navegar por el árbol.

### <a name="content-view"></a>Vista de contenido

La vista de contenido del Automatización de la interfaz de usuario es un subconjunto de la vista de control. Solo incluye los elementos de interfaz de usuario que tienen [**IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) y la propiedad [**IUIAutomationElement::IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) establecida en **TRUE.**

La vista de contenido contiene elementos de interfaz de usuario que transmiten la información real en una interfaz de usuario, incluidos los elementos de la interfaz de usuario que pueden recibir el foco del teclado y algún texto que no sea una etiqueta en un elemento de interfaz de usuario. Estos son los elementos de interfaz de usuario que son más interesantes para una aplicación de lector de pantalla. Por ejemplo, los valores de un cuadro combinado desplegable aparecen en la vista de contenido porque los valores representan la información que usa un usuario final.

En la vista de contenido, un cuadro combinado y un cuadro de lista se representan como una colección de elementos de interfaz de usuario donde se puede seleccionar uno o varios elementos. El hecho de que un elemento siempre esté abierto y un elemento pueda expandirse y contraerse es irrelevante en la vista de contenido porque está diseñado para mostrar los datos o el contenido que se presenta al usuario.

La vista de contenido se obtiene buscando elementos que tienen las propiedades [**IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) y [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) establecidas en **TRUE** o mediante [**IUIAutomation::ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) para obtener una interfaz [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) para navegar por el árbol.

Las imágenes siguientes muestran las diferencias entre la vista de control y la vista de contenido. La primera imagen muestra un cuadro combinado simple con tres elementos en la lista desplegable. La segunda imagen muestra cómo aparecen los elementos de interfaz de usuario del cuadro combinado en las vistas de control y contenido de UISpy.exe aplicación.

![captura de pantalla de un cuadro combinado simple con tres elementos desplegables](images/combobox.png)

![captura de pantalla de la aplicación uispy con vistas de control y contenido de elementos de cuadro combinado](images/treeviews.jpg)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Creación del objeto CUIAutomation](uiauto-creatingcuiautomation.md)
</dt> <dt>

[Obtener elementos de UI Automation](uiauto-obtainingelements.md)
</dt> <dt>

[Fundamentos de UI Automation](entry-uiautocore-overview.md)
</dt> </dl>

 

 




