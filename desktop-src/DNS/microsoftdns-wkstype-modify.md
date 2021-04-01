---
title: Método Modify de la clase MicrosoftDNS_WKSType
description: El método Modify actualiza un registro de recursos de Well-Known Services (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_WKSType clase
- MicrosoftDNS_WKSType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905388"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="befef-106">Método Modify de la \_ clase MicrosoftDNS WKSType</span><span class="sxs-lookup"><span data-stu-id="befef-106">Modify method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="befef-107">El método **Modify** actualiza un registro de recursos de Well-Known Services (WKS).</span><span class="sxs-lookup"><span data-stu-id="befef-107">The **Modify** method updates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="befef-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="befef-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="befef-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="befef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="befef-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="befef-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="befef-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="befef-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="befef-112">*InternetAddress* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="befef-112">*InternetAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="befef-113">Dirección IP de Internet del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="befef-113">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="befef-114">*IPProtocol* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="befef-114">*IPProtocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="befef-115">Cadena que representa el protocolo IP para este registro.</span><span class="sxs-lookup"><span data-stu-id="befef-115">String representing the IP protocol for this record.</span></span> <span data-ttu-id="befef-116">Los valores válidos son UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="befef-116">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="befef-117">*Servicios* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="befef-117">*Services* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="befef-118">Cadena que contiene todos los servicios utilizados por el registro de servicio conocido (WKS).</span><span class="sxs-lookup"><span data-stu-id="befef-118">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="befef-119">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="befef-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="befef-120">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="befef-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="befef-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="befef-121">Return value</span></span>

<span data-ttu-id="befef-122">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="befef-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="befef-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="befef-123">Remarks</span></span>

<span data-ttu-id="befef-124">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="befef-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="befef-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="befef-125">Requirements</span></span>



| <span data-ttu-id="befef-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="befef-126">Requirement</span></span> | <span data-ttu-id="befef-127">Value</span><span class="sxs-lookup"><span data-stu-id="befef-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="befef-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="befef-128">Minimum supported client</span></span><br/> | <span data-ttu-id="befef-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="befef-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="befef-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="befef-130">Minimum supported server</span></span><br/> | <span data-ttu-id="befef-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="befef-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="befef-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="befef-132">Namespace</span></span><br/>                | <span data-ttu-id="befef-133">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="befef-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="befef-134">MOF</span><span class="sxs-lookup"><span data-stu-id="befef-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="befef-135"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="befef-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="befef-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="befef-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="befef-137">**MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="befef-137">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="befef-138">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS WKSType**</span><span class="sxs-lookup"><span data-stu-id="befef-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="befef-139">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="befef-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





