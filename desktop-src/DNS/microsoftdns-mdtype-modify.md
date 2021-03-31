---
title: Método Modify de la clase MicrosoftDNS_MDType
description: El método Modify actualiza un registro de recursos de agente de correo para el dominio (MD).
ms.assetid: d14c8ada-d715-489f-9956-a940b94006e5
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_MDType clase
- MicrosoftDNS_MDType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ed5e3a8d7f819447d256ba3bce31f4eaa6986a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150258"
---
# <a name="modify-method-of-the-microsoftdns_mdtype-class"></a><span data-ttu-id="c1b0b-106">Método Modify de la \_ clase MicrosoftDNS MDType</span><span class="sxs-lookup"><span data-stu-id="c1b0b-106">Modify method of the MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="c1b0b-107">El método **Modify** actualiza un registro de recursos de agente de correo para el dominio (MD).</span><span class="sxs-lookup"><span data-stu-id="c1b0b-107">The **Modify** method updates a Mail Agent for Domain (MD) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1b0b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1b0b-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c1b0b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1b0b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1b0b-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c1b0b-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1b0b-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="c1b0b-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c1b0b-112">*MDHost* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c1b0b-112">*MDHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1b0b-113">Cadena que representa el host de entrega de correo.</span><span class="sxs-lookup"><span data-stu-id="c1b0b-113">String representing the mail delivery host.</span></span>

</dd> <dt>

<span data-ttu-id="c1b0b-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c1b0b-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c1b0b-115">Referencia al objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="c1b0b-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1b0b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1b0b-116">Return value</span></span>

<span data-ttu-id="c1b0b-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c1b0b-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1b0b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1b0b-118">Remarks</span></span>

<span data-ttu-id="c1b0b-119">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="c1b0b-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b0b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1b0b-120">Requirements</span></span>



| <span data-ttu-id="c1b0b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1b0b-121">Requirement</span></span> | <span data-ttu-id="c1b0b-122">Value</span><span class="sxs-lookup"><span data-stu-id="c1b0b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b0b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1b0b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c1b0b-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c1b0b-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c1b0b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1b0b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c1b0b-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c1b0b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c1b0b-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c1b0b-127">Namespace</span></span><br/>                | <span data-ttu-id="c1b0b-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="c1b0b-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c1b0b-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c1b0b-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1b0b-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1b0b-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1b0b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1b0b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b0b-132">**MicrosoftDNS \_ MDType**</span><span class="sxs-lookup"><span data-stu-id="c1b0b-132">**MicrosoftDNS\_MDType**</span></span>](microsoftdns-mdtype.md)
</dt> <dt>

[<span data-ttu-id="c1b0b-133">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MDType**</span><span class="sxs-lookup"><span data-stu-id="c1b0b-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c1b0b-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c1b0b-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





