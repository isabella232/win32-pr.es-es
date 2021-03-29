---
title: Método Modify de la clase MicrosoftDNS_AAAAType
description: El método Modify actualiza un registro de recursos de dirección IPv6 (AAAA).
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_AAAAType clase
- MicrosoftDNS_AAAAType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc216233fe3d41e4f1e31fe0d471e766c4dc8476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905256"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a><span data-ttu-id="3130e-106">Método Modify de la \_ clase MicrosoftDNS AAAAType</span><span class="sxs-lookup"><span data-stu-id="3130e-106">Modify method of the MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="3130e-107">El método **Modify** actualiza un registro de recursos de dirección IPv6 (aaaa).</span><span class="sxs-lookup"><span data-stu-id="3130e-107">The **Modify** method updates an IPv6 address (AAAA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3130e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3130e-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3130e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3130e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3130e-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3130e-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3130e-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="3130e-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3130e-112">*DirecciónIPv6* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3130e-112">*IPv6Address* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3130e-113">Dirección IPv6 para el host.</span><span class="sxs-lookup"><span data-stu-id="3130e-113">IPv6 address for the host.</span></span>

</dd> <dt>

<span data-ttu-id="3130e-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="3130e-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3130e-115">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="3130e-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3130e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3130e-116">Return value</span></span>

<span data-ttu-id="3130e-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3130e-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3130e-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3130e-118">Remarks</span></span>

<span data-ttu-id="3130e-119">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="3130e-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="3130e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3130e-120">Requirements</span></span>



| <span data-ttu-id="3130e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3130e-121">Requirement</span></span> | <span data-ttu-id="3130e-122">Value</span><span class="sxs-lookup"><span data-stu-id="3130e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3130e-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3130e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3130e-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3130e-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3130e-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3130e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3130e-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3130e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3130e-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3130e-127">Namespace</span></span><br/>                | <span data-ttu-id="3130e-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="3130e-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3130e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="3130e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3130e-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3130e-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3130e-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="3130e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3130e-132">**MicrosoftDNS \_ AAAAType**</span><span class="sxs-lookup"><span data-stu-id="3130e-132">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)
</dt> <dt>

[<span data-ttu-id="3130e-133">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS AAAAType**</span><span class="sxs-lookup"><span data-stu-id="3130e-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="3130e-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="3130e-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





