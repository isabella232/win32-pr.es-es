---
title: Métodos de la propiedad IADsNameTranslate (iAds. h)
description: Establece la propiedad ChaseReferral.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsNameTranslate ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996831"
---
# <a name="iadsnametranslate-property-methods"></a><span data-ttu-id="f9ea0-104">Métodos de propiedad IADsNameTranslate</span><span class="sxs-lookup"><span data-stu-id="f9ea0-104">IADsNameTranslate Property Methods</span></span>

<span data-ttu-id="f9ea0-105">El método Property de la interfaz [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) establece la propiedad **ChaseReferral** .</span><span class="sxs-lookup"><span data-stu-id="f9ea0-105">The property method of the [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface sets the **ChaseReferral** property.</span></span> <span data-ttu-id="f9ea0-106">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f9ea0-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f9ea0-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9ea0-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f9ea0-108">**ChaseReferral**</span><span class="sxs-lookup"><span data-stu-id="f9ea0-108">**ChaseReferral**</span></span>
<span data-ttu-id="f9ea0-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f9ea0-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="f9ea0-110">Opciones de seguimiento de referencia tal y como se define en la [**\_ \_ \_ enumeración**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)de referencias de seguimiento de anuncios.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-110">Options of referral chasing as defined in [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum).</span></span> <span data-ttu-id="f9ea0-111">Cuando se establece el seguimiento de referencias, la traducción del nombre se realiza en objetos que no pertenecen a este directorio y son las referencias devueltas por el seguimiento de la referencia.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-111">When referral chasing is set, the name translation is performed on objects that do not belong to this directory and are the referrals returned from referral chasing.</span></span>

<dt>

<span data-ttu-id="f9ea0-112">Tipo de acceso: solo escritura</span><span class="sxs-lookup"><span data-stu-id="f9ea0-112">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="f9ea0-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="f9ea0-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="f9ea0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9ea0-114">Remarks</span></span>

<span data-ttu-id="f9ea0-115">Las opciones de seguimiento de referencia solo se aplican cuando se usa [**IADsNameTranslate:: set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) y [**IADsNameTranslate:: get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get).</span><span class="sxs-lookup"><span data-stu-id="f9ea0-115">The referral chasing options apply only when you use [**IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) and [**IADsNameTranslate::Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get).</span></span> <span data-ttu-id="f9ea0-116">La característica no está disponible con [**IADsNameTranslate:: SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) o [**IADsNameTranslate:: GETEX**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).</span><span class="sxs-lookup"><span data-stu-id="f9ea0-116">The feature is not available with [**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) or [**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).</span></span>

<span data-ttu-id="f9ea0-117">La interfaz [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) tiene una implementación parcial de [**la \_ \_ \_ enumeración de referencias de seguimiento de anuncios**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) mediante la propiedad **ChaseReferral** .</span><span class="sxs-lookup"><span data-stu-id="f9ea0-117">The [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface has a partial implementation of [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) through the **ChaseReferral** property.</span></span> <span data-ttu-id="f9ea0-118">Si la propiedad **ChaseReferral** se establece en cero (0), es lo mismo que especificar las **referencias de \_ seguimiento de anuncios \_ \_ nunca** (0).</span><span class="sxs-lookup"><span data-stu-id="f9ea0-118">If the **ChaseReferral** property is set to zero (0), it is the same as specifying **ADS\_CHASE\_REFERRALS\_NEVER** (0).</span></span> <span data-ttu-id="f9ea0-119">Si se usa un valor distinto de cero, es lo mismo que especificar las **referencias de seguimiento de anuncios \_ \_ \_ siempre** (0x60).</span><span class="sxs-lookup"><span data-stu-id="f9ea0-119">If a nonzero value is used, it is the same as specifying **ADS\_CHASE\_REFERRALS\_ALWAYS** (0x60).</span></span> <span data-ttu-id="f9ea0-120">**IADsNameTranslate** no implementa las opciones externas de referencias de **\_ seguimiento \_ \_ subordinadas** (0X20) **o \_ \_ referencias \_ de seguimiento de ADS** (0x40).</span><span class="sxs-lookup"><span data-stu-id="f9ea0-120">**IADsNameTranslate** does not implement the **ADS\_CHASE\_REFERRALS\_SUBORDINATE** (0x20) or **ADS\_CHASE\_REFERRALS\_EXTERNAL** (0x40) options.</span></span>

<span data-ttu-id="f9ea0-121">La configuración predeterminada para el seguimiento de referencias está habilitada (las **referencias de seguimiento de anuncios \_ \_ \_ siempre**).</span><span class="sxs-lookup"><span data-stu-id="f9ea0-121">The default setting for referral chasing is enabled (**ADS\_CHASE\_REFERRALS\_ALWAYS**).</span></span> <span data-ttu-id="f9ea0-122">Sin el seguimiento de la referencia, puede hacer que la traducción del nombre se realice en los objetos que residen solo en el servidor de directorio conectado.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-122">Without referral chasing, you can have name translation performed on those objects residing on the connected directory server only.</span></span> <span data-ttu-id="f9ea0-123">Si no está seguro de si el objeto de interés está en el servidor especificado, debe establecer esta propiedad para que sea **\_ \_ \_ siempre referencias de seguimiento de anuncios**.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-123">If you are uncertain whether the object of interest is on the specified server, you should set this property to be **ADS\_CHASE\_REFERRALS\_ALWAYS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9ea0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9ea0-124">Requirements</span></span>



| <span data-ttu-id="f9ea0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9ea0-125">Requirement</span></span> | <span data-ttu-id="f9ea0-126">Value</span><span class="sxs-lookup"><span data-stu-id="f9ea0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ea0-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9ea0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f9ea0-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9ea0-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9ea0-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9ea0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f9ea0-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9ea0-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9ea0-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9ea0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9ea0-132"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9ea0-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f9ea0-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9ea0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9ea0-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9ea0-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f9ea0-135">IID</span><span class="sxs-lookup"><span data-stu-id="f9ea0-135">IID</span></span><br/>                      | <span data-ttu-id="f9ea0-136">IID \_ IADsNameTranslate se define como B1B272A3-3625-11D1-A3A4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="f9ea0-136">IID\_IADsNameTranslate is defined as B1B272A3-3625-11D1-A3A4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="f9ea0-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9ea0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9ea0-138">**\_ \_ enumeración de referencias de seguimiento de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="f9ea0-138">**ADS\_CHASE\_REFERRALS\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[<span data-ttu-id="f9ea0-139">**IADsNameTranslate**</span><span class="sxs-lookup"><span data-stu-id="f9ea0-139">**IADsNameTranslate**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[<span data-ttu-id="f9ea0-140">**IADsNameTranslate:: get**</span><span class="sxs-lookup"><span data-stu-id="f9ea0-140">**IADsNameTranslate::Get**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[<span data-ttu-id="f9ea0-141">**IADsNameTranslate::GetEx**</span><span class="sxs-lookup"><span data-stu-id="f9ea0-141">**IADsNameTranslate::GetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[<span data-ttu-id="f9ea0-142">**IADsNameTranslate:: set**</span><span class="sxs-lookup"><span data-stu-id="f9ea0-142">**IADsNameTranslate::Set**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[<span data-ttu-id="f9ea0-143">**IADsNameTranslate::SetEx**</span><span class="sxs-lookup"><span data-stu-id="f9ea0-143">**IADsNameTranslate::SetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[<span data-ttu-id="f9ea0-144">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="f9ea0-144">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





