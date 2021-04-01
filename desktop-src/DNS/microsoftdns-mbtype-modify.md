---
title: Método Modify de la clase MicrosoftDNS_MBType
description: El método Modify actualiza un registro de recursos de buzón (MB).
ms.assetid: ee76031c-ac1b-4ebb-9fb2-3b64553867cc
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_MBType clase
- MicrosoftDNS_MBType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 135d6f0fcb0faf5c1e8da152798863c8cecc8641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802642"
---
# <a name="modify-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="4d757-106">Método Modify de la \_ clase MicrosoftDNS MBType</span><span class="sxs-lookup"><span data-stu-id="4d757-106">Modify method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="4d757-107">El método **Modify** actualiza un registro de recursos de buzón (MB).</span><span class="sxs-lookup"><span data-stu-id="4d757-107">The **Modify** method updates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d757-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d757-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MBHost,
  [out, ref]     MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="4d757-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d757-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d757-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4d757-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d757-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="4d757-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="4d757-112">*MBHost* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d757-112">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d757-113">Cadena que representa el nombre de host del buzón del registro MB.</span><span class="sxs-lookup"><span data-stu-id="4d757-113">String representing the mailbox host name for the MB record.</span></span>

</dd> <dt>

<span data-ttu-id="4d757-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="4d757-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4d757-115">Referencia al objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="4d757-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d757-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d757-116">Return value</span></span>

<span data-ttu-id="4d757-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4d757-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d757-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d757-118">Remarks</span></span>

<span data-ttu-id="4d757-119">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="4d757-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d757-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d757-120">Requirements</span></span>



| <span data-ttu-id="4d757-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d757-121">Requirement</span></span> | <span data-ttu-id="4d757-122">Value</span><span class="sxs-lookup"><span data-stu-id="4d757-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d757-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d757-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4d757-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4d757-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4d757-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d757-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4d757-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4d757-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4d757-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4d757-127">Namespace</span></span><br/>                | <span data-ttu-id="4d757-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="4d757-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4d757-129">MOF</span><span class="sxs-lookup"><span data-stu-id="4d757-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d757-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d757-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d757-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d757-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d757-132">**MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="4d757-132">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="4d757-133">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MBType**</span><span class="sxs-lookup"><span data-stu-id="4d757-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="4d757-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="4d757-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





