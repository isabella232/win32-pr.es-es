---
title: Método Modify de la clase MicrosoftDNS_RPType
description: El método Modify actualiza un registro de recursos de persona responsable (RP).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_RPType clase
- MicrosoftDNS_RPType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ec575424e6e26c79f8d6a27e62732cad6ddc57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905341"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="2aa51-106">Método Modify de la \_ clase MicrosoftDNS RPType</span><span class="sxs-lookup"><span data-stu-id="2aa51-106">Modify method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="2aa51-107">El método **Modify** actualiza un registro de recursos de persona responsable (RP).</span><span class="sxs-lookup"><span data-stu-id="2aa51-107">The **Modify** method updates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aa51-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2aa51-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="2aa51-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2aa51-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aa51-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2aa51-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa51-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="2aa51-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="2aa51-112">*RPMailbox* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2aa51-112">*RPMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa51-113">FQDN que especifica el buzón de correo para la persona responsable.</span><span class="sxs-lookup"><span data-stu-id="2aa51-113">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="2aa51-114">*TXTDomainName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2aa51-114">*TXTDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa51-115">FQDN para el que existen registros de recursos TXT.</span><span class="sxs-lookup"><span data-stu-id="2aa51-115">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="2aa51-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="2aa51-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa51-117">Referencia al objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="2aa51-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aa51-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2aa51-118">Return value</span></span>

<span data-ttu-id="2aa51-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2aa51-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aa51-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2aa51-120">Remarks</span></span>

<span data-ttu-id="2aa51-121">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="2aa51-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aa51-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2aa51-122">Requirements</span></span>



| <span data-ttu-id="2aa51-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2aa51-123">Requirement</span></span> | <span data-ttu-id="2aa51-124">Value</span><span class="sxs-lookup"><span data-stu-id="2aa51-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa51-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2aa51-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2aa51-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2aa51-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2aa51-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2aa51-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2aa51-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2aa51-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2aa51-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2aa51-129">Namespace</span></span><br/>                | <span data-ttu-id="2aa51-130">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="2aa51-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2aa51-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2aa51-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2aa51-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2aa51-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aa51-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2aa51-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aa51-134">**MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="2aa51-134">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="2aa51-135">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS RPType**</span><span class="sxs-lookup"><span data-stu-id="2aa51-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="2aa51-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="2aa51-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





