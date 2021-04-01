---
title: MicrosoftDNS_RootHints (clase)
description: La \_ clase MicrosoftDNS RootHints describe el RootHints almacenado en un archivo caché en un servidor DNS. Esta clase simplifica la visualización de la contención de objetos DNS, en lugar de representar un objeto real.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- DNS de la clase MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150445"
---
# <a name="microsoftdns_roothints-class"></a><span data-ttu-id="48d15-106">MicrosoftDNS ( \_ clase RootHints)</span><span class="sxs-lookup"><span data-stu-id="48d15-106">MicrosoftDNS\_RootHints class</span></span>

<span data-ttu-id="48d15-107">La clase **MicrosoftDNS \_ RootHints** describe el RootHints almacenado en un archivo caché en un servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="48d15-107">The **MicrosoftDNS\_RootHints** class describes the RootHints stored in a Cache file on a DNS Server.</span></span> <span data-ttu-id="48d15-108">Esta clase simplifica la visualización de la contención de objetos DNS, en lugar de representar un objeto real.</span><span class="sxs-lookup"><span data-stu-id="48d15-108">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span>

<span data-ttu-id="48d15-109">**MicrosoftDNS \_ RootHints** es un contenedor para los registros de recursos almacenados por el servidor DNS en un archivo caché.</span><span class="sxs-lookup"><span data-stu-id="48d15-109">**MicrosoftDNS\_RootHints** is a container for the resource records stored by the DNS Server in a Cache file.</span></span> <span data-ttu-id="48d15-110">Cada instancia de la clase **MicrosoftDNS \_ RootHints** debe estar asignada exactamente a un servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="48d15-110">Every instance of the **MicrosoftDNS\_RootHints** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="48d15-111">Puede estar asociado a varias instancias de la clase [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="48d15-111">It may be associated with multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

<span data-ttu-id="48d15-112">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="48d15-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="48d15-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48d15-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="48d15-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="48d15-114">Members</span></span>

<span data-ttu-id="48d15-115">La clase **MicrosoftDNS \_ RootHints** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="48d15-115">The **MicrosoftDNS\_RootHints** class has these types of members:</span></span>

-   [<span data-ttu-id="48d15-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="48d15-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="48d15-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="48d15-117">Methods</span></span>

<span data-ttu-id="48d15-118">La clase **MicrosoftDNS \_ RootHints** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="48d15-118">The **MicrosoftDNS\_RootHints** class has these methods.</span></span>



| <span data-ttu-id="48d15-119">Método</span><span class="sxs-lookup"><span data-stu-id="48d15-119">Method</span></span>                        | <span data-ttu-id="48d15-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="48d15-120">Description</span></span>                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d15-121">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="48d15-121">**GetDistinguishedName**</span></span>      | <span data-ttu-id="48d15-122">Recupera el nombre distintivo de la zona.</span><span class="sxs-lookup"><span data-stu-id="48d15-122">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="48d15-123">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="48d15-123">Qualifiers: Implemented</span></span><br/>   |
| <span data-ttu-id="48d15-124">**WriteBackRootHintDatafile**</span><span class="sxs-lookup"><span data-stu-id="48d15-124">**WriteBackRootHintDatafile**</span></span> | <span data-ttu-id="48d15-125">Vuelve a escribir RootHints en el archivo de caché DNS.</span><span class="sxs-lookup"><span data-stu-id="48d15-125">Writes the RootHints back to the DNS Cache file.</span></span> <br/> <span data-ttu-id="48d15-126">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="48d15-126">Qualifiers: Implemented</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="48d15-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48d15-127">Requirements</span></span>



| <span data-ttu-id="48d15-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="48d15-128">Requirement</span></span> | <span data-ttu-id="48d15-129">Value</span><span class="sxs-lookup"><span data-stu-id="48d15-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48d15-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48d15-130">Minimum supported client</span></span><br/> | <span data-ttu-id="48d15-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="48d15-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="48d15-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48d15-132">Minimum supported server</span></span><br/> | <span data-ttu-id="48d15-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="48d15-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="48d15-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="48d15-134">Namespace</span></span><br/>                | <span data-ttu-id="48d15-135">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="48d15-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="48d15-136">MOF</span><span class="sxs-lookup"><span data-stu-id="48d15-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48d15-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48d15-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48d15-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="48d15-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48d15-139">**\_Dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="48d15-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="48d15-140">**Método WriteBackRootHintDatafile de la \_ clase MicrosoftDNS RootHints**</span><span class="sxs-lookup"><span data-stu-id="48d15-140">**WriteBackRootHintDatafile Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[<span data-ttu-id="48d15-141">**Método GetDistinguishedName de la \_ clase MicrosoftDNS RootHints**</span><span class="sxs-lookup"><span data-stu-id="48d15-141">**GetDistinguishedName Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





