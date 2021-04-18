---
description: Especifica la configuración de EAPHost.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Elemento EAPConfig (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 955b3647aca787097495b6051407b718dfa91f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667142"
---
# <a name="eapconfig-onex-element"></a><span data-ttu-id="62712-103">Elemento EAPConfig (OneX)</span><span class="sxs-lookup"><span data-stu-id="62712-103">EAPConfig (OneX) Element</span></span>

<span data-ttu-id="62712-104">El elemento **EAPConfig** (Onex) especifica la configuración de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="62712-104">The **EAPConfig** (OneX) element specifies the EAPHost configuration.</span></span>

<span data-ttu-id="62712-105">A diferencia de la mayoría de los elementos del esquema de perfil 802.1 X, este elemento se encuentra en el `https://www.microsoft.com/provisioning/EapHostConfig` espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="62712-105">Unlike most elements in the 802.1X profile schema, this element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span> <span data-ttu-id="62712-106">Sus elementos secundarios se definen en el [esquema eaphostconfig](../eaphost/eaphostconfigschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="62712-106">Its child elements are defined in the [eaphostconfig schema](../eaphost/eaphostconfigschema-schema.md).</span></span> <span data-ttu-id="62712-107">El elemento [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) es un elemento secundario del elemento **EAPConfig** .</span><span class="sxs-lookup"><span data-stu-id="62712-107">The [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) element is a child of the **EAPConfig** element.</span></span>

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="62712-108">El elemento **EAPConfig** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="62712-108">The **EAPConfig** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="62712-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62712-109">Requirements</span></span>



| <span data-ttu-id="62712-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="62712-110">Requirement</span></span> | <span data-ttu-id="62712-111">Value</span><span class="sxs-lookup"><span data-stu-id="62712-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="62712-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62712-112">Minimum supported client</span></span><br/> | <span data-ttu-id="62712-113">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="62712-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="62712-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62712-114">Minimum supported server</span></span><br/> | <span data-ttu-id="62712-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="62712-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="62712-116">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="62712-116">Redistributable</span></span><br/>          | <span data-ttu-id="62712-117">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="62712-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="62712-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="62712-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="62712-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="62712-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="62712-120">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="62712-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="62712-121">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="62712-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="62712-122">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="62712-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
