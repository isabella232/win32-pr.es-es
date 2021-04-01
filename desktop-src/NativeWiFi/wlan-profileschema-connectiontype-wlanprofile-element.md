---
description: Indica el modo de funcionamiento de la red.
ms.assetid: b71de38a-6373-4d96-90dd-a3ad4a7de074
title: connectionType (WLANProfile), elemento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1e7b456260c656ebb3d64b6a3732fe97ca3ca488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908340"
---
# <a name="connectiontype-wlanprofile-element"></a><span data-ttu-id="1c44d-103">connectionType (WLANProfile), elemento</span><span class="sxs-lookup"><span data-stu-id="1c44d-103">connectionType (WLANProfile) Element</span></span>

<span data-ttu-id="1c44d-104">El elemento connectionType (WLANProfile) indica el modo operativo de la red.</span><span class="sxs-lookup"><span data-stu-id="1c44d-104">The connectionType (WLANProfile) element indicates the operating mode of the network.</span></span>

<span data-ttu-id="1c44d-105">Un valor de **ESS** indica una red de infraestructura, mientras que **IBSS** indica una red ad hoc.</span><span class="sxs-lookup"><span data-stu-id="1c44d-105">A value of **ESS** indicates an infrastructure network, while **IBSS** indicates an ad-hoc network.</span></span>

``` syntax
<xs:element name="connectionType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="IBSS"
             />
            <xs:enumeration
                value="ESS"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="1c44d-106">El elemento **connectionType** se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1c44d-106">The **connectionType** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="1c44d-107">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1c44d-107">Examples</span></span>

<span data-ttu-id="1c44d-108">Para ver los perfiles de ejemplo que usan el elemento **connectionType** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="1c44d-108">To view sample profiles that use the **connectionType** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c44d-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c44d-109">Requirements</span></span>



| <span data-ttu-id="1c44d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c44d-110">Requirement</span></span> | <span data-ttu-id="1c44d-111">Value</span><span class="sxs-lookup"><span data-stu-id="1c44d-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1c44d-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c44d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1c44d-113">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="1c44d-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1c44d-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c44d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1c44d-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c44d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="1c44d-116">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1c44d-116">Redistributable</span></span><br/>          | <span data-ttu-id="1c44d-117">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="1c44d-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="1c44d-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c44d-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="1c44d-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="1c44d-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1c44d-120">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="1c44d-120">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="1c44d-121">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="1c44d-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1c44d-122">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="1c44d-122">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




