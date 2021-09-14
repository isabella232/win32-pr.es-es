---
title: Descripción de los problemas de subprocesamiento
description: En este tema se describen los escenarios comunes de subprocesos para las implementaciones de cliente de Microsoft Automatización de la interfaz de usuario y se explica cómo evitar problemas que pueden producirse si un cliente usa subprocesos incorrectamente.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- clients,Automatización de la interfaz de usuario problemas de subprocesos
- clients,threading issues
- clients,event handler threading model
- clients,Automatización de la interfaz de usuario de subprocesos del controlador de eventos
- clients,Automatización de la interfaz de usuario affinity
- clients,affinity
- Automatización de la interfaz de usuario, problemas de subprocesos
- Automatización de la interfaz de usuario, modelo de subprocesos del controlador de eventos
- Automatización de la interfaz de usuario,affinity
- problemas con el subprocesamiento
- modelo de subprocesos del controlador de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172594"
---
# <a name="understanding-threading-issues"></a>Descripción de los problemas de subprocesamiento

En este tema se describen los escenarios comunes de subprocesos para las implementaciones de cliente de Microsoft Automatización de la interfaz de usuario y se explica cómo evitar problemas que pueden producirse si un cliente usa subprocesos incorrectamente.

Este tema contiene las siguientes secciones:

-   [Automatización de la interfaz de usuario y el subproceso de interfaz de usuario](#ui-automation-and-the-ui-thread)
-   [Modelo de subprocesos para controladores de eventos](#threading-model-for-event-handlers)
-   [Afinidad de apartamento COM en Windows](#com-apartment-affinity-on-64-bit-windows)
-   [Temas relacionados](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a>Automatización de la interfaz de usuario y el subproceso de interfaz de usuario

Debido a la forma Automatización de la interfaz de usuario utiliza Windows mensajes, pueden producirse conflictos cuando una aplicación cliente intenta interactuar con su propia interfaz de usuario en el subproceso de la interfaz de usuario. Estos conflictos pueden provocar un rendimiento muy lento o incluso hacer que la aplicación deje de responder.

Si la aplicación cliente está diseñada para interactuar con todos los elementos del escritorio, incluida su propia interfaz de usuario, debe realizar todas las llamadas Automatización de la interfaz de usuario desde un subproceso independiente. Esto incluye buscar elementos, por ejemplo, mediante el uso de [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) o el método [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) y el uso de patrones de control. Este subproceso no debe ser propietario de ninguna ventana y debe ser un subproceso de modelo de multiproceso (MTA) del Modelo de objetos componentes (COM) (uno que inicialice COM mediante una llamada a [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) con la marca **COINIT \_ MULTITHREADED).**

Es seguro realizar llamadas Automatización de la interfaz de usuario en un controlador de eventos Automatización de la interfaz de usuario, ya que siempre se llama al controlador de eventos en un subproceso que no es de interfaz de usuario. Sin embargo, al suscribirse a eventos que pueden originarse desde la interfaz de usuario de la aplicación cliente, debe realizar la llamada a [**IUIAutomation::AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)o a un método relacionado, en un subproceso que no sea de interfaz de usuario (que también debe ser un subproceso MTA). Quite los controladores de eventos que estén en el mismo subproceso.

Un Automatización de la interfaz de usuario cliente no debe usar varios subprocesos para agregar o quitar controladores de eventos. Un comportamiento inesperado puede producirse si se agrega o quita un controlador de eventos mientras se agrega o quita otro en el mismo proceso de cliente.

## <a name="threading-model-for-event-handlers"></a>Modelo de subprocesos para controladores de eventos

Un Automatización de la interfaz de usuario cliente debe usar el modelo de subprocesos MTA com para subprocesos que implementan controladores de eventos. El uso del modelo Single-Threaded Apartment (STA) puede provocar problemas como impedir que los clientes quiten controladores de eventos del subproceso.

## <a name="com-apartment-affinity-on-64-bit-windows"></a>Afinidad de apartamento COM en Windows

Según la especificación COM, la duración de un objeto remoto se rige por la duración del apartamento donde se llama a la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el objeto. Cuando se cierra el apartamento original, también se libera el objeto remoto.

Para los clientes Automatización de la interfaz de usuario, este comportamiento COM puede significar que la duración del asistente remoto de 32/64 (creado por UIAutomationCore.dll) utilizado por un elemento de 32 bits se rige por la duración del apartamento del subproceso que creó el elemento. Si el Automatización de la interfaz de usuario serializa el elemento a otro subproceso, el elemento puede invalidarse cuando se cierra el apartamento de origen. El Automatización de la interfaz de usuario cliente debe controlar estos problemas correctamente al detectar errores al usar elementos de automatización serializados.

El mismo problema puede producirse con un cliente de Automatización de la interfaz de usuario de 32 bits que tiene elementos de 64 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Obtener elementos de UI Automation](uiauto-obtainingelements.md)
</dt> <dt>

[Suscribirse a eventos Automatización de la interfaz de usuario eventos](uiauto-eventsforclients.md)
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[INFO: Descripciones y funcionamiento de modelos de subprocesos OLE](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 