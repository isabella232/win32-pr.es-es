---
title: Tipo de privacidad (Wininet. h)
description: Especifica que la configuración de privacidad es para cookies de terceros o de terceros.
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38583d5f0c5cee148353f98f5d2be2d4f1a50216
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905645"
---
# <a name="privacy-type"></a><span data-ttu-id="22d5e-103">Tipo de privacidad</span><span class="sxs-lookup"><span data-stu-id="22d5e-103">Privacy Type</span></span>

<span data-ttu-id="22d5e-104">Especifica que la configuración de privacidad es para cookies de terceros o de terceros.</span><span class="sxs-lookup"><span data-stu-id="22d5e-104">Specifies that privacy settings are for either first-party or third-party cookies.</span></span>

<dl> <dt>

<span data-ttu-id="22d5e-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**tipo de privacidad de la \_ \_ primera \_ entidad**</span><span class="sxs-lookup"><span data-stu-id="22d5e-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**PRIVACY\_TYPE\_FIRST\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d5e-106">0</span><span class="sxs-lookup"><span data-stu-id="22d5e-106">0</span></span>
</dt> <dt>



<span data-ttu-id="22d5e-107">Hace referencia a la configuración de privacidad de las cookies de primera entidad.</span><span class="sxs-lookup"><span data-stu-id="22d5e-107">Refers to privacy settings for first party cookies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22d5e-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**tipo de privacidad de \_ \_ terceros \_**</span><span class="sxs-lookup"><span data-stu-id="22d5e-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**PRIVACY\_TYPE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d5e-109">1</span><span class="sxs-lookup"><span data-stu-id="22d5e-109">1</span></span>
</dt> <dt>



<span data-ttu-id="22d5e-110">Hace referencia a la configuración de privacidad de las cookies de terceros.</span><span class="sxs-lookup"><span data-stu-id="22d5e-110">Refers to privacy settings for third party cookies.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22d5e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22d5e-111">Remarks</span></span>

<span data-ttu-id="22d5e-112">Las cookies se clasifican como propias y de terceros.</span><span class="sxs-lookup"><span data-stu-id="22d5e-112">Cookies are categorized as first-party and third-party.</span></span> <span data-ttu-id="22d5e-113">Una cookie de primera entidad es aquella que se origina desde el dominio del host.</span><span class="sxs-lookup"><span data-stu-id="22d5e-113">A first-party cookie is one that originates from the host domain.</span></span> <span data-ttu-id="22d5e-114">Si " https://www.blueyonderairlines.com " se encuentra en la barra de direcciones de Microsoft Internet Explorer, "www.blueyonderairlines.com" es el dominio del host.</span><span class="sxs-lookup"><span data-stu-id="22d5e-114">If "https://www.blueyonderairlines.com" is found in the Microsoft Internet Explorer address bar, "www.blueyonderairlines.com" is the host domain.</span></span> <span data-ttu-id="22d5e-115">Al visitar esta página, si una cookie se establece desde un dominio que no sea "www.blueyonderairlines.com", como "www.fourthcoffee.com", se considera que esta cookie es una cookie de terceros.</span><span class="sxs-lookup"><span data-stu-id="22d5e-115">While visiting this page, if a cookie is set from a domain other than "www.blueyonderairlines.com", such as "www.fourthcoffee.com", this cookie is considered a third-party cookie.</span></span>

> [!Note]  
> <span data-ttu-id="22d5e-116">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="22d5e-116">WinINet does not support server implementations.</span></span> <span data-ttu-id="22d5e-117">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="22d5e-117">In addition, it should not be used from a service.</span></span> <span data-ttu-id="22d5e-118">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="22d5e-118">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22d5e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22d5e-119">Requirements</span></span>



| <span data-ttu-id="22d5e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="22d5e-120">Requirement</span></span> | <span data-ttu-id="22d5e-121">Value</span><span class="sxs-lookup"><span data-stu-id="22d5e-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="22d5e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22d5e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="22d5e-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="22d5e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="22d5e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22d5e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="22d5e-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="22d5e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="22d5e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22d5e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="22d5e-127"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="22d5e-127"><dt>Wininet.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22d5e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="22d5e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d5e-129">**PrivacyGetZonePreferenceW**</span><span class="sxs-lookup"><span data-stu-id="22d5e-129">**PrivacyGetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[<span data-ttu-id="22d5e-130">**PrivacySetZonePreferenceW**</span><span class="sxs-lookup"><span data-stu-id="22d5e-130">**PrivacySetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

