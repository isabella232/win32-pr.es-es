---
title: MicrosoftDNS_MRType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de cambio de nombre de buzón (MR).
ms.assetid: fa5da18f-121b-477b-8876-6e337382e9b8
keywords:
- DNS de la clase MicrosoftDNS_MRType
- MicrosoftDNS_MRType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
- MicrosoftDNS_MRType.Modify
- MicrosoftDNS_MRType.MRMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 732f0e6f51963f5ae810e4730406a94264fdde47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150811"
---
# <a name="microsoftdns_mrtype-class"></a><span data-ttu-id="d933f-105">MicrosoftDNS ( \_ clase MRType)</span><span class="sxs-lookup"><span data-stu-id="d933f-105">MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="d933f-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de cambio de nombre de buzón (MR).</span><span class="sxs-lookup"><span data-stu-id="d933f-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox Rename (MR) record.</span></span>

<span data-ttu-id="d933f-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="d933f-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d933f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d933f-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MRType : MicrosoftDNS_ResourceRecord
{
  string MRMailbox;
};
```

## <a name="members"></a><span data-ttu-id="d933f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d933f-109">Members</span></span>

<span data-ttu-id="d933f-110">La clase **MicrosoftDNS \_ MRType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d933f-110">The **MicrosoftDNS\_MRType** class has these types of members:</span></span>

-   [<span data-ttu-id="d933f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d933f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d933f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d933f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d933f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d933f-113">Methods</span></span>

<span data-ttu-id="d933f-114">La clase **MicrosoftDNS \_ MRType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d933f-114">The **MicrosoftDNS\_MRType** class has these methods.</span></span>



| <span data-ttu-id="d933f-115">Método</span><span class="sxs-lookup"><span data-stu-id="d933f-115">Method</span></span>                             | <span data-ttu-id="d933f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d933f-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d933f-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="d933f-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="d933f-118">Este método crea una instancia de un tipo ' MR ' de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario del buzón, la clase (valor predeterminado = IN), el valor de período de vida y el cambio de nombre del buzón.</span><span class="sxs-lookup"><span data-stu-id="d933f-118">This method instantiates an 'MR' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox rename.</span></span> <span data-ttu-id="d933f-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="d933f-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="d933f-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="d933f-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="d933f-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="d933f-121">**Modify**</span></span>                         | <span data-ttu-id="d933f-122">Este método actualiza el TTL y el buzón MR a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="d933f-122">This method updates the TTL and MR Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="d933f-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="d933f-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="d933f-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="d933f-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="d933f-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="d933f-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="d933f-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d933f-126">Properties</span></span>

<span data-ttu-id="d933f-127">La clase **MicrosoftDNS \_ MRType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d933f-127">The **MicrosoftDNS\_MRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d933f-128">**MRMailbox**</span><span class="sxs-lookup"><span data-stu-id="d933f-128">**MRMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d933f-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d933f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d933f-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d933f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d933f-131">FQDN que especifica un buzón que es el cambio de nombre adecuado del buzón especificado en el nombre del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="d933f-131">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d933f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d933f-132">Requirements</span></span>



| <span data-ttu-id="d933f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d933f-133">Requirement</span></span> | <span data-ttu-id="d933f-134">Value</span><span class="sxs-lookup"><span data-stu-id="d933f-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d933f-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d933f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d933f-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d933f-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d933f-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d933f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d933f-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d933f-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d933f-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d933f-139">Namespace</span></span><br/>                | <span data-ttu-id="d933f-140">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="d933f-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d933f-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d933f-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d933f-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d933f-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d933f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="d933f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d933f-144">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MRType**</span><span class="sxs-lookup"><span data-stu-id="d933f-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d933f-145">**Método Modify de la \_ clase MicrosoftDNS MRType**</span><span class="sxs-lookup"><span data-stu-id="d933f-145">**Modify Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="d933f-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d933f-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





