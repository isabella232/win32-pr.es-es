---
title: Método Modify de la clase MicrosoftDNS_RTType
description: El método Modify actualiza un registro de recursos de ruta a través de (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_RTType clase
- MicrosoftDNS_RTType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8267bf1dc256ec95a456978643226ab5c01af93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534324"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="dc1e4-106">Método Modify de la \_ clase MicrosoftDNS RTType</span><span class="sxs-lookup"><span data-stu-id="dc1e4-106">Modify method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="dc1e4-107">El método **Modify** actualiza un registro de recursos de ruta a través de (RT).</span><span class="sxs-lookup"><span data-stu-id="dc1e4-107">The **Modify** method updates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc1e4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc1e4-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="dc1e4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc1e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc1e4-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dc1e4-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dc1e4-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="dc1e4-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="dc1e4-112">*Preferencia* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dc1e4-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dc1e4-113">Preferencia asignada a este RR entre otros en el mismo propietario.</span><span class="sxs-lookup"><span data-stu-id="dc1e4-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="dc1e4-114">Se prefieren los valores inferiores.</span><span class="sxs-lookup"><span data-stu-id="dc1e4-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="dc1e4-115">*IntermediateHost* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dc1e4-115">*IntermediateHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dc1e4-116">FQDN que especifica un host que actúa como intermediario para alcanzar el host especificado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="dc1e4-116">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="dc1e4-117">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="dc1e4-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="dc1e4-118">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="dc1e4-118">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc1e4-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc1e4-119">Return value</span></span>

<span data-ttu-id="dc1e4-120">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dc1e4-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc1e4-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc1e4-121">Remarks</span></span>

<span data-ttu-id="dc1e4-122">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="dc1e4-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc1e4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc1e4-123">Requirements</span></span>



| <span data-ttu-id="dc1e4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc1e4-124">Requirement</span></span> | <span data-ttu-id="dc1e4-125">Value</span><span class="sxs-lookup"><span data-stu-id="dc1e4-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc1e4-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc1e4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dc1e4-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dc1e4-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dc1e4-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc1e4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dc1e4-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc1e4-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dc1e4-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc1e4-130">Namespace</span></span><br/>                | <span data-ttu-id="dc1e4-131">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="dc1e4-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dc1e4-132">MOF</span><span class="sxs-lookup"><span data-stu-id="dc1e4-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc1e4-133"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc1e4-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc1e4-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc1e4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc1e4-135">**MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="dc1e4-135">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="dc1e4-136">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS RTType**</span><span class="sxs-lookup"><span data-stu-id="dc1e4-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="dc1e4-137">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="dc1e4-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





