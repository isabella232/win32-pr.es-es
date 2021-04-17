---
title: Método GetObjectByTextRepresentation de la clase MicrosoftDNS_ResourceRecord
description: El método GetObjectByTextRepresentation recupera una instancia existente de la clase MicrosoftDNS \_ ResourceRecord.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- GetObjectByTextRepresentation el método DNS
- Método GetObjectByTextRepresentation DNS, clase MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord de clase DNS, método GetObjectByTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491170"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="5ec88-106">Método GetObjectByTextRepresentation de la \_ clase MicrosoftDNS ResourceRecord</span><span class="sxs-lookup"><span data-stu-id="5ec88-106">GetObjectByTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="5ec88-107">El método **GetObjectByTextRepresentation** recupera una instancia existente de la clase [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="5ec88-107">The **GetObjectByTextRepresentation** method retrieves an existing instance of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec88-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ec88-108">Syntax</span></span>


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a><span data-ttu-id="5ec88-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ec88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ec88-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5ec88-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec88-111">Nombre del servidor DNS desde el que se debe recuperar el RR.</span><span class="sxs-lookup"><span data-stu-id="5ec88-111">Name of the DNS Server from which the RR should be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="5ec88-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5ec88-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec88-113">Nombre del contenedor del que se debe obtener el RR.</span><span class="sxs-lookup"><span data-stu-id="5ec88-113">Name of the container from which the RR should be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="5ec88-114">*TextRepresentation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5ec88-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec88-115">Representación de texto del RR que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="5ec88-115">Text representation of the RR to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="5ec88-116">*RR* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5ec88-116">*RR* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec88-117">Referencia al RR con instancias.</span><span class="sxs-lookup"><span data-stu-id="5ec88-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ec88-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ec88-118">Return value</span></span>

<span data-ttu-id="5ec88-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5ec88-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ec88-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ec88-120">Requirements</span></span>



| <span data-ttu-id="5ec88-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ec88-121">Requirement</span></span> | <span data-ttu-id="5ec88-122">Value</span><span class="sxs-lookup"><span data-stu-id="5ec88-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec88-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ec88-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5ec88-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5ec88-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5ec88-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ec88-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5ec88-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5ec88-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5ec88-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5ec88-127">Namespace</span></span><br/>                | <span data-ttu-id="5ec88-128">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="5ec88-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5ec88-129">MOF</span><span class="sxs-lookup"><span data-stu-id="5ec88-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ec88-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ec88-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec88-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ec88-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec88-132">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="5ec88-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="5ec88-133">**Método CreateInstanceFromTextRepresentation de la \_ clase MicrosoftDNS ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="5ec88-133">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





