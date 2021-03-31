---
title: Descripción de los problemas de subprocesos
description: En este tema se describen escenarios comunes de subprocesos para implementaciones de cliente de automatización de la interfaz de usuario de Microsoft y se explica cómo evitar problemas que pueden producirse si un cliente usa el subproceso de forma incorrecta.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- clientes, problemas de subprocesos de automatización de la interfaz de usuario
- clientes, problemas de subprocesos
- clientes, modelo de subprocesos del controlador de eventos
- clientes, modelo de subprocesos del controlador de eventos de UI Automation
- clientes, afinidad de UI Automation
- clientes, afinidad
- Automatización de la interfaz de usuario, problemas de subprocesos
- Automatización de la interfaz de usuario, modelo de subprocesos del controlador de eventos
- Automatización de la interfaz de usuario, afinidad
- problemas con el subprocesamiento
- modelo de subprocesos del controlador de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077805"
---
# <a name="understanding-threading-issues"></a>Descripción de los problemas de subprocesos

En este tema se describen escenarios comunes de subprocesos para implementaciones de cliente de automatización de la interfaz de usuario de Microsoft y se explica cómo evitar problemas que pueden producirse si un cliente usa el subproceso de forma incorrecta.

Este tema contiene las siguientes secciones:

-   [Automatización de la interfaz de usuario y subproceso de interfaz de usuario](#ui-automation-and-the-ui-thread)
-   [Modelo de subprocesos para controladores de eventos](#threading-model-for-event-handlers)
-   [Afinidad de Apartamento COM en Windows de 64 bits](#com-apartment-affinity-on-64-bit-windows)
-   [Temas relacionados](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a>Automatización de la interfaz de usuario y subproceso de interfaz de usuario

Debido al modo en que la automatización de la interfaz de usuario utiliza mensajes de Windows, pueden producirse conflictos cuando una aplicación cliente intenta interactuar con su propia interfaz de usuario en el subproceso de la interfaz de usuario. Estos conflictos pueden dar lugar a un rendimiento muy lento o incluso provocar que la aplicación deje de responder.

Si la aplicación cliente está diseñada para interactuar con todos los elementos del escritorio, incluida su propia interfaz de usuario, debe realizar todas las llamadas de automatización de la interfaz de usuario desde un subproceso independiente. Esto incluye la ubicación de elementos, por ejemplo, mediante [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) o el método [**IUIAutomationElement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) y el uso de patrones de control. Este subproceso no debe poseer ninguna ventana de y debe ser un subproceso del modelo de Apartamento multiproceso (MTA) de modelo de objetos componentes (COM) (uno que inicializa COM mediante una llamada a [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) con la marca de **coinit \_ multiproceso** ).

Es seguro realizar llamadas de automatización de la interfaz de usuario en un controlador de eventos de automatización de la interfaz de usuario, porque siempre se llama al controlador de eventos en un subproceso que no es de interfaz de usuario. Sin embargo, al suscribirse a eventos que pueden originarse en la interfaz de usuario de la aplicación cliente, debe realizar la llamada a [**IUIAutomation:: AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler), o un método relacionado, en un subproceso que no sea de interfaz de usuario (que también debe ser un subproceso MTA). Quite los controladores de eventos que estén en el mismo subproceso.

Un cliente de UI Automation no debe utilizar varios subprocesos para agregar o quitar controladores de eventos. Un comportamiento inesperado puede producirse si se agrega o se quita un controlador de eventos mientras se agrega o quita otro en el mismo proceso de cliente.

## <a name="threading-model-for-event-handlers"></a>Modelo de subprocesos para controladores de eventos

Un cliente de automatización de la interfaz de usuario debe utilizar el modelo de subprocesos del MTA de COM para los subprocesos que implementan controladores de eventos. El uso del modelo de contenedor uniproceso (STA) puede causar problemas, como evitar que los clientes quiten controladores de eventos del subproceso.

## <a name="com-apartment-affinity-on-64-bit-windows"></a>Afinidad de Apartamento COM en Windows de 64 bits

Según la especificación COM, la duración de un objeto remoto se rige por la duración del apartamento donde se llama a la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el objeto. Cuando se cierra el apartamento original, el objeto remoto también se libera.

En el caso de los clientes de automatización de la interfaz de usuario, este comportamiento COM puede significar que la duración de la aplicación auxiliar Remote 32/64 (creada por UIAutomationCore.dll) utilizada por un elemento de 32 bits se rige por la duración del apartamento del subproceso que creó el elemento. Si el cliente de automatización de la interfaz de usuario calcula las referencias del elemento en otro subproceso, el elemento se puede invalidar Cuando el apartamento de origen se apaga. El cliente de automatización de la interfaz de usuario debe controlar estos problemas correctamente mediante la detección de errores al usar elementos de automatización de serialización.

El mismo problema puede producirse con un cliente de automatización de la interfaz de usuario de 32 bits que tiene elementos de 64 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Obtener elementos de UI Automation](uiauto-obtainingelements.md)
</dt> <dt>

[Suscribirse a eventos de UI Automation](uiauto-eventsforclients.md)
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[INFORMACIÓN: descripciones y funcionamiento de modelos de subprocesos OLE](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 