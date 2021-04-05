---
title: MicrosoftDNS_MBType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de recursos de buzón (MB).
ms.assetid: b8f3b106-58f4-44b8-b2db-b00f1a495641
keywords:
- DNS de la clase MicrosoftDNS_MBType
- MicrosoftDNS_MBType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
- MicrosoftDNS_MBType.Modify
- MicrosoftDNS_MBType.MBHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ad6599ad058f65beba961f00c1bd6c43663487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996549"
---
# <a name="microsoftdns_mbtype-class"></a><span data-ttu-id="a95fd-105">MicrosoftDNS ( \_ clase MBType)</span><span class="sxs-lookup"><span data-stu-id="a95fd-105">MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="a95fd-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de recursos de buzón (MB).</span><span class="sxs-lookup"><span data-stu-id="a95fd-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox (MB) resource record.</span></span>

<span data-ttu-id="a95fd-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="a95fd-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a95fd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a95fd-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MBType : MicrosoftDNS_ResourceRecord
{
  string MBHost;
};
```

## <a name="members"></a><span data-ttu-id="a95fd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a95fd-109">Members</span></span>

<span data-ttu-id="a95fd-110">La clase **MicrosoftDNS \_ MBType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a95fd-110">The **MicrosoftDNS\_MBType** class has these types of members:</span></span>

-   [<span data-ttu-id="a95fd-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a95fd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a95fd-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a95fd-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a95fd-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a95fd-113">Methods</span></span>

<span data-ttu-id="a95fd-114">La clase **MicrosoftDNS \_ MBType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a95fd-114">The **MicrosoftDNS\_MBType** class has these methods.</span></span>



| <span data-ttu-id="a95fd-115">Método</span><span class="sxs-lookup"><span data-stu-id="a95fd-115">Method</span></span>                             | <span data-ttu-id="a95fd-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a95fd-116">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a95fd-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a95fd-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="a95fd-118">Crea una instancia de un RR de MB en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario del buzón, la clase (valor predeterminado = IN), el valor de período de vida y el host de buzón.</span><span class="sxs-lookup"><span data-stu-id="a95fd-118">Instantiates an MB RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox host.</span></span> <span data-ttu-id="a95fd-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="a95fd-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="a95fd-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="a95fd-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="a95fd-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="a95fd-121">**Modify**</span></span>                         | <span data-ttu-id="a95fd-122">Actualiza el host de TTL y MB a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="a95fd-122">Updates the TTL and MB host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="a95fd-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="a95fd-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="a95fd-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="a95fd-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="a95fd-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="a95fd-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="a95fd-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a95fd-126">Properties</span></span>

<span data-ttu-id="a95fd-127">La clase **MicrosoftDNS \_ MBType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a95fd-127">The **MicrosoftDNS\_MBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a95fd-128">**MBHost**</span><span class="sxs-lookup"><span data-stu-id="a95fd-128">**MBHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a95fd-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a95fd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a95fd-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a95fd-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a95fd-131">FQDN que especifica un host del buzón especificado en el nombre del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="a95fd-131">FQDN that specifies a host of the mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a95fd-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a95fd-132">Requirements</span></span>



| <span data-ttu-id="a95fd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a95fd-133">Requirement</span></span> | <span data-ttu-id="a95fd-134">Value</span><span class="sxs-lookup"><span data-stu-id="a95fd-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a95fd-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a95fd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a95fd-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a95fd-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a95fd-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a95fd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a95fd-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a95fd-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a95fd-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a95fd-139">Namespace</span></span><br/>                | <span data-ttu-id="a95fd-140">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="a95fd-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a95fd-141">MOF</span><span class="sxs-lookup"><span data-stu-id="a95fd-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a95fd-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a95fd-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a95fd-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="a95fd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a95fd-144">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MBType**</span><span class="sxs-lookup"><span data-stu-id="a95fd-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a95fd-145">**Método Modify de la \_ clase MicrosoftDNS MBType**</span><span class="sxs-lookup"><span data-stu-id="a95fd-145">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="a95fd-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="a95fd-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





