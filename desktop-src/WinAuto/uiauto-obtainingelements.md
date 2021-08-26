---
title: Obtener elementos de UI Automation
description: En este tema se describen varias maneras de obtener interfaces IUIAutomationElement para elementos de interfaz de usuario.
ms.assetid: 8675851a-4a72-4cbe-ab71-ed6fc891be17
keywords:
- clientes, obtener Automatización de la interfaz de usuario elementos
- clients,Automatización de la interfaz de usuario elementos
- clients,root elements
- clients,ámbito de búsqueda
- Automatización de la interfaz de usuario, obtener elementos
- Automatización de la interfaz de usuario,elements
- Automatización de la interfaz de usuario,root elements
- Automatización de la interfaz de usuario,conditions
- Automatización de la interfaz de usuario,ámbito de búsqueda
- obtener Automatización de la interfaz de usuario elementos
- elementos raíz
- ámbito de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: f2ecf8a30f468e7a7ca4df60465993fa7acdc1e8eef1c8537d8c3d796132cb82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997745"
---
# <a name="obtaining-ui-automation-elements"></a>Obtener elementos de UI Automation

En este tema se describen varias maneras de obtener interfaces [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para elementos de interfaz de usuario.

**IUIAutomationElement** se usa en la aplicación de ejemplo Automatización de la interfaz de usuario de cliente de [contenido del documento.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)

## <a name="root-element"></a>Elemento raíz

Aunque los elementos se pueden recuperar directamente mediante métodos, como [**IUIAutomation::GetFocusedElement,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)algunas aplicaciones cliente requieren una vista de la estructura jerárquica de los elementos, conocida como el árbol Automatización de la interfaz de usuario. El elemento raíz de esta jerarquía es el escritorio. Puede obtener este elemento mediante el método [**IUIAutomation::GetRootElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelement) o el método [**IUIAutomation::GetRootElementBuildCache.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelementbuildcache) Ambos métodos recuperan un [**puntero de interfaz IUIAutomationElement.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) Puede buscar elementos descendientes mediante métodos, como [**IUIAutomationElement::FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) y [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall).

> [!Note]  
> En general, debe intentar obtener solo elementos secundarios directos del elemento raíz. Una búsqueda de descendientes puede recorrer en iteración cientos o miles de elementos. Si intenta obtener un elemento concreto en un nivel inferior, debe iniciar la búsqueda desde la ventana de aplicación o desde un contenedor en un nivel inferior.

 

## <a name="conditions"></a>Condiciones

Para la mayoría de las técnicas que se usan para recuperar Automatización de la interfaz de usuario elementos, debe especificar una condición. Una condición es un conjunto de criterios que define los elementos que desea recuperar. Una condición se representa mediante la [**interfaz IUIAutomationCondition.**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)

La condición más sencilla es la condición verdadera, que es un objeto predefinido que especifica que se van a devolver todos los elementos del ámbito de búsqueda. La condición false es la inversa de la condición verdadera y es menos útil, ya que impediría que se encontrara ningún elemento. Puede obtener una interfaz a la condición true mediante [**IUIAutomation::CreateTrueCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtruecondition).

Otras tres condiciones predefinidas, disponibles como propiedades en el objeto [**IUIAutomation,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) se pueden usar solas o en combinación con otras condiciones: [**IUIAutomation::ContentViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewcondition), [**ControlViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewcondition)y [**RawViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewcondition). **RawViewCondition**, usado por sí mismo, es equivalente a la condición true, porque no filtra elementos por las propiedades [**IUIAutomationElement::CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) o [**CurrentIsContentElement.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement)

Otras condiciones se construyen a partir de objetos de condición, cada una de las cuales especifica un valor de propiedad. Por ejemplo, una condición de propiedad podría especificar que el elemento está habilitado o que admite un determinado patrón de control.

Las condiciones que usan lógica booleana se pueden combinar llamando a [**IUIAutomation::CreateAndCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createandcondition), [**CreateOrCondition,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createorcondition) [**CreateNotCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createnotcondition)y métodos relacionados.

## <a name="search-scope"></a>Ámbito de búsqueda

Las búsquedas que se realizan mediante [**IUIAutomationElement::FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) o [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) deben tener un ámbito y un punto de partida.

> [!Note]  
> Cualquier comentario sobre estos dos métodos también se aplica a [**IUIAutomationElement::FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache) y [**FindAllBuildCache.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findallbuildcache)

 

El ámbito define el espacio alrededor del lugar inicial en el que se va a buscar. Esto puede incluir el propio elemento, sus elementos del mismo nivel, su elemento primario, sus elementos secundarios inmediatos y sus descendientes. Tenga en cuenta que **los métodos Find** no admiten la búsqueda en el árbol de Automatización de la interfaz de usuario Microsoft; Es decir, no se admite la búsqueda de elementos antecesores.

El ámbito de una búsqueda se define mediante una combinación bit a bit de valores del tipo enumerado [**TreeScope.**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)

## <a name="finding-a-known-element"></a>Búsqueda de un elemento conocido

Para buscar un elemento conocido identificado por nombre, identificador de automatización o alguna otra propiedad o combinación de propiedades, es más fácil usar el método [**IUIAutomationElement::FindFirst.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) Si el elemento buscado es una ventana de aplicación, el punto inicial de la búsqueda puede ser el elemento raíz.

Esta forma de buscar Automatización de la interfaz de usuario elementos es más útil en escenarios de prueba automatizados.

Para obtener un ejemplo de código que muestra cómo buscar un elemento know, vea [Buscar un elemento por nombre.](uiauto-howto-find-ui-elements.md)

## <a name="finding-elements-in-a-subtree"></a>Búsqueda de elementos en un subárbol

Para buscar todos los elementos que cumplen criterios específicos y están relacionados con un elemento conocido, puede llamar a [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) en el elemento conocido. Por ejemplo, use este método para recuperar elementos de lista o elementos de menú de una lista o menú, o para identificar todos los controles de un cuadro de diálogo.

Para obtener un ejemplo de código que muestra cómo buscar elementos en un subárbol, vea [Buscar elementos relacionados.](uiauto-howto-find-ui-elements.md)

## <a name="walking-a-subtree"></a>Recorrer un subárbol

Si no tiene conocimientos previos de las aplicaciones con las que se puede usar el cliente, puede construir un subárbol de todos los elementos de interés mediante [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker). El cliente podría hacer esto, por ejemplo, en respuesta a un evento de cambio de foco. es decir, cuando una aplicación o un control recibe el foco de entrada, el cliente de Automatización de la interfaz de usuario examina los elementos secundarios y quizás todos los descendientes del elemento centrado.

Tenga en cuenta que recorrer el Automatización de la interfaz de usuario de trabajo consume muchos recursos. Recorrer el árbol solo cuando no sea factible usar los métodos [**IUIAutomationElement::FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst), [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)o [**BuildUpdatedCache.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache)

Para definir su propio árbol, pase una condición personalizada a [**IUIAutomation::CreateTreeWalker,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtreewalker)o bien puede usar uno de los siguientes objetos predefinidos que se definen como propiedades de la [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)base.



| Object                                                              | Propósito                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) | Busca solo los elementos cuya [**propiedad IUIAutomationElement::CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) sea **TRUE.** |
| [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) | Busca solo los elementos cuya [**propiedad IUIAutomationElement::CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) sea **TRUE.** |
| [**RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker)         | Busca todos los elementos.                                                                                                                                          |



 

Después de obtener un [**elemento IUIAutomationTreeWalker,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)llame a los métodos **IUIAutomationTreeWalker::GetXxx** para navegar por los elementos del subárbol y pasar el elemento desde el que empezar a recorrer.

El [**método IUIAutomationTreeWalker::Normalize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelement) se puede usar para navegar a un elemento del subárbol desde otro elemento que no forma parte de la vista. Por ejemplo, supongamos que crea una vista de un subárbol mediante [**IUIAutomation::ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker). La aplicación recibe la notificación de que una barra de desplazamiento ha recibido el foco de entrada. Como una barra de desplazamiento no es un elemento de contenido, no está presente en la vista del subárbol. Sin embargo, puede pasar el [**elemento IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) que representa la barra de desplazamiento a **IUIAutomationTreeWalker::Normalize** y recuperar el antecesor más cercano que se encuentra en la vista de contenido.

Para obtener ejemplos de código que muestran cómo usar la interfaz [**IUIAutomationTreeWalker,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) vea [How to Walk the Automatización de la interfaz de usuario Tree](uiauto-howto-walk-uiautomation-tree.md).

## <a name="other-ways-to-retrieve-an-element"></a>Otras maneras de recuperar un elemento

Además de las búsquedas y la navegación, puede recuperar [**un elemento IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de las maneras siguientes.

### <a name="from-an-event"></a>Desde un evento

Cuando la aplicación recibe un evento Automatización de la interfaz de usuario, el objeto de origen pasado al controlador de eventos se representa mediante [**un elemento IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement). Por ejemplo, si se suscribe a eventos con cambio de foco, el origen pasado a [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) es el elemento que recibió el foco. Para obtener más información, [vea Suscribirse a Automatización de la interfaz de usuario eventos](uiauto-eventsforclients.md).

### <a name="from-a-point"></a>Desde un punto

Para recuperar un [**elemento IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) a partir de coordenadas de pantalla, por ejemplo, una posición de cursor, use el [**método IUIAutomation::ElementFromPoint.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)

### <a name="from-a-window-handle"></a>Desde un identificador de ventana

Para recuperar un [**elemento IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de **un HWND,** use el [**método IUIAutomation::ElementFromHandle.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle)

### <a name="from-the-focused-control"></a>Desde el control con el foco

Para recuperar un [**elemento IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) que representa el control centrado, use el método [**IUIAutomation::GetFocusedElement.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)

## <a name="related-topics"></a>Temas relacionados

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)

[Automatización de la interfaz de usuario aplicación de ejemplo de cliente de contenido de documento](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)
