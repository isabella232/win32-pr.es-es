---
title: Automatización de la interfaz de usuario interfaces de elementos para clientes
description: En esta sección se describen las interfaces usadas por microsoft Automatización de la interfaz de usuario cliente para buscar, acceder y consultar elementos Automatización de la interfaz de usuario datos.
ms.assetid: dd7cdcf1-3511-424f-b729-b71a7e11cdd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356bd61a3f4a4626c8cc382c924b62967c01ddb201b8411eaa5451c822ede38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133418"
---
# <a name="ui-automation-element-interfaces-for-clients"></a>Automatización de la interfaz de usuario interfaces de elementos para clientes

En esta sección se describen las interfaces usadas por microsoft Automatización de la interfaz de usuario cliente para buscar, acceder y consultar elementos Automatización de la interfaz de usuario datos.

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)<br/>                         | Expone métodos que permiten que Automatización de la interfaz de usuario cliente detecten, accedan y filtren Automatización de la interfaz de usuario elementos. Automatización de la interfaz de usuario expone todos los elementos del Automatización de la interfaz de usuario como un objeto representado por la [**interfaz IUIAutomation.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) Los miembros de esta interfaz no son específicos de un elemento determinado.<br/> |
| [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2)<br/>                       | Extiende la interfaz [**IUIAutomation para**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) exponer métodos adicionales para controlar Automatización de la interfaz de usuario funcionalidad.<br/>                                                                                                                                                                                                   |
| [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3)<br/>                       | Extiende la interfaz [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2) para exponer métodos adicionales para controlar Automatización de la interfaz de usuario funcionalidad.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4)<br/>                       | Extiende la interfaz [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3) para exponer métodos adicionales para controlar Automatización de la interfaz de usuario funcionalidad.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5)<br/>                       | Extiende la interfaz [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4) para exponer métodos adicionales para controlar Automatización de la interfaz de usuario funcionalidad.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation6)<br/>                       | Extiende la interfaz [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5) para exponer métodos adicionales para controlar Automatización de la interfaz de usuario funcionalidad.<br/>                                                                                                                                                                                                 |
| [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest)<br/> | Expone las propiedades y los métodos de una solicitud de caché. Las aplicaciones cliente usan esta interfaz para especificar las propiedades y los patrones de control que se almacenarán en caché cuando se obtenga Automatización de la interfaz de usuario elemento .<br/>                                                                                                                                                 |
| [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)<br/>           | Expone métodos y propiedades para un elemento Automatización de la interfaz de usuario, que representa un elemento de interfaz de usuario. <br/>                                                                                                                                                                                                                                                        |
| [**IUIAutomationElement2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2)<br/>         | Extiende la [**interfaz IUIAutomationElement.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) <br/>                                                                                                                                                                                                                                                             |
| [**IUIAutomationElement3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3)<br/>         | Extiende la [**interfaz IUIAutomationElement2.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2) <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4)<br/>         | Extiende la [**interfaz IUIAutomationElement3.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3) <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5)<br/>         | Extiende la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) para proporcionar acceso a los datos de punto de referencia actuales y almacenados en caché.<br/>                                                                                                                                                                                                      |
| [**IUIAutomationElement6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6)<br/>         | Extiende la interfaz [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5) para proporcionar acceso a las descripciones completa actuales y almacenadas en caché.<br/>                                                                                                                                                                                                  |
| [**IUIAutomationElement7**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7)<br/>         | Extiende la [**interfaz IUIAutomationElement6.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6)<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement8**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8)<br/>         | Extiende la [**interfaz IUIAutomationElement7.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7)<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement9**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/>         | Extiende la [**interfaz IUIAutomationElement8.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8)<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray)<br/> | Representa una colección de Automatización de la interfaz de usuario elementos.<br/>                                                                                                                                                                                                                                                                                              |
| [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar)<br/>       | Expone métodos para registrar nuevos patrones de control, propiedades y eventos.<br/>                                                                                                                                                                                                                                                                   |
| [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)<br/>     | Expone las propiedades y los métodos que Automatización de la interfaz de usuario aplicaciones cliente usan para ver y navegar por los Automatización de la interfaz de usuario en el escritorio. <br/>                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Automatización de la interfaz de usuario clientes](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





