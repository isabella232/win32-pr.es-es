---
title: Método Modify de la clase MicrosoftDNS_CNAMEType
description: El método Modify actualiza un registro de recursos de nombre canónico (CNAME).
ms.assetid: 7e550026-d901-44a0-86ac-520682232ccb
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_CNAMEType clase
- MicrosoftDNS_CNAMEType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ddbe1e1592c4331be808340c216954cd8d7b14f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490654"
---
# <a name="modify-method-of-the-microsoftdns_cnametype-class"></a><span data-ttu-id="dfb57-106">Método Modify de la \_ clase MicrosoftDNS CNAMEType</span><span class="sxs-lookup"><span data-stu-id="dfb57-106">Modify method of the MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="dfb57-107">El método **Modify** actualiza un registro de recursos de nombre canónico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="dfb57-107">The **Modify** method updates a Canonical Name (CNAME) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb57-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfb57-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="dfb57-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dfb57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfb57-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dfb57-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb57-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="dfb57-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="dfb57-112">*PrimaryName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dfb57-112">*PrimaryName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb57-113">Cadena que representa el nombre principal del registro CNAME.</span><span class="sxs-lookup"><span data-stu-id="dfb57-113">String representing the primary name for the CNAME record.</span></span>

</dd> <dt>

<span data-ttu-id="dfb57-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="dfb57-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb57-115">Referencia al objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="dfb57-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfb57-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfb57-116">Return value</span></span>

<span data-ttu-id="dfb57-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dfb57-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfb57-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfb57-118">Remarks</span></span>

<span data-ttu-id="dfb57-119">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="dfb57-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb57-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfb57-120">Requirements</span></span>



| <span data-ttu-id="dfb57-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfb57-121">Requirement</span></span> | <span data-ttu-id="dfb57-122">Value</span><span class="sxs-lookup"><span data-stu-id="dfb57-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb57-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfb57-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb57-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dfb57-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dfb57-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfb57-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb57-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dfb57-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dfb57-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dfb57-127">Namespace</span></span><br/>                | <span data-ttu-id="dfb57-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="dfb57-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dfb57-129">MOF</span><span class="sxs-lookup"><span data-stu-id="dfb57-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfb57-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfb57-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb57-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfb57-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb57-132">**MicrosoftDNS \_ CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="dfb57-132">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md)
</dt> <dt>

[<span data-ttu-id="dfb57-133">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="dfb57-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="dfb57-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="dfb57-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





