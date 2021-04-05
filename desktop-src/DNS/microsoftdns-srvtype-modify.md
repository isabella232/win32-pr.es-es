---
title: Método Modify de la clase MicrosoftDNS_SRVType
description: El método Modify actualiza un registro de recursos de servicio (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_SRVType clase
- MicrosoftDNS_SRVType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079703"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="432d7-106">Método Modify de la \_ clase MicrosoftDNS SRVType</span><span class="sxs-lookup"><span data-stu-id="432d7-106">Modify method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="432d7-107">El método **Modify** actualiza un registro de recursos de servicio (SRV).</span><span class="sxs-lookup"><span data-stu-id="432d7-107">The **Modify** method updates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="432d7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="432d7-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="432d7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="432d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="432d7-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="432d7-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="432d7-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="432d7-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="432d7-112">*Prioridad* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="432d7-112">*Priority* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="432d7-113">Prioridad del host de destino especificado en el nombre del propietario.</span><span class="sxs-lookup"><span data-stu-id="432d7-113">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="432d7-114">Los números más bajos implican prioridades más altas.</span><span class="sxs-lookup"><span data-stu-id="432d7-114">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="432d7-115">*Peso* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="432d7-115">*Weight* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="432d7-116">Peso del host de destino.</span><span class="sxs-lookup"><span data-stu-id="432d7-116">Weight of the target host.</span></span> <span data-ttu-id="432d7-117">Esto resulta útil al seleccionar entre los hosts que tienen la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="432d7-117">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="432d7-118">Las posibilidades de usar este host deben ser proporcionales a su peso.</span><span class="sxs-lookup"><span data-stu-id="432d7-118">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="432d7-119">*Puerto* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="432d7-119">*Port* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="432d7-120">Puerto usado en el host de destino de un servicio de protocolo.</span><span class="sxs-lookup"><span data-stu-id="432d7-120">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="432d7-121">*SRVDomainName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="432d7-121">*SRVDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="432d7-122">FQDN del host de destino.</span><span class="sxs-lookup"><span data-stu-id="432d7-122">FQDN of the target host.</span></span> <span data-ttu-id="432d7-123">Un destino de \\ . \\ significa que el servicio no está disponible en este dominio.</span><span class="sxs-lookup"><span data-stu-id="432d7-123">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="432d7-124">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="432d7-124">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="432d7-125">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="432d7-125">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="432d7-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="432d7-126">Return value</span></span>

<span data-ttu-id="432d7-127">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="432d7-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="432d7-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="432d7-128">Remarks</span></span>

<span data-ttu-id="432d7-129">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="432d7-129">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="432d7-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="432d7-130">Requirements</span></span>



| <span data-ttu-id="432d7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="432d7-131">Requirement</span></span> | <span data-ttu-id="432d7-132">Value</span><span class="sxs-lookup"><span data-stu-id="432d7-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="432d7-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="432d7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="432d7-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="432d7-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="432d7-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="432d7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="432d7-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="432d7-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="432d7-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="432d7-137">Namespace</span></span><br/>                | <span data-ttu-id="432d7-138">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="432d7-138">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="432d7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="432d7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="432d7-140"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="432d7-140"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="432d7-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="432d7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="432d7-142">**MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="432d7-142">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="432d7-143">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS SRVType**</span><span class="sxs-lookup"><span data-stu-id="432d7-143">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="432d7-144">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="432d7-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





