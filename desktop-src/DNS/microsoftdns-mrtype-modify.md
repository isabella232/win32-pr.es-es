---
title: Método Modify de la clase MicrosoftDNS_MRType
description: El método Modify actualiza un registro de recursos de cambio de nombre de buzón (MR).
ms.assetid: eb833735-d485-4603-9976-305244537acd
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_MRType clase
- MicrosoftDNS_MRType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996692301e8446b3fd67e20eca036cd085e83b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490486"
---
# <a name="modify-method-of-the-microsoftdns_mrtype-class"></a><span data-ttu-id="061fa-106">Método Modify de la \_ clase MicrosoftDNS MRType</span><span class="sxs-lookup"><span data-stu-id="061fa-106">Modify method of the MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="061fa-107">El método **Modify** actualiza un registro de recursos de cambio de nombre de buzón (MR).</span><span class="sxs-lookup"><span data-stu-id="061fa-107">The **Modify** method updates a Mailbox Rename (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="061fa-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="061fa-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="061fa-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="061fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="061fa-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="061fa-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="061fa-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="061fa-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="061fa-112">*MRMailbox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="061fa-112">*MRMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="061fa-113">FQDN que especifica un buzón que es el cambio de nombre adecuado del buzón especificado en el nombre del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="061fa-113">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="061fa-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="061fa-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="061fa-115">Referencia al objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="061fa-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="061fa-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="061fa-116">Return value</span></span>

<span data-ttu-id="061fa-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="061fa-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="061fa-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="061fa-118">Remarks</span></span>

<span data-ttu-id="061fa-119">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="061fa-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="061fa-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="061fa-120">Requirements</span></span>



| <span data-ttu-id="061fa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="061fa-121">Requirement</span></span> | <span data-ttu-id="061fa-122">Value</span><span class="sxs-lookup"><span data-stu-id="061fa-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="061fa-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="061fa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="061fa-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="061fa-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="061fa-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="061fa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="061fa-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="061fa-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="061fa-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="061fa-127">Namespace</span></span><br/>                | <span data-ttu-id="061fa-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="061fa-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="061fa-129">MOF</span><span class="sxs-lookup"><span data-stu-id="061fa-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="061fa-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="061fa-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="061fa-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="061fa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061fa-132">**MicrosoftDNS \_ MRType**</span><span class="sxs-lookup"><span data-stu-id="061fa-132">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)
</dt> <dt>

[<span data-ttu-id="061fa-133">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MRType**</span><span class="sxs-lookup"><span data-stu-id="061fa-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="061fa-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="061fa-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





