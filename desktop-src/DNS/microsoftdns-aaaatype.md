---
title: MicrosoftDNS_AAAAType (clase)
description: Subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de dirección IPv6 (aaaa). El registro AAAA se pronuncia normalmente \ 0034; un registro de cuatro a 0034.
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- DNS de la clase MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType.Modify
- MicrosoftDNS_AAAAType.IPv6Address
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0131177c342730c08868946c29356554cbfb9cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658181"
---
# <a name="microsoftdns_aaaatype-class"></a><span data-ttu-id="99fa3-106">MicrosoftDNS ( \_ clase AAAAType)</span><span class="sxs-lookup"><span data-stu-id="99fa3-106">MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="99fa3-107">Subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de dirección IPv6 (aaaa).</span><span class="sxs-lookup"><span data-stu-id="99fa3-107">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an IPv6 Address (AAAA) record.</span></span> <span data-ttu-id="99fa3-108">El registro AAAA se pronuncia normalmente como "registro cuádruple-a".</span><span class="sxs-lookup"><span data-stu-id="99fa3-108">The AAAA record is commonly pronounced "quad-a record".</span></span>

<span data-ttu-id="99fa3-109">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="99fa3-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="99fa3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99fa3-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a><span data-ttu-id="99fa3-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="99fa3-111">Members</span></span>

<span data-ttu-id="99fa3-112">La clase **MicrosoftDNS \_ AAAAType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="99fa3-112">The **MicrosoftDNS\_AAAAType** class has these types of members:</span></span>

-   [<span data-ttu-id="99fa3-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="99fa3-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="99fa3-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="99fa3-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="99fa3-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="99fa3-115">Methods</span></span>

<span data-ttu-id="99fa3-116">La clase **MicrosoftDNS \_ AAAAType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="99fa3-116">The **MicrosoftDNS\_AAAAType** class has these methods.</span></span>



| <span data-ttu-id="99fa3-117">Método</span><span class="sxs-lookup"><span data-stu-id="99fa3-117">Method</span></span>                             | <span data-ttu-id="99fa3-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="99fa3-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99fa3-119">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="99fa3-119">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="99fa3-120">Crea una instancia de un tipo ' AAAA ' de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el propietario o el nombre de host, la clase (valor predeterminado = IN), el valor de período de vida y la dirección IPv6.</span><span class="sxs-lookup"><span data-stu-id="99fa3-120">Instantiates an 'AAAA' type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Host Name, class (default = IN), time-to-live value, and the IPv6 address.</span></span> <span data-ttu-id="99fa3-121">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="99fa3-121">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="99fa3-122">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="99fa3-122">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="99fa3-123">**Modify**</span><span class="sxs-lookup"><span data-stu-id="99fa3-123">**Modify**</span></span>                         | <span data-ttu-id="99fa3-124">Actualiza el TTL y la dirección IPv6 a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="99fa3-124">Updates the TTL and IPv6 address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="99fa3-125">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="99fa3-125">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="99fa3-126">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="99fa3-126">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="99fa3-127">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="99fa3-127">Qualifiers: Implemented</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="99fa3-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="99fa3-128">Properties</span></span>

<span data-ttu-id="99fa3-129">La clase **MicrosoftDNS \_ AAAAType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="99fa3-129">The **MicrosoftDNS\_AAAAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99fa3-130">**IPv6Address**</span><span class="sxs-lookup"><span data-stu-id="99fa3-130">**IPv6Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99fa3-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="99fa3-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99fa3-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="99fa3-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="99fa3-133">Dirección IPv6 para el host.</span><span class="sxs-lookup"><span data-stu-id="99fa3-133">IPv6 address for the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99fa3-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99fa3-134">Requirements</span></span>



| <span data-ttu-id="99fa3-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="99fa3-135">Requirement</span></span> | <span data-ttu-id="99fa3-136">Value</span><span class="sxs-lookup"><span data-stu-id="99fa3-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99fa3-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99fa3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="99fa3-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="99fa3-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="99fa3-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99fa3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="99fa3-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="99fa3-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="99fa3-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="99fa3-141">Namespace</span></span><br/>                | <span data-ttu-id="99fa3-142">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="99fa3-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="99fa3-143">MOF</span><span class="sxs-lookup"><span data-stu-id="99fa3-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99fa3-144"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99fa3-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99fa3-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="99fa3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99fa3-146">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS AAAAType**</span><span class="sxs-lookup"><span data-stu-id="99fa3-146">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="99fa3-147">**Método Modify de la \_ clase MicrosoftDNS AAAAType**</span><span class="sxs-lookup"><span data-stu-id="99fa3-147">**Modify Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[<span data-ttu-id="99fa3-148">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="99fa3-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





