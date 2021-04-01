---
title: Método Modify de la clase MicrosoftDNS_MXType
description: El método Modify actualiza un registro de recursos de intercambio de correo (MR).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_MXType clase
- MicrosoftDNS_MXType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a665d0673e048eff684b4c985b54a1c57e030a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997067"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="8a382-106">Método Modify de la \_ clase MicrosoftDNS MXType</span><span class="sxs-lookup"><span data-stu-id="8a382-106">Modify method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="8a382-107">El método **Modify** actualiza un registro de recursos de intercambio de correo (MR).</span><span class="sxs-lookup"><span data-stu-id="8a382-107">The **Modify** method updates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a382-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a382-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8a382-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a382-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a382-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8a382-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a382-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="8a382-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8a382-112">*Preferencia* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8a382-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a382-113">Preferencia asignada a este RR entre otros en el mismo propietario.</span><span class="sxs-lookup"><span data-stu-id="8a382-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="8a382-114">Se prefieren los valores inferiores.</span><span class="sxs-lookup"><span data-stu-id="8a382-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="8a382-115">*MailExchange* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8a382-115">*MailExchange* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a382-116">FQDN que especifica un host que desea actuar como intercambio de correo electrónico para el nombre del propietario.</span><span class="sxs-lookup"><span data-stu-id="8a382-116">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="8a382-117">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="8a382-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8a382-118">Referencia al objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="8a382-118">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a382-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a382-119">Return value</span></span>

<span data-ttu-id="8a382-120">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8a382-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a382-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a382-121">Remarks</span></span>

<span data-ttu-id="8a382-122">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="8a382-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a382-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a382-123">Requirements</span></span>



| <span data-ttu-id="8a382-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a382-124">Requirement</span></span> | <span data-ttu-id="8a382-125">Value</span><span class="sxs-lookup"><span data-stu-id="8a382-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a382-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a382-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8a382-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8a382-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8a382-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a382-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8a382-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a382-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8a382-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8a382-130">Namespace</span></span><br/>                | <span data-ttu-id="8a382-131">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="8a382-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8a382-132">MOF</span><span class="sxs-lookup"><span data-stu-id="8a382-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a382-133"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a382-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a382-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a382-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a382-135">**MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="8a382-135">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="8a382-136">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MXType**</span><span class="sxs-lookup"><span data-stu-id="8a382-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="8a382-137">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="8a382-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





