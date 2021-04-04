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
# <a name="proxy-factory-interfaces-for-clients"></a><span data-ttu-id="1c8de-103">Interfaces de generador de proxy para clientes</span><span class="sxs-lookup"><span data-stu-id="1c8de-103">Proxy Factory Interfaces for Clients</span></span>

<span data-ttu-id="1c8de-104">En esta sección se describen las interfaces de generador de proxy para las aplicaciones cliente de automatización de la interfaz de usuario no administradas.</span><span class="sxs-lookup"><span data-stu-id="1c8de-104">This section describes the proxy factory interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1c8de-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1c8de-105">In this section</span></span>



| <span data-ttu-id="1c8de-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="1c8de-106">Interface</span></span>                                                                                      | <span data-ttu-id="1c8de-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c8de-107">Description</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c8de-108">**IUIAutomationProxyFactory**</span><span class="sxs-lookup"><span data-stu-id="1c8de-108">**IUIAutomationProxyFactory**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | <span data-ttu-id="1c8de-109">Expone propiedades y métodos de un objeto que crea un proveedor de automatización de la interfaz de usuario de Microsoft para los elementos de la interfaz de usuario que no tienen compatibilidad nativa con la automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1c8de-109">Exposes properties and methods of an object that creates a Microsoft UI Automation provider for UI elements that do not have native support for UI Automation.</span></span> <span data-ttu-id="1c8de-110">Esta interfaz la implementan los servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="1c8de-110">This interface is implemented by proxies.</span></span><br/>                                                                          |
| [<span data-ttu-id="1c8de-111">**IUIAutomationProxyFactoryEntry**</span><span class="sxs-lookup"><span data-stu-id="1c8de-111">**IUIAutomationProxyFactoryEntry**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | <span data-ttu-id="1c8de-112">Representa un generador de proxy en la tabla que mantiene la automatización de la interfaz de usuario y expone propiedades y métodos que las aplicaciones cliente pueden usar para interactuar con los objetos [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) .</span><span class="sxs-lookup"><span data-stu-id="1c8de-112">Represents a proxy factory in the table maintained by UI Automation, and exposes properties and methods that can be used by client applications to interact with [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) objects.</span></span><br/>                                   |
| [<span data-ttu-id="1c8de-113">**IUIAutomationProxyFactoryMapping**</span><span class="sxs-lookup"><span data-stu-id="1c8de-113">**IUIAutomationProxyFactoryMapping**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | <span data-ttu-id="1c8de-114">Expone propiedades y métodos para una tabla de generadores de proxy.</span><span class="sxs-lookup"><span data-stu-id="1c8de-114">Exposes properties and methods for a table of proxy factories.</span></span> <span data-ttu-id="1c8de-115">Cada entrada de la tabla se representa mediante una interfaz [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) .</span><span class="sxs-lookup"><span data-stu-id="1c8de-115">Each table entry is represented by an [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) interface.</span></span> <span data-ttu-id="1c8de-116">Las entradas se encuentran en el orden en que el sistema intentará usar los servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="1c8de-116">The entries are in the order in which the system will attempt to use the proxies.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1c8de-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c8de-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c8de-118">Clientes de UI Automation</span><span class="sxs-lookup"><span data-stu-id="1c8de-118">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





