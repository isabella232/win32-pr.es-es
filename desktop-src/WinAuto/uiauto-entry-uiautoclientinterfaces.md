---
title: Interfaces de elementos de UI Automation para clientes
description: En esta sección se describen las interfaces utilizadas por el cliente de automatización de la interfaz de usuario de Microsoft para buscar, acceder y consultar elementos de automatización de la interfaz de usuario.
ms.assetid: dd7cdcf1-3511-424f-b729-b71a7e11cdd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a08859784d18905adbed463ac776bb2e717211f
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/05/2021
ms.locfileid: "103997617"
---
# <a name="ui-automation-element-interfaces-for-clients"></a>Interfaces de elementos de UI Automation para clientes

En esta sección se describen las interfaces utilizadas por el cliente de automatización de la interfaz de usuario de Microsoft para buscar, acceder y consultar elementos de automatización de la interfaz de usuario.

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)<br/>                         | Expone métodos que permiten a las aplicaciones cliente de automatización de la interfaz de usuario detectar, acceder y filtrar elementos de automatización de la interfaz de usuario. La automatización de la interfaz de usuario expone todos los elementos de la automatización de la interfaz de usuario como un objeto representado por la interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) . Los miembros de esta interfaz no son específicos de un elemento determinado.<br/> |
| [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2)<br/>                       | Extiende la interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) para exponer métodos adicionales para controlar la funcionalidad de automatización de la interfaz de usuario.<br/>                                                                                                                                                                                                   |
| [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3)<br/>                       | Extiende la interfaz [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2) para exponer métodos adicionales para controlar la funcionalidad de automatización de la interfaz de usuario.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4)<br/>                       | Extiende la interfaz [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3) para exponer métodos adicionales para controlar la funcionalidad de automatización de la interfaz de usuario.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5)<br/>                       | Extiende la interfaz [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4) para exponer métodos adicionales para controlar la funcionalidad de automatización de la interfaz de usuario.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation6)<br/>                       | Extiende la interfaz [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5) para exponer métodos adicionales para controlar la funcionalidad de automatización de la interfaz de usuario.<br/>                                                                                                                                                                                                 |
| [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest)<br/> | Expone propiedades y métodos de una solicitud de caché. Las aplicaciones cliente utilizan esta interfaz para especificar las propiedades y los patrones de control que se van a almacenar en caché cuando se obtiene un elemento de automatización de la interfaz de usuario.<br/>                                                                                                                                                 |
| [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)<br/>           | Expone métodos y propiedades para un elemento de automatización de la interfaz de usuario, que representa un elemento de la interfaz de usuario. <br/>                                                                                                                                                                                                                                                        |
| [**IUIAutomationElement2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2)<br/>         | Extiende la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . <br/>                                                                                                                                                                                                                                                             |
| [**IUIAutomationElement3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3)<br/>         | Extiende la interfaz [**IUIAutomationElement2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2) . <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4)<br/>         | Extiende la interfaz [**IUIAutomationElement3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3) . <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5)<br/>         | Extiende la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) para proporcionar acceso a los datos de punto de referencia actuales y almacenados en caché.<br/>                                                                                                                                                                                                      |
| [**IUIAutomationElement6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6)<br/>         | Extiende la interfaz [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5) para proporcionar acceso a las descripciones completas actuales y almacenadas en caché.<br/>                                                                                                                                                                                                  |
| [**IUIAutomationElement7**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7)<br/>         | Extiende la interfaz [**IUIAutomationElement6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6) .<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement8**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8)<br/>         | Extiende la interfaz [**IUIAutomationElement7**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7) .<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement9**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/>         | Extiende la interfaz [**IUIAutomationElement8**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8) .<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray)<br/> | Representa una colección de elementos de automatización de la interfaz de usuario.<br/>                                                                                                                                                                                                                                                                                              |
| [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar)<br/>       | Expone métodos para registrar nuevos patrones de control, propiedades y eventos.<br/>                                                                                                                                                                                                                                                                   |
| [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)<br/>     | Expone propiedades y métodos que las aplicaciones cliente de automatización de la interfaz de usuario usan para ver y navegar por los elementos de automatización de la interfaz de usuario en el escritorio. <br/>                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes de UI Automation](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





