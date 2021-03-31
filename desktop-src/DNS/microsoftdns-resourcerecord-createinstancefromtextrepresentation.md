---
title: Método CreateInstanceFromTextRepresentation de la clase MicrosoftDNS_ResourceRecord
description: El método CreateInstanceFromTextRepresentation crea una instancia de un \_ objeto MicrosoftDNS ResourceRecord.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- CreateInstanceFromTextRepresentation el método DNS
- Método CreateInstanceFromTextRepresentation DNS, clase MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord de clase DNS, método CreateInstanceFromTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a578d036180ecb1dc8a5e66bf853eec8845583f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079481"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="7dbb9-106">Método CreateInstanceFromTextRepresentation de la \_ clase MicrosoftDNS ResourceRecord</span><span class="sxs-lookup"><span data-stu-id="7dbb9-106">CreateInstanceFromTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="7dbb9-107">El método **CreateInstanceFromTextRepresentation** crea una instancia de un objeto [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="7dbb9-107">The **CreateInstanceFromTextRepresentation** method instantiates a [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dbb9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7dbb9-108">Syntax</span></span>


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a><span data-ttu-id="7dbb9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7dbb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dbb9-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7dbb9-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dbb9-111">Nombre del servidor DNS en el que se debe crear el RR.</span><span class="sxs-lookup"><span data-stu-id="7dbb9-111">Name of the DNS Server on which the RR should be created.</span></span>

</dd> <dt>

<span data-ttu-id="7dbb9-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7dbb9-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dbb9-113">Nombre del contenedor en el que se debe colocar el nuevo RR.</span><span class="sxs-lookup"><span data-stu-id="7dbb9-113">Name of the container into which the new RR should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="7dbb9-114">*TextRepresentation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7dbb9-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dbb9-115">Representación de texto de la instancia de RR que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="7dbb9-115">Text representation of the RR instance to be created.</span></span>

</dd> <dt>

<span data-ttu-id="7dbb9-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="7dbb9-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7dbb9-117">Referencia al RR con instancias.</span><span class="sxs-lookup"><span data-stu-id="7dbb9-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dbb9-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7dbb9-118">Return value</span></span>

<span data-ttu-id="7dbb9-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7dbb9-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dbb9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dbb9-120">Requirements</span></span>



| <span data-ttu-id="7dbb9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dbb9-121">Requirement</span></span> | <span data-ttu-id="7dbb9-122">Value</span><span class="sxs-lookup"><span data-stu-id="7dbb9-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7dbb9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7dbb9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7dbb9-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7dbb9-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7dbb9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7dbb9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7dbb9-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7dbb9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7dbb9-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7dbb9-127">Namespace</span></span><br/>                | <span data-ttu-id="7dbb9-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="7dbb9-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="7dbb9-129">MOF</span><span class="sxs-lookup"><span data-stu-id="7dbb9-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7dbb9-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7dbb9-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dbb9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7dbb9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dbb9-132">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="7dbb9-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="7dbb9-133">**Método GetObjectByTextRepresentation de la \_ clase MicrosoftDNS ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="7dbb9-133">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





