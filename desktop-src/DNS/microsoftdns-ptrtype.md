---
title: MicrosoftDNS_PTRType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de puntero (PTR).
ms.assetid: 2cb0f13b-e683-473b-9cdd-bc5d805b919d
keywords:
- DNS de la clase MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
- MicrosoftDNS_PTRType.Modify
- MicrosoftDNS_PTRType.PTRDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65dc434eb751ed925ab9efcdaf29f04741b749ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534336"
---
# <a name="microsoftdns_ptrtype-class"></a><span data-ttu-id="22402-105">MicrosoftDNS ( \_ clase PTRType)</span><span class="sxs-lookup"><span data-stu-id="22402-105">MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="22402-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de puntero (PTR).</span><span class="sxs-lookup"><span data-stu-id="22402-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Pointer (PTR) record.</span></span>

<span data-ttu-id="22402-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="22402-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="22402-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22402-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_PTRType : MicrosoftDNS_ResourceRecord
{
  string PTRDomainName;
};
```

## <a name="members"></a><span data-ttu-id="22402-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="22402-109">Members</span></span>

<span data-ttu-id="22402-110">La clase **MicrosoftDNS \_ PTRType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="22402-110">The **MicrosoftDNS\_PTRType** class has these types of members:</span></span>

-   [<span data-ttu-id="22402-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="22402-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="22402-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22402-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="22402-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="22402-113">Methods</span></span>

<span data-ttu-id="22402-114">La clase **MicrosoftDNS \_ PTRType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="22402-114">The **MicrosoftDNS\_PTRType** class has these methods.</span></span>



| <span data-ttu-id="22402-115">Método</span><span class="sxs-lookup"><span data-stu-id="22402-115">Method</span></span>                             | <span data-ttu-id="22402-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="22402-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22402-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="22402-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="22402-118">Crea una instancia de un registro de recursos de DNS PTR en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y el FQDN del registro PTR.</span><span class="sxs-lookup"><span data-stu-id="22402-118">Instantiates a DNS PTR Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the FQDN of the PTR record.</span></span> <span data-ttu-id="22402-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="22402-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="22402-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="22402-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="22402-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="22402-121">**Modify**</span></span>                         | <span data-ttu-id="22402-122">Actualiza el nombre de dominio TTL y PTR a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="22402-122">Updates the TTL and PTR Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="22402-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="22402-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="22402-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="22402-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="22402-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="22402-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="22402-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22402-126">Properties</span></span>

<span data-ttu-id="22402-127">La clase **MicrosoftDNS \_ PTRType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="22402-127">The **MicrosoftDNS\_PTRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22402-128">**PTRDomainName**</span><span class="sxs-lookup"><span data-stu-id="22402-128">**PTRDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22402-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22402-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22402-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22402-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22402-131">FQDN de los datos del registro PTR.</span><span class="sxs-lookup"><span data-stu-id="22402-131">FQDN of the PTR record data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22402-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22402-132">Requirements</span></span>



| <span data-ttu-id="22402-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="22402-133">Requirement</span></span> | <span data-ttu-id="22402-134">Value</span><span class="sxs-lookup"><span data-stu-id="22402-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22402-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22402-135">Minimum supported client</span></span><br/> | <span data-ttu-id="22402-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="22402-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="22402-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22402-137">Minimum supported server</span></span><br/> | <span data-ttu-id="22402-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="22402-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="22402-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="22402-139">Namespace</span></span><br/>                | <span data-ttu-id="22402-140">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="22402-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="22402-141">MOF</span><span class="sxs-lookup"><span data-stu-id="22402-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22402-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22402-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22402-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="22402-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22402-144">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS PTRType**</span><span class="sxs-lookup"><span data-stu-id="22402-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="22402-145">**Método Modify de la \_ clase MicrosoftDNS PTRType**</span><span class="sxs-lookup"><span data-stu-id="22402-145">**Modify Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="22402-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="22402-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





