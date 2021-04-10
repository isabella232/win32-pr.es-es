---
title: Método Modify de la clase MicrosoftDNS_MGType
description: El método Modify actualiza un registro de recursos de grupo de correo (MG).
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_MGType clase
- MicrosoftDNS_MGType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706502569687a3c035c943e0a9dcc04aa1732492
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150638"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="e6c66-106">Método Modify de la \_ clase MicrosoftDNS MGType</span><span class="sxs-lookup"><span data-stu-id="e6c66-106">Modify method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="e6c66-107">El método **Modify** actualiza un registro de recursos de grupo de correo (mg).</span><span class="sxs-lookup"><span data-stu-id="e6c66-107">The **Modify** method updates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c66-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6c66-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="e6c66-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6c66-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6c66-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e6c66-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e6c66-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="e6c66-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="e6c66-112">*MGMailbox* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e6c66-112">*MGMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e6c66-113">FQDN que especifica un buzón que es miembro del grupo de correo especificado por el nombre del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="e6c66-113">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="e6c66-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e6c66-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e6c66-115">Referencia al objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="e6c66-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6c66-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6c66-116">Return value</span></span>

<span data-ttu-id="e6c66-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e6c66-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6c66-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6c66-118">Remarks</span></span>

<span data-ttu-id="e6c66-119">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="e6c66-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c66-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6c66-120">Requirements</span></span>



| <span data-ttu-id="e6c66-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6c66-121">Requirement</span></span> | <span data-ttu-id="e6c66-122">Value</span><span class="sxs-lookup"><span data-stu-id="e6c66-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c66-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6c66-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6c66-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e6c66-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e6c66-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6c66-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6c66-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e6c66-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e6c66-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e6c66-127">Namespace</span></span><br/>                | <span data-ttu-id="e6c66-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="e6c66-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e6c66-129">MOF</span><span class="sxs-lookup"><span data-stu-id="e6c66-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6c66-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6c66-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6c66-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6c66-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c66-132">**MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="e6c66-132">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="e6c66-133">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MGType**</span><span class="sxs-lookup"><span data-stu-id="e6c66-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e6c66-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="e6c66-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





