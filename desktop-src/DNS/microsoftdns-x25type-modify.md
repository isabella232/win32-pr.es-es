---
title: Método Modify de la clase MicrosoftDNS_X25Type
description: El método Modify actualiza un registro de recursos X. 25 (x25).
ms.assetid: 2d82d67e-ae29-4ded-86fe-7db0ef5ed74f
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_X25Type clase
- MicrosoftDNS_X25Type de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10db2fa770d3da8487a712e631c41fdd4256bf7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150529"
---
# <a name="modify-method-of-the-microsoftdns_x25type-class"></a><span data-ttu-id="e7937-106">Método Modify de la \_ clase MicrosoftDNS X25Type</span><span class="sxs-lookup"><span data-stu-id="e7937-106">Modify method of the MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="e7937-107">El método **Modify** actualiza un registro de recursos X. 25 (x25).</span><span class="sxs-lookup"><span data-stu-id="e7937-107">The **Modify** method updates an X.25 (X25) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7937-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7937-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a><span data-ttu-id="e7937-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7937-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7937-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e7937-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e7937-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="e7937-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="e7937-112">*PSDNAddress* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e7937-112">*PSDNAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e7937-113">Dirección PSDN del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="e7937-113">PSDN address of the owner of the RR.</span></span>

</dd> <dt>

<span data-ttu-id="e7937-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e7937-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e7937-115">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="e7937-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7937-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7937-116">Return value</span></span>

<span data-ttu-id="e7937-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e7937-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7937-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7937-118">Remarks</span></span>

<span data-ttu-id="e7937-119">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="e7937-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7937-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7937-120">Requirements</span></span>



| <span data-ttu-id="e7937-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7937-121">Requirement</span></span> | <span data-ttu-id="e7937-122">Value</span><span class="sxs-lookup"><span data-stu-id="e7937-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7937-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7937-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e7937-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e7937-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e7937-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7937-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e7937-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e7937-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e7937-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e7937-127">Namespace</span></span><br/>                | <span data-ttu-id="e7937-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="e7937-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e7937-129">MOF</span><span class="sxs-lookup"><span data-stu-id="e7937-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7937-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7937-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7937-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7937-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7937-132">**MicrosoftDNS \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="e7937-132">**MicrosoftDNS\_X25Type**</span></span>](microsoftdns-x25type.md)
</dt> <dt>

[<span data-ttu-id="e7937-133">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS X25Type**</span><span class="sxs-lookup"><span data-stu-id="e7937-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e7937-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="e7937-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





