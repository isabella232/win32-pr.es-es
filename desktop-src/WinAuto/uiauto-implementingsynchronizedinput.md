---
title: Patrón de control SynchronizedInput
description: Describe las directrices y convenciones para implementar ISynchronizedInputProvider, incluida información sobre propiedades y métodos.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control SynchronizedInput
- Automatización de la interfaz de usuario, patrón de control SynchronizedInput
- Automatización de la interfaz de usuario, ISynchronizedInputProvider
- ISynchronizedInputProvider
- implementación de patrones de control SynchronizedInput de UI Automation
- Patrones de control de SynchronizedInput
- patrones de control, ISynchronizedInputProvider
- patrones de control, implementar la automatización de la interfaz de usuario SynchronizedInput
- patrones de control, SynchronizedInput
- interfaces, ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704735"
---
# <a name="synchronizedinput-control-pattern"></a>Patrón de control SynchronizedInput

Describe las directrices y convenciones para implementar [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), incluida información sobre propiedades y métodos. El patrón de control **SynchronizedInput** permite a las aplicaciones cliente de automatización de la interfaz de usuario de Microsoft dirigir la entrada del mouse o del teclado a un elemento específico de la interfaz de usuario.

Este patrón de control se usa normalmente en scripts de pruebas automatizadas para enviar la entrada del mouse o del teclado a un elemento específico de la interfaz de usuario y, a continuación, comprobar que el elemento ha recibido la entrada.

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **ISynchronizedInputProvider**](#required-members-for-isynchronizedinputprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **SynchronizedInput** , tenga en cuenta las siguientes directrices y convenciones:

-   Cuando se llama al método [**ISynchronizedInputProvider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) , el proveedor de automatización de la interfaz de usuario debe iniciar la comprobación de la entrada del tipo especificado y, a continuación, realizar una de las siguientes acciones:
    -   Cuando se encuentra una entrada coincidente para el elemento, el proveedor debe generar el evento de [**\_ InputReachedTargetEventId de UIA**](uiauto-event-ids.md) .
    -   Cuando se encuentra la entrada coincidente, pero alcanzó un elemento diferente, el proveedor debe generar el evento de [**\_ InputReachedOtherElementEventId de UIA**](uiauto-event-ids.md) .
    -   Cuando se encuentra una entrada no coincidente, el proveedor debe descartar la entrada y generar el evento [**\_ InputDiscardedEventId de UIA**](uiauto-event-ids.md) .
-   El proveedor de automatización de la interfaz de usuario debe descartar la entrada si es para un elemento distinto del elemento actual.
-   Cuando el elemento recibe la entrada, o cuando se llama al método [**ISynchronizedInputProvider:: CANCEL**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) , el proveedor detiene la comprobación de la entrada y continúa de la forma habitual.
-   Si se llama a [**ISynchronizedInputProvider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) cuando el proveedor ya está escuchando la entrada, el proveedor debe devolver [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md).

## <a name="required-members-for-isynchronizedinputprovider"></a>Miembros requeridos para **ISynchronizedInputProvider**

Se requieren las siguientes propiedades, métodos y eventos para implementar la interfaz [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) .



| Miembros requeridos                                                                         | Tipo de miembro | Notas |
|------------------------------------------------------------------------------------------|-------------|-------|
| [**StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | Método      | None  |
| [**Cancelar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | Método      | None  |
| [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) | Evento       | None  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




