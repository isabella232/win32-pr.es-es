---
description: Un proveedor de consumidores de eventos es un componente de la arquitectura de consumidor permanente que determina qué consumidor de eventos permanente controla un evento determinado.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Escribir un proveedor de consumidor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c7aeeb9b44b37d887df49cf5049d5a9e59ad72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706557"
---
# <a name="writing-an-event-consumer-provider"></a><span data-ttu-id="d7197-103">Escribir un proveedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="d7197-103">Writing an Event Consumer Provider</span></span>

<span data-ttu-id="d7197-104">Un proveedor de consumidores de eventos es un componente de la arquitectura de consumidor permanente que determina qué consumidor de eventos permanente controla un evento determinado.</span><span class="sxs-lookup"><span data-stu-id="d7197-104">An event consumer provider is a component of the permanent consumer architecture that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="d7197-105">Debe crear un proveedor de consumidor de eventos junto con los consumidores de eventos permanentes para enrutar los eventos correctamente desde WMI.</span><span class="sxs-lookup"><span data-stu-id="d7197-105">You should create an event consumer provider along with your permanent event consumers to route events properly from WMI.</span></span>

<span data-ttu-id="d7197-106">Un proveedor de consumidor de eventos vincula un proveedor de eventos con una lista de clases de consumidor.</span><span class="sxs-lookup"><span data-stu-id="d7197-106">An event consumer provider links an event provider with a list of consumer classes.</span></span> <span data-ttu-id="d7197-107">Las instancias de estas clases de consumidor reciben los eventos de ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="d7197-107">Instances of these consumer classes then receive events from that provider.</span></span> <span data-ttu-id="d7197-108">WMI identifica el proveedor de consumidores en el que se entregan los eventos, en función de la instancia de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , que asocia la instancia del proveedor de consumidores [**\_ \_ Win32Provider**](--win32provider.md) a una clase de consumidor lógico.</span><span class="sxs-lookup"><span data-stu-id="d7197-108">WMI identifies which consumer provider the events are delivered to, based on the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) instance, which associates the consumer provider [**\_\_Win32Provider**](--win32provider.md) instance with a logical consumer class.</span></span> <span data-ttu-id="d7197-109">Los usuarios crean instancias de la clase Consumer como parte de una suscripción permanente.</span><span class="sxs-lookup"><span data-stu-id="d7197-109">Users create instances of the consumer class as part of a permanent subscription.</span></span> <span data-ttu-id="d7197-110">Si el proveedor de eventos no se está ejecutando cuando se produce un evento, WMI inicia el proveedor cuando necesita proporcionar eventos.</span><span class="sxs-lookup"><span data-stu-id="d7197-110">If the event provider is not running when an event occurs, then WMI starts the provider when it needs to deliver events.</span></span>

<span data-ttu-id="d7197-111">En el procedimiento siguiente se describe cómo implementar un proveedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="d7197-111">The following procedure describes how to implement an event consumer provider.</span></span>

<span data-ttu-id="d7197-112">**Para implementar un proveedor de consumidor de eventos**</span><span class="sxs-lookup"><span data-stu-id="d7197-112">**To implement an event consumer provider**</span></span>

1.  <span data-ttu-id="d7197-113">Diseñe clases de consumidor en Managed Object Format (MOF) y regístrela en WMI.</span><span class="sxs-lookup"><span data-stu-id="d7197-113">Design consumer classes in Managed Object Format (MOF) and register them with WMI.</span></span> <span data-ttu-id="d7197-114">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="d7197-114">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

    <span data-ttu-id="d7197-115">Los proveedores de clases se registran en WMI mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y una clase [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="d7197-115">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class.</span></span> <span data-ttu-id="d7197-116">Para obtener más información, vea [registrar un proveedor de consumidor de eventos](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d7197-116">For more information, see [Registering an Event Consumer Provider](registering-an-event-consumer-provider.md).</span></span>

2.  <span data-ttu-id="d7197-117">Implemente la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d7197-117">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="d7197-118">WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para cargar e inicializar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="d7197-118">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="d7197-119">Para obtener más información, vea [inicializar un proveedor](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d7197-119">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="d7197-120">Se recomienda encarecidamente a los proveedores de consumidores de eventos que utilicen el modelo de multithreading "both".</span><span class="sxs-lookup"><span data-stu-id="d7197-120">Event consumer providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="d7197-121">Implemente la interfaz [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d7197-121">Implement the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface for your provider.</span></span>

    <span data-ttu-id="d7197-122">La interfaz [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) es la interfaz principal para un proveedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="d7197-122">The [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface is the primary interface for an event consumer provider.</span></span>

4.  <span data-ttu-id="d7197-123">Proporcione uno o más consumidores físicos para recibir los mensajes de eventos de WMI.</span><span class="sxs-lookup"><span data-stu-id="d7197-123">Supply one or more physical consumers to receive the event messages from WMI.</span></span>

    <span data-ttu-id="d7197-124">Un consumidor físico es un objeto COM que representa un consumidor de eventos permanente.</span><span class="sxs-lookup"><span data-stu-id="d7197-124">A physical consumer is a COM object that represents a permanent event consumer.</span></span> <span data-ttu-id="d7197-125">Todos los consumidores físicos deben implementar la interfaz [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) .</span><span class="sxs-lookup"><span data-stu-id="d7197-125">All physical consumers must implement the [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) interface.</span></span> <span data-ttu-id="d7197-126">Para obtener más información, consulte [implementación de un consumidor físico](implementing-a-physical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="d7197-126">For more information, see [Implementing a Physical Consumer](implementing-a-physical-consumer.md).</span></span>

 

 



