---
title: Obtener elementos de UI Automation
description: En este tema se describen varias maneras de obtener interfaces de IUIAutomationElement para los elementos de la interfaz de usuario.
ms.assetid: 8675851a-4a72-4cbe-ab71-ed6fc891be17
keywords:
- clientes, obtener elementos de UI Automation
- clientes, elementos de UI Automation
- clientes, elementos raíz
- clientes, ámbito de búsqueda
- Automatización de la interfaz de usuario, obtener elementos
- Automatización de la interfaz de usuario, elementos
- Automatización de la interfaz de usuario, elementos raíz
- Automatización de la interfaz de usuario, condiciones
- Automatización de la interfaz de usuario, ámbito de búsqueda
- obtener elementos de UI Automation
- elementos raíz
- ámbito de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: a1adbcea5cea81f97350ef15c491b289e07d3ee6
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105698466"
---
# <a name="obtaining-ui-automation-elements"></a>Obtener elementos de UI Automation

En este tema se describen varias maneras de obtener interfaces de [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para los elementos de la interfaz de usuario.

**IUIAutomationElement** se utiliza en la [aplicación de ejemplo cliente de contenido de documento de UI Automation](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient).

## <a name="root-element"></a>Elemento raíz

Aunque los elementos se pueden recuperar directamente mediante métodos, como [**IUIAutomation:: GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), algunas aplicaciones cliente requieren una vista de la estructura jerárquica de los elementos, lo que se conoce como el árbol de automatización de la interfaz de usuario. El elemento raíz de esta jerarquía es el escritorio. Puede obtener este elemento mediante el método [**IUIAutomation:: GetRootElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelement) o el método [**IUIAutomation:: GetRootElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelementbuildcache) . Ambos métodos recuperan un puntero de la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . Puede buscar elementos descendientes mediante métodos, como [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) y [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall).

> [!Note]  
> En general, debe intentar obtener solo elementos secundarios directos del elemento raíz. Una búsqueda de descendientes puede iterar a través de cientos o miles de elementos. Si intenta obtener un elemento concreto en un nivel inferior, debe iniciar la búsqueda desde la ventana de aplicación o desde un contenedor en un nivel inferior.

 

## <a name="conditions"></a>Condiciones

Para la mayoría de las técnicas que se usan para recuperar elementos de automatización de la interfaz de usuario, debe especificar una condición. Una condición es un conjunto de criterios que define los elementos que desea recuperar. Una condición se representa mediante la interfaz [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition) .

La condición más simple es la condición verdadera, que es un objeto predefinido que especifica que se devolverán todos los elementos del ámbito de búsqueda. La condición falsa es el inverso de la condición verdadera y es menos útil, ya que impediría que se encontrara cualquier elemento. Puede obtener una interfaz de la condición verdadera mediante [**IUIAutomation:: CreateTrueCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtruecondition).

Otras tres condiciones predefinidas, disponibles como propiedades en el objeto [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , se pueden usar solos o en combinación con otras condiciones: [**IUIAutomation:: ContentViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewcondition), [**ControlViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewcondition)y [**RawViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewcondition). **RawViewCondition**, que se usa por sí solo, es equivalente a la verdadera condición, porque no filtra los elementos por las propiedades [**IUIAutomationElement:: CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) o [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) .

Otras condiciones se crean a partir de objetos de condición, cada uno de los cuales especifica un valor de propiedad. Por ejemplo, una condición de propiedad podría especificar que el elemento está habilitado o que admite un patrón de control determinado.

Las condiciones que usan la lógica booleana se pueden combinar llamando a [**IUIAutomation:: CreateAndCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createandcondition), [**CreateOrCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createorcondition), [**CreateNotCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createnotcondition)y métodos relacionados.

## <a name="search-scope"></a>Ámbito de búsqueda

Las búsquedas realizadas mediante [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) o [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) deben tener un ámbito y un lugar de inicio.

> [!Note]  
> Los comentarios sobre estos dos métodos también se aplican a [**IUIAutomationElement:: FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache) y [**FindAllBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findallbuildcache).

 

El ámbito define el espacio alrededor del lugar de inicio en el que se va a buscar. Esto podría incluir el propio elemento, sus elementos relacionados, su elemento primario, sus elementos secundarios inmediatos y sus descendientes. Tenga en cuenta que los métodos de **búsqueda** no admiten la búsqueda en el árbol de automatización de la interfaz de usuario de Microsoft. es decir, no se admite la búsqueda de elementos antecesores.

El ámbito de una búsqueda se define mediante una combinación bit a bit de los valores del tipo enumerado [**TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) .

## <a name="finding-a-known-element"></a>Búsqueda de un elemento conocido

Para buscar un elemento conocido que se identifica mediante el nombre, el ID. de automatización o alguna otra propiedad o combinación de propiedades, es más fácil usar el método [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) . Si el elemento que se busca es una ventana de la aplicación, el punto inicial de la búsqueda puede ser el elemento raíz.

Esta forma de buscar elementos de automatización de la interfaz de usuario es muy útil en escenarios de pruebas automatizadas.

Para obtener un ejemplo de código que muestra cómo buscar un elemento conocido, vea [Buscar un elemento por su nombre](uiauto-howto-find-ui-elements.md).

## <a name="finding-elements-in-a-subtree"></a>Búsqueda de elementos en un subárbol

Para buscar todos los elementos que cumplen criterios específicos y que están relacionados con un elemento conocido, puede llamar a [**IUIAutomationElement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) en el elemento conocido. Por ejemplo, use este método para recuperar elementos de lista o elementos de menú de una lista o un menú, o para identificar todos los controles de un cuadro de diálogo.

Para obtener un ejemplo de código que muestra cómo buscar elementos en un subárbol, vea [Buscar elementos relacionados](uiauto-howto-find-ui-elements.md).

## <a name="walking-a-subtree"></a>Recorrer un subárbol

Si no tiene conocimiento previo de las aplicaciones con las que se puede usar el cliente, puede construir un subárbol de todos los elementos de interés mediante [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker). El cliente podría hacer esto, por ejemplo, en respuesta a un evento de cambio de foco. es decir, cuando una aplicación o un control recibe el foco de entrada, el cliente de automatización de la interfaz de usuario examina los elementos secundarios y quizás todos los descendientes del elemento que tiene el foco.

Tenga en cuenta que el recorrido del árbol de automatización de la interfaz de usuario consume muchos recursos. Recorra el árbol solo cuando no sea factible usar los métodos [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst), [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)o [**BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache) .

Puede definir su propio rastreador de árboles pasando una condición personalizada a [**IUIAutomation:: CreateTreeWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtreewalker)o puede usar uno de los siguientes objetos predefinidos que se definen como propiedades de la [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)base.



| Object                                                              | Propósito                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) | Busca solo los elementos cuya propiedad [**IUIAutomationElement:: CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) es **true**. |
| [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) | Busca solo los elementos cuya propiedad [**IUIAutomationElement:: CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) es **true**. |
| [**RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker)         | Busca todos los elementos.                                                                                                                                          |



 

Después de obtener un [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker), llame a los métodos **IUIAutomationTreeWalker:: GetXxx** para navegar por los elementos del subárbol, pasando el elemento desde el que se va a empezar a recorrer.

El método [**IUIAutomationTreeWalker:: Normalize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelement) se puede usar para desplazarse a un elemento del subárbol desde otro elemento que no forma parte de la vista. Por ejemplo, supongamos que crea una vista de un subárbol mediante [**IUIAutomation:: ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker). La aplicación recibe la notificación de que una barra de desplazamiento ha recibido el foco de entrada. Como una barra de desplazamiento no es un elemento de contenido, no está presente en la vista del subárbol. Sin embargo, puede pasar el [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) que representa la barra de desplazamiento a **IUIAutomationTreeWalker:: Normalize** y recuperar el antecesor más cercano que se encuentra en la vista de contenido.

Para ver ejemplos de código que muestran cómo usar la interfaz [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) , consulte [cómo recorrer el árbol de automatización de la interfaz de usuario](uiauto-howto-walk-uiautomation-tree.md).

## <a name="other-ways-to-retrieve-an-element"></a>Otras maneras de recuperar un elemento

Además de las búsquedas y la navegación, puede recuperar un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de las siguientes maneras.

### <a name="from-an-event"></a>Desde un evento

Cuando la aplicación recibe un evento de automatización de la interfaz de usuario, el objeto de origen que se pasa al controlador de eventos se representa mediante un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement). Por ejemplo, si se suscribe a eventos de cambio de foco, el origen que se pasa a [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) es el elemento que recibió el foco. Para obtener más información, vea [suscribirse a eventos de automatización de la interfaz de usuario](uiauto-eventsforclients.md).

### <a name="from-a-point"></a>Desde un punto

Para recuperar un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de las coordenadas de pantalla (por ejemplo, una posición del cursor), use el método [**IUIAutomation:: ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) .

### <a name="from-a-window-handle"></a>Desde un identificador de ventana

Para recuperar un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de un **hWnd**, use el método [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle) .

### <a name="from-the-focused-control"></a>Desde el control con el foco

Para recuperar un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) que representa el control con el foco, use el método [**IUIAutomation:: GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement) .

## <a name="related-topics"></a>Temas relacionados

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)

[Aplicación de ejemplo de cliente de contenido de documento de UI Automation](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)
