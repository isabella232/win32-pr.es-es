---
title: información general Automatización de la interfaz de usuario clientes de Automatización de la interfaz de usuario
description: En este tema se describen las tareas principales implicadas en la implementación de una aplicación cliente Automatización de la interfaz de usuario Microsoft.
ms.assetid: 536ccf03-2f52-49e5-a95f-ea56cf821779
keywords:
- Automatización de la interfaz de usuario,introducción a los clientes
- clients,about
- clients,elements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37ff185e72c25f5c3b8eeba8cdd4ae9250391a867538ad3e4b6de4f8d1dce25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117928687"
---
# <a name="ui-automation-clients-overview"></a>información general Automatización de la interfaz de usuario clientes de Automatización de la interfaz de usuario

En este tema se describen las tareas principales implicadas en la implementación de una aplicación cliente Automatización de la interfaz de usuario Microsoft.

Un Automatización de la interfaz de usuario cliente es cualquier aplicación que use la API de Automatización de la interfaz de usuario para acceder a información sobre los elementos de la interfaz de usuario o para controlar las aplicaciones mediante la manipulación mediante programación de sus elementos de interfaz de usuario. Automatización de la interfaz de usuario clientes incluyen aplicaciones de tecnología de asistencia, como lectores de pantalla, que recuperan información sobre los elementos de la interfaz de usuario y presentan la información de una manera que se puede usar para las personas con discapacidades. También incluyen aplicaciones como programas de reconocimiento de voz y herramientas de pruebas de software, que usan Automatización de la interfaz de usuario en lugar del mouse y el teclado para "impulsar" otras aplicaciones.

Desde una Automatización de la interfaz de usuario, las tareas principales que una Automatización de la interfaz de usuario cliente debe realizar incluyen las siguientes:

1.  **Obtenga una instancia del objeto CUIAutomation.**

    La información sobre los elementos de la interfaz de usuario y el acceso a la funcionalidad de elementos de la interfaz de usuario se expone a los clientes Automatización de la interfaz de usuario de interfaz de usuario. Sin embargo, las aplicaciones cliente no funcionan directamente con los proveedores. En su lugar, un servicio principal se encuentra entre el cliente y el proveedor. Cuando un cliente llama Automatización de la interfaz de usuario API, realmente llama al servicio principal de Automatización de la interfaz de usuario que, a su vez, realiza llamadas a las interfaces implementadas por el proveedor.

    Para obtener acceso al servicio Automatización de la interfaz de usuario principal, un cliente debe crear una instancia del objeto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) y recuperar un puntero de interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) en el objeto . El **puntero IUIAutomation es** la clave del cliente para acceder a toda la funcionalidad de Automatización de la interfaz de usuario que está disponible para el cliente. Para obtener más información, [vea Creating the CUIAutomation Object](uiauto-creatingcuiautomation.md).

2.  **Recupere las interfaces IUIAutomationElement para los elementos de la interfaz de usuario del Automatización de la interfaz de usuario árbol.**

    Automatización de la interfaz de usuario expone elementos individuales de la interfaz de usuario como objetos que implementan la [**interfaz IUIAutomationElement.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) La información sobre un elemento está disponible para los clientes a través de las propiedades expuestas por la interfaz **IUIAutomationElement** del elemento, junto con el acceso a los patrones de control del elemento. Las propiedades y los métodos expuestos por las interfaces de patrón de control proporcionan acceso a la información y funcionalidad específicas del control.

    Los Automatización de la interfaz de usuario de elemento se proporcionan a los clientes en una estructura jerárquica de árbol denominada Automatización de la interfaz de usuario árbol. Los clientes usan métodos expuestos por la interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) para recuperar interfaces [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para elementos de la interfaz de usuario en el árbol y para recuperar otras interfaces usadas para buscar en el árbol elementos que coincidan con un conjunto determinado de criterios. Para obtener más información, [vea Obtener Automatización de la interfaz de usuario elementos](uiauto-obtainingelements.md).

    Al recuperar elementos de la interfaz de usuario, los clientes pueden mejorar el rendimiento del sistema mediante las funcionalidades de almacenamiento en caché de Automatización de la interfaz de usuario. El almacenamiento en caché permite a un cliente especificar un conjunto de propiedades y patrones de control para recuperar junto con el elemento . En una sola llamada entre procesos, Automatización de la interfaz de usuario recupera el elemento y las propiedades y los patrones de control especificados y, a continuación, los almacena en la memoria caché. Sin almacenamiento en caché, se requiere una llamada entre procesos independiente para recuperar cada propiedad o patrón de control. Para obtener más información, vea [Caching Automatización de la interfaz de usuario Properties and Control Patterns](uiauto-cachingforclients.md).

3.  **Recupere las propiedades del elemento de la interfaz de usuario e invoque la funcionalidad del elemento de interfaz de usuario.**

    Los clientes usan [**la interfaz IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para recuperar las propiedades y los patrones de control de un elemento. La interfaz incluye dos versiones de cada método de recuperación de propiedades: una versión recupera la propiedad de la memoria caché y la otra recupera la propiedad del proveedor. Para obtener más información, [vea Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).

4.  **Responder a Automatización de la interfaz de usuario eventos.**

    Automatización de la interfaz de usuario proveedores notifican a los clientes de cambios o apariciones importantes en la interfaz de usuario mediante la generación de eventos. Los clientes deben determinar qué eventos necesitan y, a continuación, implementar y registrar interfaces de control de eventos para recibir y procesar esos eventos. Para obtener más información, [vea Suscribirse a Automatización de la interfaz de usuario eventos](uiauto-eventsforclients.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> </dl>

 

 