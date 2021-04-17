---
title: Elemento Connections
description: Obtenga información sobre el elemento Connections. Este elemento recopila y contiene cero o más elementos de conexión.
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Elemento Connections EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cdb23c9f1a6130e2fe77061286e8a0657c3e2f5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714450"
---
# <a name="connections-element"></a><span data-ttu-id="04b63-105">Elemento Connections</span><span class="sxs-lookup"><span data-stu-id="04b63-105">Connections Element</span></span>

<span data-ttu-id="04b63-106">El elemento **Connections** recopila y contiene cero o más elementos de [**conexión**](eapconnectionpropertiesv1schema-connection-connections-element.md) .</span><span class="sxs-lookup"><span data-stu-id="04b63-106">The **Connections** element collects and contains zero or more [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) elements.</span></span>

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Name"
                            type="string"
                         />
                        <xs:element
                            maxOccurs="unbounded"
                            ref="Eap"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="04b63-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="04b63-107">Child elements</span></span>



| <span data-ttu-id="04b63-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="04b63-108">Element</span></span>                                                                              | <span data-ttu-id="04b63-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="04b63-109">Type</span></span>   | <span data-ttu-id="04b63-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="04b63-110">Description</span></span>                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04b63-111">**Participante**</span><span class="sxs-lookup"><span data-stu-id="04b63-111">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | <span data-ttu-id="04b63-112">Identifica el elemento de configuración de EAP.</span><span class="sxs-lookup"><span data-stu-id="04b63-112">Identifies the EAP configuration element.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="04b63-113">**Conectarse**</span><span class="sxs-lookup"><span data-stu-id="04b63-113">**Connection**</span></span>](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | <span data-ttu-id="04b63-114">Define cada valor de configuración y lo asocia a un nombre.</span><span class="sxs-lookup"><span data-stu-id="04b63-114">Defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="04b63-115">El elemento de [**conexión**](eapconnectionpropertiesv1schema-connection-connections-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="04b63-115">The [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="04b63-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="04b63-116">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md)              | <span data-ttu-id="04b63-117">string</span><span class="sxs-lookup"><span data-stu-id="04b63-117">string</span></span> | <span data-ttu-id="04b63-118">Captura el nombre de la conexión que se está definiendo y ayuda en la identificación de varias conexiones.</span><span class="sxs-lookup"><span data-stu-id="04b63-118">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span><br/>                                                                     |



## <a name="remarks"></a><span data-ttu-id="04b63-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04b63-119">Remarks</span></span>

<span data-ttu-id="04b63-120">El elemento **Connections** no se utiliza con métodos heredados a través de las API de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="04b63-120">The **Connections** element is not used with legacy methods via the EAPHost APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b63-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04b63-121">Requirements</span></span>



| <span data-ttu-id="04b63-122">Role</span><span class="sxs-lookup"><span data-stu-id="04b63-122">Role</span></span> | <span data-ttu-id="04b63-123">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="04b63-123">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="04b63-124">Remoto</span><span class="sxs-lookup"><span data-stu-id="04b63-124">Client</span></span><br/> | <span data-ttu-id="04b63-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="04b63-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="04b63-126">Servidor</span><span class="sxs-lookup"><span data-stu-id="04b63-126">Server</span></span><br/> | <span data-ttu-id="04b63-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="04b63-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="04b63-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="04b63-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b63-129">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="04b63-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="04b63-130">Esquema eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="04b63-130">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





