---
title: Funciones para proveedores
description: En esta sección se describen las funciones del proveedor de automatización de la interfaz de usuario para las aplicaciones de Microsoft Win32.
ms.assetid: 76012ec7-0114-4b6b-a35e-5cfde5b90230
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0542c3d0b313e1bed8ec040924349e37a29fea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685716"
---
# <a name="functions-for-providers"></a>Funciones para proveedores

En esta sección se describen las funciones del proveedor de automatización de la interfaz de usuario para las aplicaciones de Microsoft Win32.

## <a name="in-this-section"></a>En esta sección



| Función                                                                                                 | Descripción                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)<br/>                       | Obtiene un valor que indica si alguna aplicación cliente está suscrita a eventos de automatización de la interfaz de usuario de Microsoft.<br/>                                             |
| [**UiaDisconnectAllProviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders)<br/>                         | Libera todos los recursos de automatización de la interfaz de usuario retenidos por todos los proveedores asociados al proceso de llamada. <br/>                                               |
| [**UiaDisconnectProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider)<br/>                                 | Libera todas las referencias que un proveedor determinado contiene a objetos de automatización de la interfaz de usuario.<br/>                                                                      |
| [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue)<br/> | Recupera un valor reservado que indica que el valor de un atributo de texto de automatización de la interfaz de usuario varía dentro de un intervalo de texto.<br/>                                      |
| [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue)<br/>     | Recupera un valor reservado que indica que no se admite una propiedad de automatización de la interfaz de usuario ni un atributo de texto.<br/>                                               |
| [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)<br/>                     | Obtiene el proveedor de host para una ventana.<br/>                                                                                                                    |
| [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider)<br/>                   | Recupera una implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que proporciona datos de Microsoft Active Accessibility en nombre de un proveedor de automatización de la interfaz de usuario.<br/> |
| [**UiaProviderForNonClient**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfornonclient)<br/>                     | Obtiene el proveedor para todo el área no cliente de una ventana o para un control en el área no cliente de una ventana.<br/>                                      |
| [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible)<br/>               | Crea un proveedor de automatización de la interfaz de usuario basado en el objeto de Microsoft Active Accessibility especificado.<br/>                                                          |
| [**UiaRaiseAsyncContentLoadedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseasynccontentloadedevent)<br/>     | Lo llama un proveedor para notificar al núcleo de automatización de la interfaz de usuario que el contenido se carga de forma asincrónica.<br/>                                                      |
| [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)<br/>                     | Notifica a los agentes de escucha de un evento.<br/>                                                                                                                         |
| [**UiaRaiseAutomationPropertyChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent)<br/>    | Los proveedores llaman a este método para notificar al núcleo de automatización de la interfaz de usuario que una propiedad de elemento ha cambiado.<br/>                                                              |
| [**UiaRaiseChangesEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisechangesevent)<br/>                           | Lo llaman los proveedores para notificar al núcleo de automatización de la interfaz de usuario que se ha producido un cambio.<br/>                                                                        |
| [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**)<br/>             | Lo llaman los proveedores para iniciar un evento de notificación.<br/>                                                                                                   |
| [**UiaRaiseStructureChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)<br/>         | Lo llama un proveedor para notificar al núcleo de automatización de la interfaz de usuario que la estructura de árbol ha cambiado.<br/>                                                              |
| [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent)<br/>   | Lo llama un proveedor para notificar al núcleo de automatización de la interfaz de usuario que un control de texto ha cambiado el texto mediante programación.<br/>                                            |
| [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)<br/>             | Obtiene una interfaz para el proveedor de automatización de la interfaz de usuario de una ventana.<br/>                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores de UI Automation](uiauto-entry-uiautoprovidersforwin32apps.md)
</dt> </dl>

 

