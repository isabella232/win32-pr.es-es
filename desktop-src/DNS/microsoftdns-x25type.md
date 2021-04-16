---
title: MicrosoftDNS_X25Type (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro X. 25 (x25).
ms.assetid: 1213dfd7-30b3-413e-b723-f4284fa0b416
keywords:
- DNS de la clase MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
- MicrosoftDNS_X25Type.Modify
- MicrosoftDNS_X25Type.PSDNAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584119dbd45d5d6c7fae347c506c42fcda4fff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658247"
---
# <a name="microsoftdns_x25type-class"></a><span data-ttu-id="ddbe8-105">MicrosoftDNS ( \_ clase X25Type)</span><span class="sxs-lookup"><span data-stu-id="ddbe8-105">MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="ddbe8-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro X. 25 (x25).</span><span class="sxs-lookup"><span data-stu-id="ddbe8-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an X.25 (X25) record.</span></span>

<span data-ttu-id="ddbe8-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="ddbe8-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddbe8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddbe8-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_X25Type : MicrosoftDNS_ResourceRecord
{
  string PSDNAddress;
};
```

## <a name="members"></a><span data-ttu-id="ddbe8-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="ddbe8-109">Members</span></span>

<span data-ttu-id="ddbe8-110">La clase **MicrosoftDNS \_ X25Type** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ddbe8-110">The **MicrosoftDNS\_X25Type** class has these types of members:</span></span>

-   [<span data-ttu-id="ddbe8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ddbe8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ddbe8-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ddbe8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ddbe8-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ddbe8-113">Methods</span></span>

<span data-ttu-id="ddbe8-114">La clase **MicrosoftDNS \_ X25Type** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ddbe8-114">The **MicrosoftDNS\_X25Type** class has these methods.</span></span>



| <span data-ttu-id="ddbe8-115">Método</span><span class="sxs-lookup"><span data-stu-id="ddbe8-115">Method</span></span>                             | <span data-ttu-id="ddbe8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddbe8-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddbe8-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ddbe8-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ddbe8-118">Crea una instancia de un tipo ' x25 ' de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y la dirección PSDN.</span><span class="sxs-lookup"><span data-stu-id="ddbe8-118">Instantiates an 'X25' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the PSDN address.</span></span> <span data-ttu-id="ddbe8-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="ddbe8-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ddbe8-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="ddbe8-120">Qualifiers: Implemented, static</span></span><br/>              |
| <span data-ttu-id="ddbe8-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="ddbe8-121">**Modify**</span></span>                         | <span data-ttu-id="ddbe8-122">Este método actualiza el TTL y la dirección PSDN a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="ddbe8-122">This method updates the TTL and PSDN Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ddbe8-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="ddbe8-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ddbe8-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="ddbe8-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ddbe8-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ddbe8-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ddbe8-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ddbe8-126">Properties</span></span>

<span data-ttu-id="ddbe8-127">La clase **MicrosoftDNS \_ X25Type** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ddbe8-127">The **MicrosoftDNS\_X25Type** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddbe8-128">**PSDNAddress**</span><span class="sxs-lookup"><span data-stu-id="ddbe8-128">**PSDNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddbe8-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddbe8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddbe8-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddbe8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddbe8-131">Dirección PSDN del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="ddbe8-131">PSDN address of the owner of the RR.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ddbe8-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddbe8-132">Requirements</span></span>



| <span data-ttu-id="ddbe8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddbe8-133">Requirement</span></span> | <span data-ttu-id="ddbe8-134">Value</span><span class="sxs-lookup"><span data-stu-id="ddbe8-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddbe8-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddbe8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ddbe8-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ddbe8-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ddbe8-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddbe8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ddbe8-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ddbe8-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ddbe8-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ddbe8-139">Namespace</span></span><br/>                | <span data-ttu-id="ddbe8-140">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="ddbe8-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ddbe8-141">MOF</span><span class="sxs-lookup"><span data-stu-id="ddbe8-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddbe8-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddbe8-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddbe8-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddbe8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddbe8-144">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS X25Type**</span><span class="sxs-lookup"><span data-stu-id="ddbe8-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ddbe8-145">**Método Modify de la \_ clase MicrosoftDNS X25Type**</span><span class="sxs-lookup"><span data-stu-id="ddbe8-145">**Modify Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-modify.md)
</dt> <dt>

[<span data-ttu-id="ddbe8-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ddbe8-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





