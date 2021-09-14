---
title: Patrón de control SynchronizedInput
description: Describe directrices y convenciones para implementar ISynchronizedInputProvider, incluida información sobre propiedades y métodos.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control SynchronizedInput
- Automatización de la interfaz de usuario, patrón de control SynchronizedInput
- Automatización de la interfaz de usuario,ISynchronizedInputProvider
- ISynchronizedInputProvider
- implementación de Automatización de la interfaz de usuario de control SynchronizedInput
- Patrones de control SynchronizedInput
- patrones de control,ISynchronizedInputProvider
- patrones de control, implementar Automatización de la interfaz de usuario SynchronizedInput
- patrones de control,SynchronizedInput
- interfaces,ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070475"
---
# <a name="synchronizedinput-control-pattern"></a>Patrón de control SynchronizedInput

Describe directrices y convenciones para implementar [**ISynchronizedInputProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider)incluida información sobre propiedades y métodos. El patrón de control **SynchronizedInput** permite a Microsoft Automatización de la interfaz de usuario cliente dirigir la entrada del mouse o el teclado a un elemento de interfaz de usuario específico.

Este patrón de control se usa normalmente en scripts de prueba automatizados para enviar entradas de mouse o teclado a un elemento específico de la interfaz de usuario y, a continuación, comprobar que el elemento recibió la entrada.

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **ISynchronizedInputProvider**](#required-members-for-isynchronizedinputprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **SynchronizedInput,** tenga en cuenta las siguientes directrices y convenciones:

-   Cuando se llama al método [**ISynchronizedInputProvider::StartListening,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) el proveedor de Automatización de la interfaz de usuario debe empezar a comprobar la entrada del tipo especificado y, a continuación, realizar una de las siguientes acciones:
    -   Cuando se encuentra la entrada correspondiente para el elemento , el proveedor debe generar el evento [**\_ InputReachedTargetEventId de UIA.**](uiauto-event-ids.md)
    -   Cuando se encuentra la entrada correspondiente, pero se alcanza un elemento diferente, el proveedor debe generar el evento [**\_ InputReachedOtherElementEventId de UIA.**](uiauto-event-ids.md)
    -   Cuando se encuentra una entrada no coincidente, el proveedor debe descartar la entrada y generar el evento [**\_ InputDiscardedEventId de UIA.**](uiauto-event-ids.md)
-   El Automatización de la interfaz de usuario debe descartar la entrada si es para un elemento distinto del elemento actual.
-   Cuando el elemento recibe la entrada o cuando se llama al método [**ISynchronizedInputProvider::Cancel,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) el proveedor deja de comprobar la entrada y continúa con normalidad.
-   Si se llama a [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) cuando el proveedor ya está escuchando la entrada, el proveedor debe devolver [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md).

## <a name="required-members-for-isynchronizedinputprovider"></a>Miembros necesarios para **ISynchronizedInputProvider**

Las siguientes propiedades, métodos y eventos son necesarios para implementar la [**interfaz ISynchronizedInputProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider)



| Miembros requeridos                                                                         | Tipo de miembro | Notas |
|------------------------------------------------------------------------------------------|-------------|-------|
| [**StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | Método      | None  |
| [**Cancelar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | Método      | None  |
| [**\_InputReachedTargetEventId de UIA**](uiauto-event-ids.md) | Evento       | None  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




