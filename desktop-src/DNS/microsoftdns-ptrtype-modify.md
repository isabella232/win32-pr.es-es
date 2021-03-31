---
title: Método Modify de la clase MicrosoftDNS_PTRType
description: El método Modify actualiza un registro de recursos de puntero (PTR).
ms.assetid: 801a6bc9-e384-4912-a73a-6b04a1655002
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_PTRType clase
- MicrosoftDNS_PTRType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 840bf100ea5cdbbb606837e90d8fa9fcebab57fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996547"
---
# <a name="modify-method-of-the-microsoftdns_ptrtype-class"></a><span data-ttu-id="c3fa4-106">Método Modify de la \_ clase MicrosoftDNS PTRType</span><span class="sxs-lookup"><span data-stu-id="c3fa4-106">Modify method of the MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="c3fa4-107">El método **Modify** actualiza un registro de recursos de puntero (PTR).</span><span class="sxs-lookup"><span data-stu-id="c3fa4-107">The **Modify** method updates a Pointer (PTR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3fa4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3fa4-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c3fa4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3fa4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3fa4-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c3fa4-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3fa4-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="c3fa4-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c3fa4-112">*PTRDomainName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c3fa4-112">*PTRDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3fa4-113">Dirección del nombre de dominio del registro PTR.</span><span class="sxs-lookup"><span data-stu-id="c3fa4-113">Domain name address of the PTR record.</span></span>

</dd> <dt>

<span data-ttu-id="c3fa4-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c3fa4-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c3fa4-115">Referencia al objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="c3fa4-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3fa4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3fa4-116">Return value</span></span>

<span data-ttu-id="c3fa4-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c3fa4-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3fa4-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3fa4-118">Remarks</span></span>

<span data-ttu-id="c3fa4-119">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="c3fa4-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3fa4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3fa4-120">Requirements</span></span>



| <span data-ttu-id="c3fa4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3fa4-121">Requirement</span></span> | <span data-ttu-id="c3fa4-122">Value</span><span class="sxs-lookup"><span data-stu-id="c3fa4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3fa4-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3fa4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c3fa4-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c3fa4-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c3fa4-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3fa4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c3fa4-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c3fa4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c3fa4-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c3fa4-127">Namespace</span></span><br/>                | <span data-ttu-id="c3fa4-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="c3fa4-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c3fa4-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c3fa4-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3fa4-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3fa4-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3fa4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3fa4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3fa4-132">**MicrosoftDNS \_ PTRType**</span><span class="sxs-lookup"><span data-stu-id="c3fa4-132">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="c3fa4-133">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS PTRType**</span><span class="sxs-lookup"><span data-stu-id="c3fa4-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c3fa4-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c3fa4-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





