---
title: Método Modify de la clase MicrosoftDNS_WINSRType
description: El método Modify actualiza un registro de recursos de búsqueda inversa de WINS (WINSr).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_WINSRType clase
- MicrosoftDNS_WINSRType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02d89c3cd191262136035f9006853e2f1a7f7dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151037"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="dcedd-106">Método Modify de la \_ clase MicrosoftDNS WINSRType</span><span class="sxs-lookup"><span data-stu-id="dcedd-106">Modify method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="dcedd-107">El método **Modify** actualiza un registro de recursos de búsqueda inversa de WINS (WINSR).</span><span class="sxs-lookup"><span data-stu-id="dcedd-107">The **Modify** method updates a WINS Reverse Look up (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcedd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcedd-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="dcedd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcedd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcedd-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dcedd-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dcedd-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="dcedd-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="dcedd-112">*MappingFlag* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dcedd-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dcedd-113">Marca de asignación de WINSr que especifica si el registro debe incluirse en la replicación de zona.</span><span class="sxs-lookup"><span data-stu-id="dcedd-113">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="dcedd-114">Puede tener solo dos valores: 0x80000000 y 0x00010000 correspondientes a las marcas de replicación y no replicación (registro local), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="dcedd-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="dcedd-115">*Tiempodeesperadebúsqueda* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dcedd-115">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dcedd-116">Tiempo de espera, en segundos, para un servidor DNS que usa la búsqueda inversa de WINS.</span><span class="sxs-lookup"><span data-stu-id="dcedd-116">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="dcedd-117">*CacheTimeout* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dcedd-117">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dcedd-118">Tiempo, en segundos, que un servidor DNS que usa la búsqueda WINS puede almacenar en caché la respuesta del servidor WINS.</span><span class="sxs-lookup"><span data-stu-id="dcedd-118">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="dcedd-119">*ResultDomain* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dcedd-119">*ResultDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dcedd-120">Nombre de dominio que se va a anexar a los nombres NetBIOS devueltos.</span><span class="sxs-lookup"><span data-stu-id="dcedd-120">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="dcedd-121">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="dcedd-121">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="dcedd-122">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="dcedd-122">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcedd-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcedd-123">Return value</span></span>

<span data-ttu-id="dcedd-124">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dcedd-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcedd-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcedd-125">Remarks</span></span>

<span data-ttu-id="dcedd-126">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="dcedd-126">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcedd-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcedd-127">Requirements</span></span>



| <span data-ttu-id="dcedd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcedd-128">Requirement</span></span> | <span data-ttu-id="dcedd-129">Value</span><span class="sxs-lookup"><span data-stu-id="dcedd-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcedd-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcedd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dcedd-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dcedd-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dcedd-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcedd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dcedd-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dcedd-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dcedd-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dcedd-134">Namespace</span></span><br/>                | <span data-ttu-id="dcedd-135">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="dcedd-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dcedd-136">MOF</span><span class="sxs-lookup"><span data-stu-id="dcedd-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcedd-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcedd-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcedd-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcedd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcedd-139">**MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="dcedd-139">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="dcedd-140">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS WINSRType**</span><span class="sxs-lookup"><span data-stu-id="dcedd-140">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="dcedd-141">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="dcedd-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





