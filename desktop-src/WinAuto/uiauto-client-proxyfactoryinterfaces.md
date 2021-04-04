---
title: Interfaces de generador de proxy para clientes
description: En esta sección se describen las interfaces de generador de proxy para las aplicaciones cliente de automatización de la interfaz de usuario no administradas.
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc1827ab36a221dcd7f27e5b2a05de91931b0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076218"
---
# <a name="proxy-factory-interfaces-for-clients"></a>Interfaces de generador de proxy para clientes

En esta sección se describen las interfaces de generador de proxy para las aplicaciones cliente de automatización de la interfaz de usuario no administradas.

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                                                      | Descripción                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | Expone propiedades y métodos de un objeto que crea un proveedor de automatización de la interfaz de usuario de Microsoft para los elementos de la interfaz de usuario que no tienen compatibilidad nativa con la automatización de la interfaz de usuario. Esta interfaz la implementan los servidores proxy.<br/>                                                                          |
| [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | Representa un generador de proxy en la tabla que mantiene la automatización de la interfaz de usuario y expone propiedades y métodos que las aplicaciones cliente pueden usar para interactuar con los objetos [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) .<br/>                                   |
| [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | Expone propiedades y métodos para una tabla de generadores de proxy. Cada entrada de la tabla se representa mediante una interfaz [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) . Las entradas se encuentran en el orden en que el sistema intentará usar los servidores proxy.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes de UI Automation](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





