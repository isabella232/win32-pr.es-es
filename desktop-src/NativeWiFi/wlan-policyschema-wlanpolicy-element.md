---
description: Contiene una directiva de LAN inalámbrica.
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: Elemento WLANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ec26a3cab15014deabca4e9332c1fbef7a788b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155280"
---
# <a name="wlanpolicy-element"></a><span data-ttu-id="7f51c-103">Elemento WLANPolicy</span><span class="sxs-lookup"><span data-stu-id="7f51c-103">WLANPolicy Element</span></span>

<span data-ttu-id="7f51c-104">El elemento **WLANPolicy** contiene una directiva de LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="7f51c-104">The **WLANPolicy** element contains a wireless LAN policy.</span></span> <span data-ttu-id="7f51c-105">Este elemento es el elemento raíz único para un perfil de directiva inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="7f51c-105">This element is the unique root element for a wireless policy profile.</span></span>

<span data-ttu-id="7f51c-106">El espacio de nombres de destino para el elemento **WLANPolicy** es `https://www.microsoft.com/networking/WLAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="7f51c-106">The target namespace for the **WLANPolicy** element is `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

``` syntax
<xs:element name="WLANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:element name="showDeniedNetwork"
                            type="boolean"
                         />
                        <xs:element name="allowEveryoneToCreateAllUserProfiles"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="networkFilter"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="allowList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="blockList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="denyAllIBSS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:element name="denyAllESS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="7f51c-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7f51c-107">Child elements</span></span>



| <span data-ttu-id="7f51c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="7f51c-108">Element</span></span>                                                                                                                    | <span data-ttu-id="7f51c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7f51c-109">Type</span></span>                                                                     | <span data-ttu-id="7f51c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f51c-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f51c-111">**allowEveryoneToCreateAllUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="7f51c-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="7f51c-112">boolean</span><span class="sxs-lookup"><span data-stu-id="7f51c-112">boolean</span></span>                                                                  | <span data-ttu-id="7f51c-113">Especifica si un usuario puede crear un perfil de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="7f51c-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="7f51c-114">**Permitidos**</span><span class="sxs-lookup"><span data-stu-id="7f51c-114">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="7f51c-115">La lista de redes LAN inalámbricas a las que se debe permitir que se conecte cualquier equipo.</span><span class="sxs-lookup"><span data-stu-id="7f51c-115">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/>                                       |
| [<span data-ttu-id="7f51c-116">**Bloqueo**</span><span class="sxs-lookup"><span data-stu-id="7f51c-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="7f51c-117">La lista de redes LAN inalámbricas a las que una máquina no debe conectarse.</span><span class="sxs-lookup"><span data-stu-id="7f51c-117">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>                                                    |
| [<span data-ttu-id="7f51c-118">**denyAllESS**</span><span class="sxs-lookup"><span data-stu-id="7f51c-118">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | <span data-ttu-id="7f51c-119">boolean</span><span class="sxs-lookup"><span data-stu-id="7f51c-119">boolean</span></span>                                                                  | <span data-ttu-id="7f51c-120">Especifica si el acceso a todas las redes de infraestructura está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="7f51c-120">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                                                           |
| [<span data-ttu-id="7f51c-121">**denyAllIBSS**</span><span class="sxs-lookup"><span data-stu-id="7f51c-121">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | <span data-ttu-id="7f51c-122">boolean</span><span class="sxs-lookup"><span data-stu-id="7f51c-122">boolean</span></span>                                                                  | <span data-ttu-id="7f51c-123">Especifica si el acceso a todas las redes ad hoc está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="7f51c-123">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                                                                   |
| [<span data-ttu-id="7f51c-124">**denominación**</span><span class="sxs-lookup"><span data-stu-id="7f51c-124">**description**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [<span data-ttu-id="7f51c-125">**nameType**</span><span class="sxs-lookup"><span data-stu-id="7f51c-125">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="7f51c-126">La descripción de una directiva de LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="7f51c-126">The description of a wireless LAN policy.</span></span> <br/>                                                                                |
| [<span data-ttu-id="7f51c-127">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="7f51c-127">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="7f51c-128">boolean</span><span class="sxs-lookup"><span data-stu-id="7f51c-128">boolean</span></span>                                                                  | <span data-ttu-id="7f51c-129">Especifica si los equipos usan el servicio de configuración automática (AutoConfig) integrado para administrar las conexiones inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="7f51c-129">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="7f51c-130">**Indicadores**</span><span class="sxs-lookup"><span data-stu-id="7f51c-130">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="7f51c-131">Contiene la configuración global del módulo de configuración automática (ACM).</span><span class="sxs-lookup"><span data-stu-id="7f51c-131">Contains the global settings for the Auto Configuration Module (ACM).</span></span> <br/>                                                    |
| [<span data-ttu-id="7f51c-132">**name**</span><span class="sxs-lookup"><span data-stu-id="7f51c-132">**name**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [<span data-ttu-id="7f51c-133">**nameType**</span><span class="sxs-lookup"><span data-stu-id="7f51c-133">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="7f51c-134">El nombre de una directiva de LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="7f51c-134">The name of a wireless LAN policy.</span></span> <br/>                                                                                       |
| [<span data-ttu-id="7f51c-135">**Storage**</span><span class="sxs-lookup"><span data-stu-id="7f51c-135">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)                                                             | [<span data-ttu-id="7f51c-136">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="7f51c-136">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="7f51c-137">Una red permitida.</span><span class="sxs-lookup"><span data-stu-id="7f51c-137">An allowed network.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="7f51c-138">**Storage**</span><span class="sxs-lookup"><span data-stu-id="7f51c-138">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)                                                             | [<span data-ttu-id="7f51c-139">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="7f51c-139">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="7f51c-140">Una red bloqueada.</span><span class="sxs-lookup"><span data-stu-id="7f51c-140">A blocked network.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="7f51c-141">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="7f51c-141">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | <span data-ttu-id="7f51c-142">La lista de redes permitidas y denegadas.</span><span class="sxs-lookup"><span data-stu-id="7f51c-142">The list of allowed and denied networks.</span></span><br/>                                                                                  |
| [<span data-ttu-id="7f51c-143">**profileList**</span><span class="sxs-lookup"><span data-stu-id="7f51c-143">**profileList**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="7f51c-144">Contiene una lista de perfiles que se van a aplicar en el nivel de dominio o de equipo.</span><span class="sxs-lookup"><span data-stu-id="7f51c-144">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                |
| [<span data-ttu-id="7f51c-145">**showDeniedNetwork**</span><span class="sxs-lookup"><span data-stu-id="7f51c-145">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="7f51c-146">boolean</span><span class="sxs-lookup"><span data-stu-id="7f51c-146">boolean</span></span>                                                                  | <span data-ttu-id="7f51c-147">Especifica si las redes denegadas aparecen en el Asistente para **conectarse a una red** .</span><span class="sxs-lookup"><span data-stu-id="7f51c-147">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="remarks"></a><span data-ttu-id="7f51c-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f51c-148">Remarks</span></span>

<span data-ttu-id="7f51c-149">Para ver la lista de elementos secundarios en una estructura similar a un árbol, [vea \_ elementos de esquema de directiva de WLAN](wlan-policyschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="7f51c-149">To view the list of child elements in a tree-like structure, see [WLAN\_policy Schema Elements](wlan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f51c-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f51c-150">Requirements</span></span>



| <span data-ttu-id="7f51c-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f51c-151">Requirement</span></span> | <span data-ttu-id="7f51c-152">Value</span><span class="sxs-lookup"><span data-stu-id="7f51c-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7f51c-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f51c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="7f51c-154">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7f51c-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7f51c-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f51c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="7f51c-156">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f51c-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




