---
description: Indica si la conexión a una LAN inalámbrica debe ser automática o iniciada por el usuario.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: Elemento connectionMode (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811467"
---
# <a name="connectionmode-wlanprofile-element"></a><span data-ttu-id="a9dcf-103">Elemento connectionMode (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="a9dcf-103">connectionMode (WLANProfile) Element</span></span>

<span data-ttu-id="a9dcf-104">El elemento connectionMode (WLANProfile) indica si la conexión a una LAN inalámbrica debe ser automática o iniciada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-104">The connectionMode (WLANProfile) element indicates whether connection to a wireless LAN should be automatic or initiated by user.</span></span>

<span data-ttu-id="a9dcf-105">Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en ESS, este valor puede ser auto o manual.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-105">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either auto or manual.</span></span> <span data-ttu-id="a9dcf-106">Si este elemento no está presente, el valor predeterminado es auto.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-106">The default value is auto if this element is absent.</span></span>

<span data-ttu-id="a9dcf-107">Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en IBSS, este valor debe ser manual.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be manual.</span></span>

``` syntax
<xs:element name="connectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="manual"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="a9dcf-108">El elemento **connectionMode** se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a9dcf-108">The **connectionMode** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9dcf-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9dcf-109">Remarks</span></span>

<span data-ttu-id="a9dcf-110">En la tabla siguiente se describen los valores de enumeración.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-110">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="a9dcf-111">Value</span><span class="sxs-lookup"><span data-stu-id="a9dcf-111">Value</span></span>  | <span data-ttu-id="a9dcf-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9dcf-112">Description</span></span>                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9dcf-113">auto</span><span class="sxs-lookup"><span data-stu-id="a9dcf-113">auto</span></span>   | <span data-ttu-id="a9dcf-114">La conexión a la red inalámbrica debe iniciarse automáticamente cuando la red esté dentro del alcance.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-114">The connection to the wireless network should be initiated automatically whenever the network is in range.</span></span> |
| <span data-ttu-id="a9dcf-115">manual</span><span class="sxs-lookup"><span data-stu-id="a9dcf-115">manual</span></span> | <span data-ttu-id="a9dcf-116">La conexión a la red inalámbrica solo se inicia en la solicitud explícita de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-116">The connection to the wireless network is only initated upon the explicit request of a user.</span></span>               |



 

## <a name="examples"></a><span data-ttu-id="a9dcf-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a9dcf-117">Examples</span></span>

<span data-ttu-id="a9dcf-118">Para ver los perfiles de ejemplo que usan el elemento **connectionMode** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="a9dcf-118">To view sample profiles that use the **connectionMode** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9dcf-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9dcf-119">Requirements</span></span>



| <span data-ttu-id="a9dcf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9dcf-120">Requirement</span></span> | <span data-ttu-id="a9dcf-121">Value</span><span class="sxs-lookup"><span data-stu-id="a9dcf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a9dcf-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9dcf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a9dcf-123">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="a9dcf-123">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a9dcf-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9dcf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a9dcf-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9dcf-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a9dcf-126">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a9dcf-126">Redistributable</span></span><br/>          | <span data-ttu-id="a9dcf-127">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="a9dcf-127">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a9dcf-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9dcf-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="a9dcf-129">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="a9dcf-129">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a9dcf-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="a9dcf-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="a9dcf-131">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="a9dcf-131">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a9dcf-132">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="a9dcf-132">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




