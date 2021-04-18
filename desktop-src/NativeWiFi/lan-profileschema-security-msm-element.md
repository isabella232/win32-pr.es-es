---
description: Contiene la configuración de seguridad para redes cableadas.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Elemento Security (MSM) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2bd052679f207cd0778f212a73663d4dfd8ce165
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105678857"
---
# <a name="security-msm-element-lan_policy"></a><span data-ttu-id="ff4c5-103">Elemento Security (MSM) (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="ff4c5-103">Security (MSM) Element (LAN_policy)</span></span>

<span data-ttu-id="ff4c5-104">El elemento de seguridad (MSM) contiene la configuración de seguridad de las redes cableadas.</span><span class="sxs-lookup"><span data-stu-id="ff4c5-104">The security (MSM) element contains security settings for wired networks.</span></span> <span data-ttu-id="ff4c5-105">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="ff4c5-105">This element is optional.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OneXEnforced"
                type="boolean"
             />
            <xs:element name="OneXEnabled"
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
```

<span data-ttu-id="ff4c5-106">El elemento de **seguridad** se define mediante el elemento [**MSM**](lan-profileschema-msm-lanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ff4c5-106">The **security** element is defined by the [**MSM**](lan-profileschema-msm-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ff4c5-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ff4c5-107">Child elements</span></span>



| <span data-ttu-id="ff4c5-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ff4c5-108">Element</span></span>                                                                 | <span data-ttu-id="ff4c5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff4c5-109">Type</span></span>    | <span data-ttu-id="ff4c5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff4c5-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff4c5-111">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="ff4c5-111">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="ff4c5-112">boolean</span><span class="sxs-lookup"><span data-stu-id="ff4c5-112">boolean</span></span> | <span data-ttu-id="ff4c5-113">Especifica si el servicio de configuración automática de redes cableadas intentará la autenticación del puerto mediante 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="ff4c5-113">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="ff4c5-114">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="ff4c5-114">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="ff4c5-115">boolean</span><span class="sxs-lookup"><span data-stu-id="ff4c5-115">boolean</span></span> | <span data-ttu-id="ff4c5-116">Especifica si el servicio de configuración automática para redes cableadas requiere el uso de 802.1 X para la autenticación de puertos.</span><span class="sxs-lookup"><span data-stu-id="ff4c5-116">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="ff4c5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff4c5-117">Requirements</span></span>



| <span data-ttu-id="ff4c5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff4c5-118">Requirement</span></span> | <span data-ttu-id="ff4c5-119">Value</span><span class="sxs-lookup"><span data-stu-id="ff4c5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff4c5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff4c5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ff4c5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ff4c5-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff4c5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff4c5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ff4c5-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff4c5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff4c5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff4c5-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff4c5-125">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="ff4c5-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ff4c5-126">**MSM**</span><span class="sxs-lookup"><span data-stu-id="ff4c5-126">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="ff4c5-127">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="ff4c5-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ff4c5-128">**MSM (LANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ff4c5-128">**MSM (LANProfile)**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




