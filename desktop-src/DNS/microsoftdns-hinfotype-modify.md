---
title: Método Modify de la clase MicrosoftDNS_HINFOType
description: El método Modify actualiza un registro de recursos de información de host (HINFO).
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_HINFOType clase
- MicrosoftDNS_HINFOType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29a01eb94d82d080142d3496bab5f7f0b9acac8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802311"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="71cba-106">Método Modify de la \_ clase MicrosoftDNS HINFOType</span><span class="sxs-lookup"><span data-stu-id="71cba-106">Modify method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="71cba-107">El método **Modify** actualiza un registro de recursos de información de host (HINFO).</span><span class="sxs-lookup"><span data-stu-id="71cba-107">The **Modify** method updates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="71cba-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71cba-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="71cba-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71cba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71cba-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="71cba-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="71cba-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="71cba-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="71cba-112">*CPU* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="71cba-112">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="71cba-113">Tipo de CPU del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="71cba-113">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="71cba-114">*Sistema operativo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="71cba-114">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="71cba-115">Sistema operativo del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="71cba-115">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="71cba-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="71cba-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="71cba-117">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="71cba-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71cba-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71cba-118">Return value</span></span>

<span data-ttu-id="71cba-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="71cba-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71cba-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71cba-120">Remarks</span></span>

<span data-ttu-id="71cba-121">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="71cba-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="71cba-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71cba-122">Requirements</span></span>



| <span data-ttu-id="71cba-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="71cba-123">Requirement</span></span> | <span data-ttu-id="71cba-124">Value</span><span class="sxs-lookup"><span data-stu-id="71cba-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71cba-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71cba-125">Minimum supported client</span></span><br/> | <span data-ttu-id="71cba-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="71cba-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="71cba-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71cba-127">Minimum supported server</span></span><br/> | <span data-ttu-id="71cba-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71cba-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="71cba-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="71cba-129">Namespace</span></span><br/>                | <span data-ttu-id="71cba-130">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="71cba-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="71cba-131">MOF</span><span class="sxs-lookup"><span data-stu-id="71cba-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71cba-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71cba-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71cba-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="71cba-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71cba-134">**MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="71cba-134">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="71cba-135">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS HINFOType**</span><span class="sxs-lookup"><span data-stu-id="71cba-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="71cba-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="71cba-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





