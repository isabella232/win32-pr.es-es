---
title: Método Modify de la clase MicrosoftDNS_ISDNType
description: El método Modify actualiza un registro de recursos ISDN.
ms.assetid: 09e23853-ca92-43a3-8bd9-7de10eb5eddc
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_ISDNType clase
- MicrosoftDNS_ISDNType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c369a6650c834ff9f35af6389c346daec86a954
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995959"
---
# <a name="modify-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="a74dc-106">Método Modify de la \_ clase MicrosoftDNS ISDNType</span><span class="sxs-lookup"><span data-stu-id="a74dc-106">Modify method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="a74dc-107">El método **Modify** actualiza un registro de recursos ISDN.</span><span class="sxs-lookup"><span data-stu-id="a74dc-107">The **Modify** method updates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a74dc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a74dc-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                ISDNNumber,
  [in, optional] string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="a74dc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a74dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a74dc-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a74dc-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a74dc-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="a74dc-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="a74dc-112">*ISDNNumber* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a74dc-112">*ISDNNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a74dc-113">Número ISDN y DDI del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="a74dc-113">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="a74dc-114">*Subdirección* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a74dc-114">*SubAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a74dc-115">Subdirección del propietario, si está definido.</span><span class="sxs-lookup"><span data-stu-id="a74dc-115">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="a74dc-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="a74dc-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a74dc-117">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="a74dc-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a74dc-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a74dc-118">Return value</span></span>

<span data-ttu-id="a74dc-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a74dc-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a74dc-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a74dc-120">Remarks</span></span>

<span data-ttu-id="a74dc-121">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="a74dc-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="a74dc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a74dc-122">Requirements</span></span>



| <span data-ttu-id="a74dc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a74dc-123">Requirement</span></span> | <span data-ttu-id="a74dc-124">Value</span><span class="sxs-lookup"><span data-stu-id="a74dc-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a74dc-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a74dc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a74dc-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a74dc-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a74dc-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a74dc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a74dc-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a74dc-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a74dc-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a74dc-129">Namespace</span></span><br/>                | <span data-ttu-id="a74dc-130">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="a74dc-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a74dc-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a74dc-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a74dc-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a74dc-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a74dc-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a74dc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74dc-134">**MicrosoftDNS \_ ISDNType**</span><span class="sxs-lookup"><span data-stu-id="a74dc-134">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="a74dc-135">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS ISDNType**</span><span class="sxs-lookup"><span data-stu-id="a74dc-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a74dc-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="a74dc-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





