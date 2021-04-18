---
description: Es el elemento raíz que identifica un perfil de banda ancha móvil.
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: Elemento MBNProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 7016d492a70192a7d6accdcb3aaa57a9c564960e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715256"
---
# <a name="mbnprofile-element"></a><span data-ttu-id="12913-103">Elemento MBNProfile</span><span class="sxs-lookup"><span data-stu-id="12913-103">MBNProfile Element</span></span>

<span data-ttu-id="12913-104">El elemento **MBNProfile** es el elemento raíz que identifica un perfil de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="12913-104">The **MBNProfile** element is the root element that identifies a Mobile Broadband profile.</span></span>

<span data-ttu-id="12913-105">Solo puede haber un elemento de este tipo por documento.</span><span class="sxs-lookup"><span data-stu-id="12913-105">There can only be one element of this type per document.</span></span>

``` syntax
<xs:element name="MBNProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="nameType"
             />
            <xs:element name="Description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="ICONFilePath"
                type="iconFileType"
                minOccurs="0"
             />
            <xs:element name="IsDefault"
                type="boolean"
             />
            <xs:element name="ProfileCreationType"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="token"
                    >
                        <xs:enumeration
                            value="UserProvisioned"
                         />
                        <xs:enumeration
                            value="AdminProvisioned"
                         />
                        <xs:enumeration
                            value="OperatorProvisioned"
                         />
                        <xs:enumeration
                            value="DeviceProvisioned"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="SubscriberID"
                type="subscriberIdType"
             />
            <xs:element name="SimIccID"
                type="simIccIDType"
                minOccurs="0"
             />
            <xs:element name="HomeProviderName"
                type="providerNameType"
                minOccurs="0"
             />
            <xs:element name="AutoConnectOnInternet"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="ConnectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="manual"
                         />
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="auto-home"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="Context"
                type="contextType"
                minOccurs="0"
             />
            <xs:element name="DataRoamingPartners"
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
```

## <a name="child-elements"></a><span data-ttu-id="12913-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="12913-106">Child elements</span></span>



| <span data-ttu-id="12913-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="12913-107">Element</span></span>                                                                          | <span data-ttu-id="12913-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="12913-108">Type</span></span>                                                           | <span data-ttu-id="12913-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="12913-109">Description</span></span>                                               |
|----------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="12913-110">**AutoConnectOnInternet**</span><span class="sxs-lookup"><span data-stu-id="12913-110">**AutoConnectOnInternet**</span></span>](schema-autoconnectoninternet-mbnprofile-element.md) | <span data-ttu-id="12913-111">boolean</span><span class="sxs-lookup"><span data-stu-id="12913-111">boolean</span></span>                                                        | <span data-ttu-id="12913-112">Si el dispositivo se conectará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="12913-112">Whether the device will automatically connect.</span></span><br/> |
| [<span data-ttu-id="12913-113">**ConnectionMode**</span><span class="sxs-lookup"><span data-stu-id="12913-113">**ConnectionMode**</span></span>](schema-connectionmode-mbnprofile-element.md)               |                                                                | <span data-ttu-id="12913-114">La configuración de conexión automática del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12913-114">The device auto connection settings.</span></span><br/>           |
| [<span data-ttu-id="12913-115">**Context**</span><span class="sxs-lookup"><span data-stu-id="12913-115">**Context**</span></span>](schema-context-mbnprofile-element.md)                             | [<span data-ttu-id="12913-116">**contextType**</span><span class="sxs-lookup"><span data-stu-id="12913-116">**contextType**</span></span>](schema-contexttype-complextype.md)          | <span data-ttu-id="12913-117">Parámetros de configuración de la conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="12913-117">Data connection setup parameters.</span></span><br/>              |
| [<span data-ttu-id="12913-118">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="12913-118">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | <span data-ttu-id="12913-119">Proveedores de red preferidos para itinerancia.</span><span class="sxs-lookup"><span data-stu-id="12913-119">Preferred network providers for roaming.</span></span><br/>       |
| [<span data-ttu-id="12913-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="12913-120">**Description**</span></span>](schema-description-mbnprofile-element.md)                     | [<span data-ttu-id="12913-121">**nameType**</span><span class="sxs-lookup"><span data-stu-id="12913-121">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="12913-122">Descripción del perfil.</span><span class="sxs-lookup"><span data-stu-id="12913-122">Description of the profile.</span></span><br/>                    |
| [<span data-ttu-id="12913-123">**HomeProviderName**</span><span class="sxs-lookup"><span data-stu-id="12913-123">**HomeProviderName**</span></span>](schema-homeprovidername-mbnprofile-element.md)           | [<span data-ttu-id="12913-124">**providerNameType**</span><span class="sxs-lookup"><span data-stu-id="12913-124">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="12913-125">Nombre del proveedor de inicio.</span><span class="sxs-lookup"><span data-stu-id="12913-125">Name of the home provider.</span></span><br/>                     |
| [<span data-ttu-id="12913-126">**ICONFilePath**</span><span class="sxs-lookup"><span data-stu-id="12913-126">**ICONFilePath**</span></span>](schema-iconfilepath-mbnprofile-element.md)                   | [<span data-ttu-id="12913-127">**iconFileType**</span><span class="sxs-lookup"><span data-stu-id="12913-127">**iconFileType**</span></span>](schema-iconfiletype-simpletype.md)         | <span data-ttu-id="12913-128">Ruta de acceso al archivo de icono.</span><span class="sxs-lookup"><span data-stu-id="12913-128">Path to the icon file.</span></span><br/>                         |
| [<span data-ttu-id="12913-129">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="12913-129">**IsDefault**</span></span>](schema-isdefault-mbnprofile-element.md)                         | <span data-ttu-id="12913-130">boolean</span><span class="sxs-lookup"><span data-stu-id="12913-130">boolean</span></span>                                                        | <span data-ttu-id="12913-131">Indica si el perfil es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="12913-131">Whether the profile is the default.</span></span><br/>            |
| [<span data-ttu-id="12913-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="12913-132">**Name**</span></span>](schema-name-mbnprofile-element.md)                                   | [<span data-ttu-id="12913-133">**nameType**</span><span class="sxs-lookup"><span data-stu-id="12913-133">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="12913-134">Nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="12913-134">Name of the profile.</span></span><br/>                           |
| [<span data-ttu-id="12913-135">**ProfileCreationType**</span><span class="sxs-lookup"><span data-stu-id="12913-135">**ProfileCreationType**</span></span>](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | <span data-ttu-id="12913-136">Información sobre el creador del perfil.</span><span class="sxs-lookup"><span data-stu-id="12913-136">Information about the profile creator.</span></span><br/>         |
| [<span data-ttu-id="12913-137">**SimIccID**</span><span class="sxs-lookup"><span data-stu-id="12913-137">**SimIccID**</span></span>](schema-simiccid-mbnprofile-element.md)                           | [<span data-ttu-id="12913-138">**simIccIDType**</span><span class="sxs-lookup"><span data-stu-id="12913-138">**simIccIDType**</span></span>](schema-simiccidtype-simpletype.md)         | <span data-ttu-id="12913-139">Número de identificación de SIM para dispositivos GSM.</span><span class="sxs-lookup"><span data-stu-id="12913-139">SIM identification number for GSM devices.</span></span><br/>     |
| [<span data-ttu-id="12913-140">**SubscriberID**</span><span class="sxs-lookup"><span data-stu-id="12913-140">**SubscriberID**</span></span>](schema-subscriberid-mbnprofile-element.md)                   | [<span data-ttu-id="12913-141">**subscriberIdType**</span><span class="sxs-lookup"><span data-stu-id="12913-141">**subscriberIdType**</span></span>](schema-subscriberidtype-simpletype.md) | <span data-ttu-id="12913-142">Identificador único del perfil.</span><span class="sxs-lookup"><span data-stu-id="12913-142">Unique identifier of the profile.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="12913-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12913-143">Requirements</span></span>



| <span data-ttu-id="12913-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="12913-144">Requirement</span></span> | <span data-ttu-id="12913-145">Value</span><span class="sxs-lookup"><span data-stu-id="12913-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="12913-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12913-146">Minimum supported client</span></span><br/> | <span data-ttu-id="12913-147">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="12913-147">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="12913-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12913-148">Minimum supported server</span></span><br/> | <span data-ttu-id="12913-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="12913-149">None supported</span></span><br/>                         |



 

 




