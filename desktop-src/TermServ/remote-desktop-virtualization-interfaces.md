---
title: Interfaces de virtualización Escritorio remoto
description: La API de virtualización de Escritorio remoto admite las siguientes interfaces.
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359175"
---
# <a name="remote-desktop-virtualization-interfaces"></a><span data-ttu-id="c48f8-103">Interfaces de virtualización Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="c48f8-103">Remote Desktop Virtualization Interfaces</span></span>

<span data-ttu-id="c48f8-104">La API de virtualización de Escritorio remoto admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="c48f8-104">The Remote Desktop Virtualization API supports the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c48f8-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c48f8-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="c48f8-106">**ITsSbBaseNotifySink**</span><span class="sxs-lookup"><span data-stu-id="c48f8-106">**ITsSbBaseNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

<span data-ttu-id="c48f8-107">Expone métodos que notifican el estado y los mensajes de error a Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="c48f8-107">Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-108">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="c48f8-108">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

<span data-ttu-id="c48f8-109">Expone métodos y propiedades que almacenan información de estado sobre una solicitud de conexión entrante desde un cliente Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="c48f8-109">Exposes methods and properties that store state information about an incoming connection request from a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-110">**ITsSbClientConnectionPropertySet**</span><span class="sxs-lookup"><span data-stu-id="c48f8-110">**ITsSbClientConnectionPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

<span data-ttu-id="c48f8-111">Se puede usar para definir las propiedades personalizadas de una conexión de cliente según corresponda.</span><span class="sxs-lookup"><span data-stu-id="c48f8-111">Can be used to define custom properties of a client connection as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-112">**ITsSbEnvironment**</span><span class="sxs-lookup"><span data-stu-id="c48f8-112">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

<span data-ttu-id="c48f8-113">Expone métodos y propiedades que contienen información sobre el entorno que hospeda el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="c48f8-113">Exposes methods and properties that contain information about the environment that hosts the target computer.</span></span> <span data-ttu-id="c48f8-114">Esta interfaz se puede usar para almacenar información sobre un servidor físico que hospeda máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="c48f8-114">This interface can be used to store information about a physical server that hosts virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-115">**ITsSbEnvironmentPropertySet**</span><span class="sxs-lookup"><span data-stu-id="c48f8-115">**ITsSbEnvironmentPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

<span data-ttu-id="c48f8-116">Se puede usar para definir las propiedades personalizadas de un entorno que hospede los equipos de destino según corresponda.</span><span class="sxs-lookup"><span data-stu-id="c48f8-116">Can be used to define custom properties of an environment that hosts target computers as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-117">**ITsSbFilterPluginStore**</span><span class="sxs-lookup"><span data-stu-id="c48f8-117">**ITsSbFilterPluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

<span data-ttu-id="c48f8-118">Filtrar el almacén de complementos</span><span class="sxs-lookup"><span data-stu-id="c48f8-118">Filter Plugin Store</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-119">**ITsSbGenericNotifySink**</span><span class="sxs-lookup"><span data-stu-id="c48f8-119">**ITsSbGenericNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

<span data-ttu-id="c48f8-120">Expone métodos que notifican la finalización de y obtiene el tiempo de espera del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c48f8-120">Exposes methods that reports completion to and gets wait time from the RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-121">**ITsSbGlobalStore**</span><span class="sxs-lookup"><span data-stu-id="c48f8-121">**ITsSbGlobalStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

<span data-ttu-id="c48f8-122">Expone métodos que consultan los equipos de destino, las sesiones, los entornos y las granjas de servidores que se han agregado al almacén de agentes de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c48f8-122">Exposes methods that query for target computers, sessions, environments, and farms that have been added to the RD Connection Broker store.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-123">**ITsSbLoadBalanceResult**</span><span class="sxs-lookup"><span data-stu-id="c48f8-123">**ITsSbLoadBalanceResult**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

<span data-ttu-id="c48f8-124">Expone métodos y propiedades que almacenan el nombre de destino devuelto por un algoritmo de equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="c48f8-124">Exposes methods and properties that store the target name returned by a load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-125">**ITsSbLoadBalancing**</span><span class="sxs-lookup"><span data-stu-id="c48f8-125">**ITsSbLoadBalancing**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

<span data-ttu-id="c48f8-126">Expone métodos que se pueden usar para proporcionar un algoritmo de equilibrio de carga personalizado.</span><span class="sxs-lookup"><span data-stu-id="c48f8-126">Exposes methods you can use to provide a custom load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-127">**ITsSbLoadBalancingNotifySink**</span><span class="sxs-lookup"><span data-stu-id="c48f8-127">**ITsSbLoadBalancingNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

<span data-ttu-id="c48f8-128">Expone métodos que devuelven el resultado de un algoritmo de equilibrio de carga al agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c48f8-128">Exposes methods that return the result of a load-balancing algorithm to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-129">**ITsSbOrchestration**</span><span class="sxs-lookup"><span data-stu-id="c48f8-129">**ITsSbOrchestration**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

<span data-ttu-id="c48f8-130">Expone los métodos que usa el agente de conexión a escritorio remoto para asegurarse de que el destino está listo antes de que un cliente se redirija a él.</span><span class="sxs-lookup"><span data-stu-id="c48f8-130">Exposes methods that RD Connection Broker uses to ensure that the target is ready before a client is redirected to it.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-131">**ITsSbOrchestrationNotifySink**</span><span class="sxs-lookup"><span data-stu-id="c48f8-131">**ITsSbOrchestrationNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

<span data-ttu-id="c48f8-132">Expone métodos que devuelven un objeto [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) al agente de conexión a escritorio remoto después de preparar correctamente el destino para una conexión.</span><span class="sxs-lookup"><span data-stu-id="c48f8-132">Exposes methods that return an [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) object to RD Connection Broker after the target is successfully prepared for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-133">**ITsSbPlacement**</span><span class="sxs-lookup"><span data-stu-id="c48f8-133">**ITsSbPlacement**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

<span data-ttu-id="c48f8-134">Expone métodos que preparan el entorno (el equipo que hospeda la máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="c48f8-134">Exposes methods that prepare the environment (the computer that hosts the virtual machine).</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-135">**ITsSbPlacementNotifySink**</span><span class="sxs-lookup"><span data-stu-id="c48f8-135">**ITsSbPlacementNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

<span data-ttu-id="c48f8-136">Expone métodos que devuelven información acerca de los entornos al agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c48f8-136">Exposes methods that return information about environments to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-137">**ITsSbPlugin**</span><span class="sxs-lookup"><span data-stu-id="c48f8-137">**ITsSbPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

<span data-ttu-id="c48f8-138">Expone métodos que inicializan y terminan complementos.</span><span class="sxs-lookup"><span data-stu-id="c48f8-138">Exposes methods that initialize and terminate plug-ins.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-139">**ITsSbPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="c48f8-139">**ITsSbPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

<span data-ttu-id="c48f8-140">Expone métodos que envían una notificación al agente de conexión a escritorio remoto sobre la inicialización o terminación de un complemento.</span><span class="sxs-lookup"><span data-stu-id="c48f8-140">Exposes methods that notify RD Connection Broker about initialization or termination of a plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-141">**ITsSbPluginPropertySet**</span><span class="sxs-lookup"><span data-stu-id="c48f8-141">**ITsSbPluginPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

<span data-ttu-id="c48f8-142">Se puede usar para definir las propiedades del complemento personalizado según corresponda.</span><span class="sxs-lookup"><span data-stu-id="c48f8-142">Can be used to define custom plug-in properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-143">**ITsSbPropertySet**</span><span class="sxs-lookup"><span data-stu-id="c48f8-143">**ITsSbPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

<span data-ttu-id="c48f8-144">Se puede usar para definir las propiedades personalizadas según corresponda.</span><span class="sxs-lookup"><span data-stu-id="c48f8-144">Can be used to define custom properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-145">**ITsSbProvider**</span><span class="sxs-lookup"><span data-stu-id="c48f8-145">**ITsSbProvider**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

<span data-ttu-id="c48f8-146">Expone métodos que crean implementaciones predeterminadas de objetos que se usan en Escritorio remoto virtualización.</span><span class="sxs-lookup"><span data-stu-id="c48f8-146">Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-147">**ITsSbProvisioning**</span><span class="sxs-lookup"><span data-stu-id="c48f8-147">**ITsSbProvisioning**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

<span data-ttu-id="c48f8-148">Expone métodos que crean y mantienen máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="c48f8-148">Exposes methods that create and maintain virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-149">**ITsSbProvisioningPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="c48f8-149">**ITsSbProvisioningPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

<span data-ttu-id="c48f8-150">Expone métodos que notifican al agente de conexión a escritorio remoto sobre el aprovisionamiento de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="c48f8-150">Exposes methods that notify RD Connection Broker about the provisioning of virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-151">**ITsSbResourceNotification**</span><span class="sxs-lookup"><span data-stu-id="c48f8-151">**ITsSbResourceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

<span data-ttu-id="c48f8-152">Expone métodos que el agente de conexión a escritorio remoto usa para notificar complementos de cualquier cambio de estado que se produzca en los objetos de conexión de cliente, destino y sesión.</span><span class="sxs-lookup"><span data-stu-id="c48f8-152">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-153">**ITsSbResourceNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="c48f8-153">**ITsSbResourceNotificationEx**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

<span data-ttu-id="c48f8-154">Expone métodos que el agente de conexión a escritorio remoto usa para notificar complementos de cualquier cambio de estado que se produzca en los objetos de conexión de cliente, destino y sesión.</span><span class="sxs-lookup"><span data-stu-id="c48f8-154">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-155">**ITsSbResourcePlugin**</span><span class="sxs-lookup"><span data-stu-id="c48f8-155">**ITsSbResourcePlugin**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

<span data-ttu-id="c48f8-156">Expone métodos que amplían las capacidades del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c48f8-156">Exposes methods that extend the capabilities of RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-157">**ITsSbResourcePluginStore**</span><span class="sxs-lookup"><span data-stu-id="c48f8-157">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

<span data-ttu-id="c48f8-158">Expone métodos que permiten a los complementos de recursos almacenar objetos como sesiones y destinos.</span><span class="sxs-lookup"><span data-stu-id="c48f8-158">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-159">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="c48f8-159">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> <dd>

<span data-ttu-id="c48f8-160">Expone métodos que permiten a los complementos de recursos almacenar objetos como sesiones y destinos.</span><span class="sxs-lookup"><span data-stu-id="c48f8-160">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-161">**ITsSbServiceNotification**</span><span class="sxs-lookup"><span data-stu-id="c48f8-161">**ITsSbServiceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

<span data-ttu-id="c48f8-162">Expone los métodos que usa el agente de conexión a escritorio remoto para notificar los complementos de los cambios de estado que se producen en el propio agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c48f8-162">Exposes methods that RD Connection Broker uses to notify plug-ins of state changes that occur in the RD Connection Broker itself.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-163">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="c48f8-163">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

<span data-ttu-id="c48f8-164">Expone propiedades que almacenan información sobre una sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="c48f8-164">Exposes properties that store information about a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-165">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="c48f8-165">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

<span data-ttu-id="c48f8-166">Expone propiedades que almacenan información de configuración y estado sobre un destino.</span><span class="sxs-lookup"><span data-stu-id="c48f8-166">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-167">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="c48f8-167">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dd>

<span data-ttu-id="c48f8-168">Expone propiedades que almacenan información de configuración y estado sobre un destino.</span><span class="sxs-lookup"><span data-stu-id="c48f8-168">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-169">**ITsSbTargetPropertySet**</span><span class="sxs-lookup"><span data-stu-id="c48f8-169">**ITsSbTargetPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

<span data-ttu-id="c48f8-170">Derive de esta interfaz para definir un conjunto de propiedades de destino personalizado.</span><span class="sxs-lookup"><span data-stu-id="c48f8-170">Derive from this interface to define a custom target property set.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-171">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="c48f8-171">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

<span data-ttu-id="c48f8-172">Expone propiedades que el agente de Conexión a Escritorio remoto usa para establecer la cola de un complemento.</span><span class="sxs-lookup"><span data-stu-id="c48f8-172">Exposes properties that the Remote Desktop Connection Broker uses to set a plugin’s queue.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-173">**ITsSbTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="c48f8-173">**ITsSbTaskPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

<span data-ttu-id="c48f8-174">Expone métodos que actualizan la cola de tareas para los complementos de Conexión a Escritorio remoto Broker.</span><span class="sxs-lookup"><span data-stu-id="c48f8-174">Exposes methods that update the queue of tasks for Remote Desktop Connection Broker plugins.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-175">**ITsSbTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="c48f8-175">**ITsSbTaskPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

<span data-ttu-id="c48f8-176">Expone métodos que notifican el estado y los mensajes de error sobre las tareas del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c48f8-176">Exposes methods that report status and error messages about tasks to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="c48f8-177">**IWTSSBPlugin**</span><span class="sxs-lookup"><span data-stu-id="c48f8-177">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

<span data-ttu-id="c48f8-178">Se usa para ampliar las capacidades de Terminal Services agente de sesiones (agente de sesiones de TS).</span><span class="sxs-lookup"><span data-stu-id="c48f8-178">Used to extend the capabilities of Terminal Services Session Broker (TS Session Broker).</span></span> <span data-ttu-id="c48f8-179">Implemente esta interfaz cuando desee proporcionar un complemento que invalide la lógica de redirección del agente de sesiones de TS.</span><span class="sxs-lookup"><span data-stu-id="c48f8-179">Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS Session Broker.</span></span>

</dd> </dl>

 

 