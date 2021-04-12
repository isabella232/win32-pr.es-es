---
title: Método Modify de la clase MicrosoftDNS_MFType
description: El método Modify actualiza un registro de recursos del agente de reenvío de correo para el dominio (MF).
ms.assetid: b4bc43a5-6f43-487d-ad6c-3e01d5b2b6b8
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_MFType clase
- MicrosoftDNS_MFType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0a363290580c7cecf47dbe00c6dd7895d23dbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491734"
---
# <a name="modify-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="7690d-106">Método Modify de la \_ clase MicrosoftDNS MFType</span><span class="sxs-lookup"><span data-stu-id="7690d-106">Modify method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="7690d-107">El método **Modify** actualiza un registro de recursos del agente de reenvío de correo para el dominio (MF).</span><span class="sxs-lookup"><span data-stu-id="7690d-107">The **Modify** method updates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7690d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7690d-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="7690d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7690d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7690d-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7690d-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7690d-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="7690d-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="7690d-112">*MFHost* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7690d-112">*MFHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7690d-113">Nombre del host que proporciona el agente de reenvío de correo.</span><span class="sxs-lookup"><span data-stu-id="7690d-113">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="7690d-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="7690d-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7690d-115">Referencia al objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="7690d-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7690d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7690d-116">Return value</span></span>

<span data-ttu-id="7690d-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7690d-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7690d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7690d-118">Remarks</span></span>

<span data-ttu-id="7690d-119">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="7690d-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="7690d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7690d-120">Requirements</span></span>



| <span data-ttu-id="7690d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7690d-121">Requirement</span></span> | <span data-ttu-id="7690d-122">Value</span><span class="sxs-lookup"><span data-stu-id="7690d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7690d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7690d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7690d-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7690d-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7690d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7690d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7690d-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7690d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7690d-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7690d-127">Namespace</span></span><br/>                | <span data-ttu-id="7690d-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="7690d-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="7690d-129">MOF</span><span class="sxs-lookup"><span data-stu-id="7690d-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7690d-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7690d-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7690d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7690d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7690d-132">**MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="7690d-132">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="7690d-133">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MFType**</span><span class="sxs-lookup"><span data-stu-id="7690d-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="7690d-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="7690d-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





