---
title: Método Modify de la clase MicrosoftDNS_MINFOType
description: El método Modify actualiza un registro de recursos de información de correo (MINFO).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_MINFOType clase
- MicrosoftDNS_MINFOType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b59d7d1231ed88e61a0ecf94cef50041ca772f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489773"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="c5f72-106">Método Modify de la \_ clase MicrosoftDNS MINFOType</span><span class="sxs-lookup"><span data-stu-id="c5f72-106">Modify method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="c5f72-107">El método **Modify** actualiza un registro de recursos de información de correo (MINFO).</span><span class="sxs-lookup"><span data-stu-id="c5f72-107">The **Modify** method updates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5f72-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5f72-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c5f72-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5f72-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5f72-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c5f72-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f72-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="c5f72-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c5f72-112">*ResponsibleMailbox* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c5f72-112">*ResponsibleMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f72-113">FQDN que especifica un buzón responsable de la lista de distribución de correo o el buzón especificado en el nombre del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="c5f72-113">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="c5f72-114">*ErrorMailbox* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c5f72-114">*ErrorMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f72-115">FQDN que especifica un buzón para recibir mensajes de error relacionados con la lista de distribución de correo o con el buzón especificado por el nombre del propietario del registro MINFO.</span><span class="sxs-lookup"><span data-stu-id="c5f72-115">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="c5f72-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c5f72-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f72-117">Referencia al objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="c5f72-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5f72-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5f72-118">Return value</span></span>

<span data-ttu-id="c5f72-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c5f72-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5f72-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5f72-120">Remarks</span></span>

<span data-ttu-id="c5f72-121">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="c5f72-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5f72-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5f72-122">Requirements</span></span>



| <span data-ttu-id="c5f72-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5f72-123">Requirement</span></span> | <span data-ttu-id="c5f72-124">Value</span><span class="sxs-lookup"><span data-stu-id="c5f72-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5f72-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5f72-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c5f72-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c5f72-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c5f72-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5f72-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c5f72-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5f72-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c5f72-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c5f72-129">Namespace</span></span><br/>                | <span data-ttu-id="c5f72-130">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="c5f72-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c5f72-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c5f72-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5f72-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5f72-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5f72-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5f72-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5f72-134">**MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="c5f72-134">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="c5f72-135">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MINFOType**</span><span class="sxs-lookup"><span data-stu-id="c5f72-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c5f72-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c5f72-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





