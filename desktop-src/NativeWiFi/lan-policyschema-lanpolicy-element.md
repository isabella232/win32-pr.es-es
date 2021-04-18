---
description: Contiene una directiva de LAN cableada.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: Elemento LANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b424a47405aa8f32276019a85902bd51b173cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687930"
---
# <a name="lanpolicy-element"></a><span data-ttu-id="19ed5-103">Elemento LANPolicy</span><span class="sxs-lookup"><span data-stu-id="19ed5-103">LANPolicy Element</span></span>

<span data-ttu-id="19ed5-104">El elemento LANPolicy contiene una directiva de LAN cableada.</span><span class="sxs-lookup"><span data-stu-id="19ed5-104">The LANPolicy element contains a wired LAN policy.</span></span> <span data-ttu-id="19ed5-105">Este elemento es el elemento raíz único para un perfil de directiva de red cableada.</span><span class="sxs-lookup"><span data-stu-id="19ed5-105">This element is the unique root element for a wired network policy profile.</span></span>

<span data-ttu-id="19ed5-106">El espacio de nombres de destino para el elemento **LANPolicy** es `https://www.microsoft.com/networking/LAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="19ed5-106">The target namespace for the **LANPolicy** element is `https://www.microsoft.com/networking/LAN/policy/v1`.</span></span>

``` syntax
<xs:element name="LANPolicy">
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

## <a name="child-elements"></a><span data-ttu-id="19ed5-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="19ed5-107">Child elements</span></span>



| <span data-ttu-id="19ed5-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="19ed5-108">Element</span></span>                                                                           | <span data-ttu-id="19ed5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="19ed5-109">Type</span></span>                                                     | <span data-ttu-id="19ed5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="19ed5-110">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19ed5-111">**denominación**</span><span class="sxs-lookup"><span data-stu-id="19ed5-111">**description**</span></span>](lan-policyschema-description-lanpolicy-element.md)             | [<span data-ttu-id="19ed5-112">**nameType**</span><span class="sxs-lookup"><span data-stu-id="19ed5-112">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="19ed5-113">Contiene la descripción de una directiva de LAN cableada.</span><span class="sxs-lookup"><span data-stu-id="19ed5-113">Contains the description of a wired LAN policy.</span></span> <br/>                                                                                                                          |
| [<span data-ttu-id="19ed5-114">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="19ed5-114">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="19ed5-115">boolean</span><span class="sxs-lookup"><span data-stu-id="19ed5-115">boolean</span></span>                                                  | <span data-ttu-id="19ed5-116">Especifica si los equipos usan el servicio de configuración automática integrado para administrar las conexiones a redes cableadas que requieren autenticación de nivel 2 (por ejemplo, 802.1 X).</span><span class="sxs-lookup"><span data-stu-id="19ed5-116">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |
| [<span data-ttu-id="19ed5-117">**Indicadores**</span><span class="sxs-lookup"><span data-stu-id="19ed5-117">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | <span data-ttu-id="19ed5-118">Contiene la configuración global para la configuración automática de redes cableadas.</span><span class="sxs-lookup"><span data-stu-id="19ed5-118">Contains the global settings for the automatic configuration of wired networks.</span></span> <br/>                                                                                          |
| [<span data-ttu-id="19ed5-119">**name**</span><span class="sxs-lookup"><span data-stu-id="19ed5-119">**name**</span></span>](lan-policyschema-name-lanpolicy-element.md)                           | [<span data-ttu-id="19ed5-120">**nameType**</span><span class="sxs-lookup"><span data-stu-id="19ed5-120">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="19ed5-121">Contiene el nombre de una directiva de LAN cableada.</span><span class="sxs-lookup"><span data-stu-id="19ed5-121">Contains the name of a wired LAN policy.</span></span> <br/>                                                                                                                                 |
| [<span data-ttu-id="19ed5-122">**profileList**</span><span class="sxs-lookup"><span data-stu-id="19ed5-122">**profileList**</span></span>](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | <span data-ttu-id="19ed5-123">Contiene una lista de perfiles que se van a aplicar en el nivel de dominio o de equipo.</span><span class="sxs-lookup"><span data-stu-id="19ed5-123">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                                                                |



## <a name="remarks"></a><span data-ttu-id="19ed5-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19ed5-124">Remarks</span></span>

<span data-ttu-id="19ed5-125">Para ver la lista de elementos secundarios en una estructura similar a un árbol, [vea \_ elementos de esquema de directiva de LAN](lan-policyschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="19ed5-125">To view the list of child elements in a tree-like structure, see [LAN\_policy Schema Elements](lan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19ed5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19ed5-126">Requirements</span></span>



| <span data-ttu-id="19ed5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="19ed5-127">Requirement</span></span> | <span data-ttu-id="19ed5-128">Value</span><span class="sxs-lookup"><span data-stu-id="19ed5-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19ed5-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19ed5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="19ed5-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="19ed5-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="19ed5-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19ed5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="19ed5-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="19ed5-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




