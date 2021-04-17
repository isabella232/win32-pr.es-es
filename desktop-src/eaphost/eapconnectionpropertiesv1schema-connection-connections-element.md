---
title: Connection (conexiones) (elemento)
description: Define cada valor de configuración y lo asocia a un nombre. El elemento de conexión es opcional.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Elemento de conexión EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714599"
---
# <a name="connection-connections-element"></a><span data-ttu-id="f526f-105">Connection (conexiones) (elemento)</span><span class="sxs-lookup"><span data-stu-id="f526f-105">Connection (Connections) Element</span></span>

<span data-ttu-id="f526f-106">El elemento de **conexión (conexiones)** define cada opción de configuración y la asocia a un nombre.</span><span class="sxs-lookup"><span data-stu-id="f526f-106">The **Connection (Connections)** element defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="f526f-107">El elemento de **conexión** es opcional.</span><span class="sxs-lookup"><span data-stu-id="f526f-107">The **Connection** element is optional.</span></span>

``` syntax
<xs:element name="Connection">
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
```

<span data-ttu-id="f526f-108">El elemento de **conexión** se define mediante [**el elemento**](eapconnectionpropertiesv1schema-connections-element.md) Connections.</span><span class="sxs-lookup"><span data-stu-id="f526f-108">The **Connection** element is defined by the [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f526f-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f526f-109">Child elements</span></span>



| <span data-ttu-id="f526f-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f526f-110">Element</span></span>                                                                 | <span data-ttu-id="f526f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="f526f-111">Type</span></span>   | <span data-ttu-id="f526f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f526f-112">Description</span></span>                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f526f-113">**Participante**</span><span class="sxs-lookup"><span data-stu-id="f526f-113">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | <span data-ttu-id="f526f-114">Identifica el elemento de configuración de EAP.</span><span class="sxs-lookup"><span data-stu-id="f526f-114">Identifies the EAP configuration element.</span></span><br/>                                                                    |
| [<span data-ttu-id="f526f-115">**Name**</span><span class="sxs-lookup"><span data-stu-id="f526f-115">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md) | <span data-ttu-id="f526f-116">string</span><span class="sxs-lookup"><span data-stu-id="f526f-116">string</span></span> | <span data-ttu-id="f526f-117">Captura el nombre de la conexión que se está definiendo y ayuda en la identificación de varias conexiones.</span><span class="sxs-lookup"><span data-stu-id="f526f-117">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="f526f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f526f-118">Requirements</span></span>



| <span data-ttu-id="f526f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f526f-119">Requirement</span></span> | <span data-ttu-id="f526f-120">Value</span><span class="sxs-lookup"><span data-stu-id="f526f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f526f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f526f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f526f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f526f-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f526f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f526f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f526f-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f526f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f526f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f526f-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f526f-126">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="f526f-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f526f-127">**Conexiones**</span><span class="sxs-lookup"><span data-stu-id="f526f-127">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

<span data-ttu-id="f526f-128">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="f526f-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f526f-129">**Conexiones**</span><span class="sxs-lookup"><span data-stu-id="f526f-129">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[<span data-ttu-id="f526f-130">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="f526f-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f526f-131">Esquema eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f526f-131">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





