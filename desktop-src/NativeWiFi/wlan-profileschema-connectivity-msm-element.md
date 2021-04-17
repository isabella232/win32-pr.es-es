---
description: Contiene varias configuraciones de conectividad.
ms.assetid: 2938f607-47a1-49eb-bf3f-247cab8637ec
title: Elemento Connectivity (MSM)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 938e5b19ffab490066fbbe299bd250191d9226a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678517"
---
# <a name="connectivity-msm-element"></a><span data-ttu-id="d4878-103">Elemento Connectivity (MSM)</span><span class="sxs-lookup"><span data-stu-id="d4878-103">connectivity (MSM) Element</span></span>

<span data-ttu-id="d4878-104">El elemento Connectivity (MSM) contiene varias configuraciones de conectividad.</span><span class="sxs-lookup"><span data-stu-id="d4878-104">The connectivity (MSM) element contains various connectivity settings.</span></span>

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="phyType"
                minOccurs="0"
                maxOccurs="4"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="a"
                         />
                        <xs:enumeration
                            value="b"
                         />
                        <xs:enumeration
                            value="g"
                         />
                        <xs:enumeration
                            value="n"
                         />
                    </xs:restriction>
                </xs:simpleType>
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

<span data-ttu-id="d4878-105">El elemento se define mediante el elemento [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d4878-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d4878-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d4878-106">Child elements</span></span>



| <span data-ttu-id="d4878-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d4878-107">Element</span></span>                                                            | <span data-ttu-id="d4878-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4878-108">Type</span></span> |
|--------------------------------------------------------------------|------|
| [<span data-ttu-id="d4878-109">**phyType**</span><span class="sxs-lookup"><span data-stu-id="d4878-109">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md) |      |



## <a name="examples"></a><span data-ttu-id="d4878-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d4878-110">Examples</span></span>

<span data-ttu-id="d4878-111">Para ver los perfiles de ejemplo que usan el elemento de **Conectividad** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d4878-111">To view sample profiles that use the **connectivity** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4878-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4878-112">Requirements</span></span>



| <span data-ttu-id="d4878-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4878-113">Requirement</span></span> | <span data-ttu-id="d4878-114">Value</span><span class="sxs-lookup"><span data-stu-id="d4878-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d4878-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4878-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d4878-116">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="d4878-116">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d4878-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4878-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d4878-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4878-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="d4878-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d4878-119">Redistributable</span></span><br/>          | <span data-ttu-id="d4878-120">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="d4878-120">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d4878-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4878-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="d4878-122">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="d4878-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d4878-123">**MSM**</span><span class="sxs-lookup"><span data-stu-id="d4878-123">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="d4878-124">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="d4878-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d4878-125">**MSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="d4878-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 




