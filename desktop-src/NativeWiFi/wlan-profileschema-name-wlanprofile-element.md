---
description: Contiene el nombre de un perfil de LAN inalámbrica.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: nombre (WLANProfile) (elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 79174d1cb24fff1841b3022fa06e201794415ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543742"
---
# <a name="name-wlanprofile-element"></a><span data-ttu-id="d9de4-103">nombre (WLANProfile) (elemento)</span><span class="sxs-lookup"><span data-stu-id="d9de4-103">name (WLANProfile) Element</span></span>

<span data-ttu-id="d9de4-104">El elemento Name (WLANProfile) contiene el nombre de un perfil de LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="d9de4-104">The name (WLANProfile) element contains the name of a wireless LAN profile.</span></span>

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

<span data-ttu-id="d9de4-105">El elemento **Name** se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d9de4-105">The **name** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9de4-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9de4-106">Remarks</span></span>

<span data-ttu-id="d9de4-107">Los nombres distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d9de4-107">Names are case-sensitive.</span></span>

<span data-ttu-id="d9de4-108">En Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2), el elemento Name se omite cuando el perfil se guarda en el almacén de perfiles.</span><span class="sxs-lookup"><span data-stu-id="d9de4-108">For Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2), the name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="d9de4-109">El nombre del perfil se deriva del SSID de la red.</span><span class="sxs-lookup"><span data-stu-id="d9de4-109">The name of the profile is derived from the SSID of the network.</span></span> <span data-ttu-id="d9de4-110">En el caso de los perfiles de red de infraestructura, el nombre del perfil es el SSID de la red.</span><span class="sxs-lookup"><span data-stu-id="d9de4-110">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="d9de4-111">En el caso de los perfiles de red ad hoc, el nombre del perfil es el SSID de la red ad hoc seguido de `-adhoc` .</span><span class="sxs-lookup"><span data-stu-id="d9de4-111">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> <span data-ttu-id="d9de4-112">No se muestran los caracteres de escape XML, como &.</span><span class="sxs-lookup"><span data-stu-id="d9de4-112">XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="d9de4-113">Evite usar caracteres de escape XML en nombres SSID para los perfiles implementados en Windows XP con SP3 o la API de LAN inalámbrica para Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="d9de4-113">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 or Wireless LAN API for Windows XP with SP2.</span></span>

<span data-ttu-id="d9de4-114">En el caso de cualquier perfil de red diseñado para usarse solo en Windows Vista o Windows Server 2008, el nombre puede ser cualquier cadena.</span><span class="sxs-lookup"><span data-stu-id="d9de4-114">For any network profile intended for use only on Windows Vista or Windows Server 2008, the name can be any string.</span></span>

## <a name="examples"></a><span data-ttu-id="d9de4-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d9de4-115">Examples</span></span>

<span data-ttu-id="d9de4-116">Para ver los perfiles de ejemplo que usan el elemento **Name** , vea [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d9de4-116">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9de4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9de4-117">Requirements</span></span>



| <span data-ttu-id="d9de4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9de4-118">Requirement</span></span> | <span data-ttu-id="d9de4-119">Value</span><span class="sxs-lookup"><span data-stu-id="d9de4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d9de4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9de4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d9de4-121">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="d9de4-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d9de4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9de4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d9de4-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9de4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="d9de4-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d9de4-124">Redistributable</span></span><br/>          | <span data-ttu-id="d9de4-125">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="d9de4-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d9de4-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9de4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9de4-127">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="d9de4-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d9de4-128">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="d9de4-128">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="d9de4-129">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="d9de4-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d9de4-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="d9de4-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




