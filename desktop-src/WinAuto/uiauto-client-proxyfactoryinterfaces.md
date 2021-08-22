---
title: Interfaces de generador de proxy para clientes
description: En esta sección se describen las interfaces de generador de proxy para aplicaciones cliente de Automatización de la interfaz de usuario no administradas.
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e92264691c35cefe3ffaf246d2e73bac5ea7dc3363a4f220eb0ddecb9f15030
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614365"
---
# <a name="proxy-factory-interfaces-for-clients"></a>Interfaces de generador de proxy para clientes

En esta sección se describen las interfaces de generador de proxy para aplicaciones cliente de Automatización de la interfaz de usuario no administradas.

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                                                      | Descripción                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | Expone propiedades y métodos de un objeto que crea un proveedor de Automatización de la interfaz de usuario microsoft para elementos de interfaz de usuario que no tienen compatibilidad nativa con Automatización de la interfaz de usuario. Esta interfaz se implementa mediante servidores proxy.<br/>                                                                          |
| [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | Representa un generador de proxy en la tabla mantenida por Automatización de la interfaz de usuario y expone propiedades y métodos que pueden usar las aplicaciones cliente para interactuar con objetos [**IUIAutomationProxyFactory.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>                                   |
| [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | Expone propiedades y métodos para una tabla de generadores de proxy. Cada entrada de tabla se representa mediante una [**interfaz IUIAutomationProxyFactoryEntry.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) Las entradas están en el orden en el que el sistema intentará usar los servidores proxy.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Automatización de la interfaz de usuario clientes](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





