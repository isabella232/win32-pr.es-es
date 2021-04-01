---
title: Método Modify de la clase MicrosoftDNS_WINSType
description: El método Modify actualiza un registro de recursos del servicio de nombres Internet de Windows (WINS).
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_WINSType clase
- MicrosoftDNS_WINSType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905391"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="5a545-106">Método Modify de la \_ clase MicrosoftDNS WINSType</span><span class="sxs-lookup"><span data-stu-id="5a545-106">Modify method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="5a545-107">El método **Modify** actualiza un registro de recursos del servicio de nombres Internet de Windows (WINS).</span><span class="sxs-lookup"><span data-stu-id="5a545-107">The **Modify** method updates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a545-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a545-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="5a545-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a545-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a545-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5a545-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5a545-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="5a545-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="5a545-112">*MappingFlag* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5a545-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5a545-113">Marca de asignación WINS que especifica si el registro debe incluirse en la replicación de zona.</span><span class="sxs-lookup"><span data-stu-id="5a545-113">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="5a545-114">Puede tener solo dos valores: 0x80000000 y 0x00010000 correspondientes a las marcas de replicación y no replicación (registro local), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5a545-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="5a545-115">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="5a545-115">The following values are valid.</span></span>



| <span data-ttu-id="5a545-116">Value</span><span class="sxs-lookup"><span data-stu-id="5a545-116">Value</span></span>                                                                                                                                               | <span data-ttu-id="5a545-117">Significado</span><span class="sxs-lookup"><span data-stu-id="5a545-117">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="5a545-118"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="5a545-118"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="5a545-119">Marca de replicación</span><span class="sxs-lookup"><span data-stu-id="5a545-119">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="5a545-120"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="5a545-120"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="5a545-121">Marca de no replicación (registro local)</span><span class="sxs-lookup"><span data-stu-id="5a545-121">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5a545-122">*Tiempodeesperadebúsqueda* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5a545-122">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5a545-123">Tiempo, en segundos, que un servidor DNS intenta resolver mediante la búsqueda de WINS.</span><span class="sxs-lookup"><span data-stu-id="5a545-123">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="5a545-124">*CacheTimeout* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5a545-124">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5a545-125">Tiempo, en segundos, que un servidor DNS que usa WINS buscan puede almacenar en caché la respuesta del servidor WINS.</span><span class="sxs-lookup"><span data-stu-id="5a545-125">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="5a545-126">*WinsServers* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5a545-126">*WinsServers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5a545-127">Lista de direcciones IP separadas por comas de los servidores WINS utilizados en WINS looks.</span><span class="sxs-lookup"><span data-stu-id="5a545-127">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="5a545-128">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="5a545-128">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5a545-129">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="5a545-129">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a545-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a545-130">Return value</span></span>

<span data-ttu-id="5a545-131">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5a545-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a545-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a545-132">Remarks</span></span>

<span data-ttu-id="5a545-133">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="5a545-133">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a545-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a545-134">Requirements</span></span>



| <span data-ttu-id="5a545-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a545-135">Requirement</span></span> | <span data-ttu-id="5a545-136">Value</span><span class="sxs-lookup"><span data-stu-id="5a545-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a545-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a545-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5a545-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5a545-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5a545-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a545-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5a545-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a545-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5a545-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5a545-141">Namespace</span></span><br/>                | <span data-ttu-id="5a545-142">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="5a545-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5a545-143">MOF</span><span class="sxs-lookup"><span data-stu-id="5a545-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a545-144"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a545-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a545-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a545-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a545-146">**MicrosoftDNS \_ WINSType**</span><span class="sxs-lookup"><span data-stu-id="5a545-146">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="5a545-147">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS WINSType**</span><span class="sxs-lookup"><span data-stu-id="5a545-147">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="5a545-148">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="5a545-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





