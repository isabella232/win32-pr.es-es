---
title: Método Modify de la clase MicrosoftDNS_TXTType
description: El método Modify actualiza un registro de recursos de texto (TXT).
ms.assetid: af61057e-95be-4290-83da-a63f01ead476
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_TXTType clase
- MicrosoftDNS_TXTType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285dfb6d5323ca3775f981aecbf5a0170392cd3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149980"
---
# <a name="modify-method-of-the-microsoftdns_txttype-class"></a><span data-ttu-id="6e09d-106">Método Modify de la \_ clase MicrosoftDNS TXTType</span><span class="sxs-lookup"><span data-stu-id="6e09d-106">Modify method of the MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="6e09d-107">El método **Modify** actualiza un registro de recursos de texto (txt).</span><span class="sxs-lookup"><span data-stu-id="6e09d-107">The **Modify** method updates a Text (TXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e09d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e09d-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="6e09d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e09d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e09d-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6e09d-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6e09d-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="6e09d-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="6e09d-112">*DescriptiveText* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e09d-112">*DescriptiveText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e09d-113">Texto descriptivo, la semántica de que depende del dominio del propietario.</span><span class="sxs-lookup"><span data-stu-id="6e09d-113">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> <dt>

<span data-ttu-id="6e09d-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="6e09d-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6e09d-115">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="6e09d-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e09d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e09d-116">Return value</span></span>

<span data-ttu-id="6e09d-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6e09d-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e09d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e09d-118">Remarks</span></span>

<span data-ttu-id="6e09d-119">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="6e09d-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e09d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e09d-120">Requirements</span></span>



| <span data-ttu-id="6e09d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e09d-121">Requirement</span></span> | <span data-ttu-id="6e09d-122">Value</span><span class="sxs-lookup"><span data-stu-id="6e09d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e09d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e09d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6e09d-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6e09d-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6e09d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e09d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6e09d-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e09d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6e09d-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6e09d-127">Namespace</span></span><br/>                | <span data-ttu-id="6e09d-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="6e09d-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6e09d-129">MOF</span><span class="sxs-lookup"><span data-stu-id="6e09d-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e09d-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e09d-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e09d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e09d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e09d-132">**MicrosoftDNS \_ TXTType**</span><span class="sxs-lookup"><span data-stu-id="6e09d-132">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)
</dt> <dt>

[<span data-ttu-id="6e09d-133">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS TXTType**</span><span class="sxs-lookup"><span data-stu-id="6e09d-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6e09d-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="6e09d-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





