---
title: Método Modify de la clase MicrosoftDNS_AType
description: El método Modify actualiza el TTL y la dirección IP de un registro de recursos de dirección de host (A).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_AType clase
- MicrosoftDNS_AType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffda093ed843cfd655711100321c9876120519c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079383"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="ded2d-106">Método Modify de la \_ clase MicrosoftDNS AType</span><span class="sxs-lookup"><span data-stu-id="ded2d-106">Modify method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="ded2d-107">El método **Modify** actualiza el TTL y la dirección IP de un registro de recursos de dirección de host (a).</span><span class="sxs-lookup"><span data-stu-id="ded2d-107">The **Modify** method updates the TTL and IP address of a host Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ded2d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ded2d-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ded2d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ded2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ded2d-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ded2d-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ded2d-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="ded2d-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ded2d-112">*Dirección IP* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ded2d-112">*IPAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ded2d-113">Cadena que representa la dirección IP del host.</span><span class="sxs-lookup"><span data-stu-id="ded2d-113">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="ded2d-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="ded2d-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ded2d-115">Referencia al objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="ded2d-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ded2d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ded2d-116">Return value</span></span>

<span data-ttu-id="ded2d-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ded2d-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ded2d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ded2d-118">Remarks</span></span>

<span data-ttu-id="ded2d-119">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="ded2d-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ded2d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ded2d-120">Requirements</span></span>



| <span data-ttu-id="ded2d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ded2d-121">Requirement</span></span> | <span data-ttu-id="ded2d-122">Value</span><span class="sxs-lookup"><span data-stu-id="ded2d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ded2d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ded2d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ded2d-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ded2d-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ded2d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ded2d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ded2d-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ded2d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ded2d-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ded2d-127">Namespace</span></span><br/>                | <span data-ttu-id="ded2d-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="ded2d-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ded2d-129">MOF</span><span class="sxs-lookup"><span data-stu-id="ded2d-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ded2d-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ded2d-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ded2d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ded2d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ded2d-132">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ded2d-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="ded2d-133">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS AType**</span><span class="sxs-lookup"><span data-stu-id="ded2d-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





