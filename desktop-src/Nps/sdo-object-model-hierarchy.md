---
title: Jerarquía del modelo de objetos
description: Los objetos del modelo de objetos SDO están organizados en una jerarquía. Esto significa que los objetos de SDO proporcionan acceso a otros objetos en SDO.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2484b4d7402f8a5b43a590651f36d4d1707bca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420994"
---
# <a name="object-model-hierarchy"></a><span data-ttu-id="f812e-104">Jerarquía del modelo de objetos</span><span class="sxs-lookup"><span data-stu-id="f812e-104">Object Model Hierarchy</span></span>

<span data-ttu-id="f812e-105">Los objetos del modelo de objetos SDO están organizados en una jerarquía.</span><span class="sxs-lookup"><span data-stu-id="f812e-105">The objects in the SDO object model are arranged in a hierarchy.</span></span> <span data-ttu-id="f812e-106">Esto significa que los objetos de SDO proporcionan acceso a otros objetos en SDO.</span><span class="sxs-lookup"><span data-stu-id="f812e-106">This means objects in SDO provide access to other objects in SDO.</span></span>

<span data-ttu-id="f812e-107">Los objetos proporcionan acceso a otros objetos de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="f812e-107">Objects provide access to other objects in two ways.</span></span> <span data-ttu-id="f812e-108">Una manera es que el objeto exponga una interfaz que proporciona métodos para recuperar otros objetos.</span><span class="sxs-lookup"><span data-stu-id="f812e-108">One way is for the object to expose an interface that provides methods to retrieve other objects.</span></span> <span data-ttu-id="f812e-109">Un ejemplo de este enfoque es el objeto de equipo.</span><span class="sxs-lookup"><span data-stu-id="f812e-109">An example of this approach is the Machine object.</span></span> <span data-ttu-id="f812e-110">El objeto de equipo expone la interfaz [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) .</span><span class="sxs-lookup"><span data-stu-id="f812e-110">The Machine object exposes the [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) interface.</span></span> <span data-ttu-id="f812e-111">El método [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) recupera un objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="f812e-111">The [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) method retrieves a Service object.</span></span> <span data-ttu-id="f812e-112">El método [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) recupera un objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="f812e-112">The [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) method retrieves a User Object.</span></span>

![objeto de equipo que expone la interfaz isdomachine](images/sdo01.png)

<span data-ttu-id="f812e-114">Para obtener más información, vea [obtener el servicio y el usuario SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span><span class="sxs-lookup"><span data-stu-id="f812e-114">For more information, see [Obtaining Service and User SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span></span>

<span data-ttu-id="f812e-115">La segunda manera en que los objetos proporcionan acceso a otros objetos es que una colección de objetos se representa como una propiedad del objeto que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="f812e-115">The second way that objects provide access to other objects is that an object collection is represented as a property of the object that contains it.</span></span> <span data-ttu-id="f812e-116">Para recuperar una colección de objetos, llame a [**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) en la propiedad de un objeto que representa la colección.</span><span class="sxs-lookup"><span data-stu-id="f812e-116">To retrieve an object collection, call [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) on the property of an object that represents the collection.</span></span> <span data-ttu-id="f812e-117">Por ejemplo, para recuperar la colección de directivas, llame a **ISdo:: GetProperty** en la interfaz [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) expuesta por el objeto NPS.</span><span class="sxs-lookup"><span data-stu-id="f812e-117">For example, to retrieve the Policies collection, call **ISdo::GetProperty** on the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface exposed by the NPS object.</span></span>

> [!Note]  
> <span data-ttu-id="f812e-118">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f812e-118">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

![recuperación de la colección de directivas](images/sdo02.png)

<span data-ttu-id="f812e-120">Para obtener el código de ejemplo que recupera la colección de directivas, consulte [recuperar una colección](/windows/desktop/Nps/sdo-retrieving-a-collection).</span><span class="sxs-lookup"><span data-stu-id="f812e-120">For sample code that retrieves the Policies collection, see [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection).</span></span>

<span data-ttu-id="f812e-121">El [**objeto de datos del servidor NPS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) tiene las siguientes propiedades que representan colecciones:</span><span class="sxs-lookup"><span data-stu-id="f812e-121">The [**NPS Server Data Object**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) has the following properties that represent collections:</span></span>

<dl> <dt>

<span data-ttu-id="f812e-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auditores</span><span class="sxs-lookup"><span data-stu-id="f812e-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auditors</span></span>
</dt> <dd>

<span data-ttu-id="f812e-123">El único Auditor de la colección de auditores es el [**registro de eventos de NT**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span><span class="sxs-lookup"><span data-stu-id="f812e-123">The only auditor in the Auditors collection is the [**NT Event Log**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span></span>

</dd> <dt>

<span data-ttu-id="f812e-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Políticas</span><span class="sxs-lookup"><span data-stu-id="f812e-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Policies</span></span>
</dt> <dd>

<span data-ttu-id="f812e-125">Cada [**objeto de directiva**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) tiene una propiedad que representa una colección de condiciones.</span><span class="sxs-lookup"><span data-stu-id="f812e-125">Each [**policy object**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) has a property that represents a collection of conditions.</span></span>

</dd> <dt>

<span data-ttu-id="f812e-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>File</span><span class="sxs-lookup"><span data-stu-id="f812e-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profiles</span></span>
</dt> <dd>

<span data-ttu-id="f812e-127">Cada [**objeto de perfil**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) de las colecciones de perfiles tiene una propiedad que representa una colección de atributos.</span><span class="sxs-lookup"><span data-stu-id="f812e-127">Each [**profile object**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) in the Profiles collections has a property that represents an attributes collection.</span></span> <span data-ttu-id="f812e-128">Vea [atributos compatibles con SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes) para obtener una lista de los atributos admitidos por SDO.</span><span class="sxs-lookup"><span data-stu-id="f812e-128">See [SDO Supported Attributes](/windows/desktop/Nps/sdo-sdo-supported-attributes) for a list of the attributes supported by SDO.</span></span>

</dd> <dt>

<span data-ttu-id="f812e-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocolos</span><span class="sxs-lookup"><span data-stu-id="f812e-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocols</span></span>
</dt> <dd>

<span data-ttu-id="f812e-130">La colección Protocols contiene el objeto de protocolo RADIUS, que contiene una colección de clientes que representa clientes RADIUS.</span><span class="sxs-lookup"><span data-stu-id="f812e-130">The protocols collection contains the RADIUS protocol object, which contains a clients collection that represents RADIUS clients.</span></span> <span data-ttu-id="f812e-131">Consulte [Agregar un cliente](/windows/desktop/Nps/sdo-adding-a-client) para ver el código de ejemplo que muestra cómo recuperar la colección de clientes.</span><span class="sxs-lookup"><span data-stu-id="f812e-131">See [Adding a Client](/windows/desktop/Nps/sdo-adding-a-client) for sample code that shows how to retrieve the client collection.</span></span>

</dd> <dt>

<span data-ttu-id="f812e-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Directivas de proxy</span><span class="sxs-lookup"><span data-stu-id="f812e-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Proxy Policies</span></span>
</dt> <dd>

<span data-ttu-id="f812e-133">Esta colección contiene las directivas de acceso a redes utilizadas para el procesamiento de solicitudes de conexión.</span><span class="sxs-lookup"><span data-stu-id="f812e-133">This collection contains Network Access Policies used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="f812e-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Perfiles de proxy</span><span class="sxs-lookup"><span data-stu-id="f812e-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Proxy Profiles</span></span>
</dt> <dd>

<span data-ttu-id="f812e-135">Esta colección contiene perfiles usados para el procesamiento de solicitudes de conexión.</span><span class="sxs-lookup"><span data-stu-id="f812e-135">This collection contains profiles used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="f812e-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>Grupos de servidores RADIUS</span><span class="sxs-lookup"><span data-stu-id="f812e-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>RADIUS Server Groups</span></span>
</dt> <dd>

<span data-ttu-id="f812e-137">Cada [**grupo de servidores RADIUS**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) de la colección de grupos de servidores RADIUS tiene una propiedad que representa la colección de servidores de ese grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="f812e-137">Each [**RADIUS server group**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) in the RADIUS Server Groups collection has a property that represents the collection of servers in that server group.</span></span>

</dd> <dt>

<span data-ttu-id="f812e-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Controladores de solicitud</span><span class="sxs-lookup"><span data-stu-id="f812e-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Request Handlers</span></span>
</dt> <dd>

<span data-ttu-id="f812e-139">Esta colección contiene la colección "Microsoft Realms Evaluator".</span><span class="sxs-lookup"><span data-stu-id="f812e-139">This collection contains the "Microsoft Realms Evaluator" collection.</span></span> <span data-ttu-id="f812e-140">La configuración de "autenticación de Microsoft NT SAM" y "cuentas de Microsoft" también está disponible en esta colección.</span><span class="sxs-lookup"><span data-stu-id="f812e-140">The "Microsoft NT SAM Authentication" and "Microsoft Accounting" settings are also available in this collection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f812e-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f812e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f812e-142">Objetos SDO y propiedades</span><span class="sxs-lookup"><span data-stu-id="f812e-142">SDO Objects and Properties</span></span>](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[<span data-ttu-id="f812e-143">Atributos compatibles con SDO</span><span class="sxs-lookup"><span data-stu-id="f812e-143">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 