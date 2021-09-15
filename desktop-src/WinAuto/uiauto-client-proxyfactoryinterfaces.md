---
title: Interfaces de generador de proxy para clientes
description: En esta sección se describen las interfaces de generador de proxy para aplicaciones cliente Automatización de la interfaz de usuario no administradas.
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc1827ab36a221dcd7f27e5b2a05de91931b0ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567305"
---
# <a name="proxy-factory-interfaces-for-clients"></a>Interfaces de generador de proxy para clientes

En esta sección se describen las interfaces de generador de proxy para aplicaciones cliente Automatización de la interfaz de usuario no administradas.

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                                                      | Descripción                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | Expone propiedades y métodos de un objeto que crea un proveedor Automatización de la interfaz de usuario Microsoft para elementos de interfaz de usuario que no tienen compatibilidad nativa con Automatización de la interfaz de usuario. Esta interfaz se implementa mediante servidores proxy.<br/>                                                                          |
| [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | Representa un generador de proxy en la tabla mantenida por Automatización de la interfaz de usuario y expone propiedades y métodos que pueden usar las aplicaciones cliente para interactuar con objetos [**IUIAutomationProxyFactory.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>                                   |
| [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | Expone propiedades y métodos para una tabla de generadores de proxy. Cada entrada de tabla se representa mediante una [**interfaz IUIAutomationProxyFactoryEntry.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) Las entradas están en el orden en el que el sistema intentará usar los servidores proxy.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Automatización de la interfaz de usuario clientes](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





