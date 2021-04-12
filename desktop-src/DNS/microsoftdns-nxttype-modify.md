---
title: Método Modify de la clase MicrosoftDNS_NXTType
description: El método Modify actualiza un registro de recursos (NXT) siguiente.
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_NXTType clase
- MicrosoftDNS_NXTType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bab7bf8480c7e18914cac4f7ae0deb8a608090f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489772"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="c21ec-106">Método Modify de la \_ clase MicrosoftDNS NXTType</span><span class="sxs-lookup"><span data-stu-id="c21ec-106">Modify method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="c21ec-107">El método **Modify** actualiza un registro de recursos (NXT) siguiente.</span><span class="sxs-lookup"><span data-stu-id="c21ec-107">The **Modify** method updates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c21ec-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c21ec-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c21ec-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c21ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c21ec-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c21ec-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c21ec-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="c21ec-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c21ec-112">*NextDomainName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c21ec-112">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c21ec-113">Siguiente nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="c21ec-113">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="c21ec-114">*Tipos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c21ec-114">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c21ec-115">Lista separada por espacios de los códigos mnemónicos del tipo RR para el nombre del propietario del registro de recursos NXT.</span><span class="sxs-lookup"><span data-stu-id="c21ec-115">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="c21ec-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c21ec-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c21ec-117">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="c21ec-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c21ec-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c21ec-118">Return value</span></span>

<span data-ttu-id="c21ec-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c21ec-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c21ec-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c21ec-120">Remarks</span></span>

<span data-ttu-id="c21ec-121">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="c21ec-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="c21ec-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c21ec-122">Requirements</span></span>



| <span data-ttu-id="c21ec-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c21ec-123">Requirement</span></span> | <span data-ttu-id="c21ec-124">Value</span><span class="sxs-lookup"><span data-stu-id="c21ec-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c21ec-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c21ec-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c21ec-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c21ec-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c21ec-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c21ec-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c21ec-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c21ec-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c21ec-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c21ec-129">Namespace</span></span><br/>                | <span data-ttu-id="c21ec-130">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="c21ec-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c21ec-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c21ec-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c21ec-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c21ec-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c21ec-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c21ec-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c21ec-134">**MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="c21ec-134">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="c21ec-135">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS NXTType**</span><span class="sxs-lookup"><span data-stu-id="c21ec-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c21ec-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c21ec-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





