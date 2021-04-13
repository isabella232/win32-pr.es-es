---
title: Introducción a los clientes de UI Automation
description: En este tema se describen las tareas principales relacionadas con la implementación de una aplicación cliente de automatización de la interfaz de usuario de Microsoft.
ms.assetid: 536ccf03-2f52-49e5-a95f-ea56cf821779
keywords:
- Automatización de la interfaz de usuario, introducción a los clientes
- clientes, acerca de
- clientes, elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d4705d75a0a80c114e2b83f9625f827c75503b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420801"
---
# <a name="ui-automation-clients-overview"></a>Introducción a los clientes de UI Automation

En este tema se describen las tareas principales relacionadas con la implementación de una aplicación cliente de automatización de la interfaz de usuario de Microsoft.

Un cliente de UI Automation es cualquier aplicación que use la API de automatización de la interfaz de usuario para tener acceso a información sobre los elementos de la interfaz de usuario o para controlar las aplicaciones mediante la manipulación mediante programación de sus elementos de interfaz de usuario Los clientes de automatización de la interfaz de usuario incluyen aplicaciones de tecnología de asistencia, como lectores de pantalla, que recuperan información sobre los elementos de la interfaz de usuario y presentan la información de una manera que se puede usar para personas con discapacidades. También incluyen aplicaciones como programas de reconocimiento de voz y herramientas de prueba de software, que usan la automatización de la interfaz de usuario en lugar del mouse y el teclado para "impulsar" otras aplicaciones.

Desde la perspectiva de la automatización de la interfaz de usuario, las tareas principales que debe realizar una aplicación cliente de automatización de la interfaz de usuario son las siguientes:

1.  **Obtener una instancia del objeto CUIAutomation.**

    Los proveedores de automatización de la interfaz de usuario exponen información sobre los elementos de interfaz de usuario y el acceso a la funcionalidad de elementos de la interfaz de usuario. Sin embargo, las aplicaciones cliente no funcionan directamente con proveedores. En su lugar, un servicio principal se encuentra entre el cliente y el proveedor. Cuando un cliente llama a la API de automatización de la interfaz de usuario, realmente llama al servicio principal de automatización de la interfaz de usuario que, a su vez, realiza llamadas a las interfaces implementadas por el proveedor.

    Para obtener acceso al servicio principal de automatización de la interfaz de usuario, un cliente debe crear una instancia del objeto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) y recuperar un puntero de interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) en el objeto. El puntero **IUIAutomation** es la clave del cliente para tener acceso a toda la funcionalidad de automatización de la interfaz de usuario que está disponible para el cliente. Para obtener más información, vea [crear el objeto CUIAutomation](uiauto-creatingcuiautomation.md).

2.  **Recupera interfaces de IUIAutomationElement para los elementos de la interfaz de usuario del árbol de automatización de la interfaz de usuario.**

    La automatización de la interfaz de usuario expone elementos de interfaz de usuario individuales como objetos que implementan la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . La información sobre un elemento está disponible para los clientes a través de las propiedades expuestas por la interfaz **IUIAutomationElement** del elemento, junto con el acceso a los patrones de control del elemento. Las propiedades y los métodos expuestos por las interfaces de patrón de control proporcionan acceso a la funcionalidad y la información específica del control.

    Los objetos de elemento de automatización de la interfaz de usuario se proporcionan a los clientes en una estructura de árbol jerárquica denominada árbol de automatización de la interfaz de usuario. Los clientes usan métodos expuestos por la interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) para recuperar interfaces [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para los elementos de la interfaz de usuario en el árbol y para recuperar otras interfaces utilizadas para buscar en el árbol los elementos que coinciden con un determinado conjunto de criterios. Para obtener más información, vea [obtener elementos de UI Automation](uiauto-obtainingelements.md).

    Al recuperar elementos de la interfaz de usuario, los clientes pueden mejorar el rendimiento del sistema mediante las capacidades de almacenamiento en caché de la automatización de la interfaz de usuario. Caching permite a un cliente especificar un conjunto de propiedades y patrones de control que se van a recuperar junto con el elemento. En una única llamada entre procesos, la automatización de la interfaz de usuario recupera el elemento, las propiedades y los patrones de control especificados y, a continuación, los almacena en la memoria caché. Sin almacenamiento en caché, se requiere una llamada de interproceso independiente para recuperar cada patrón de propiedad o de control. Para obtener más información, vea [caching UI Automation Properties and Control Patterns](uiauto-cachingforclients.md).

3.  **Recuperar las propiedades de los elementos de la interfaz de usuario e invocar la funcionalidad del elemento**

    Los clientes usan la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para recuperar las propiedades y los patrones de control de un elemento. La interfaz incluye dos versiones de cada método de recuperación de propiedades: una versión recupera la propiedad de la memoria caché, la otra recupera la propiedad del proveedor. Para obtener más información, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).

4.  **Responder a eventos de UI Automation.**

    Los proveedores de automatización de la interfaz de usuario notifican a los clientes los cambios o repeticiones importantes en la interfaz de usuario mediante la generación de eventos. Los clientes deben determinar qué eventos necesitan y, a continuación, implementar y registrar interfaces de control de eventos para recibir y procesar esos eventos. Para obtener más información, vea [suscribirse a eventos de automatización de la interfaz de usuario](uiauto-eventsforclients.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> </dl>

 

 