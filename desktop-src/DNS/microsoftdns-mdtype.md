---
title: MicrosoftDNS_MDType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro del agente de correo para el dominio (MD).
ms.assetid: 11242372-65fe-44ee-845b-2430aec59127
keywords:
- DNS de la clase MicrosoftDNS_MDType
- MicrosoftDNS_MDType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
- MicrosoftDNS_MDType.Modify
- MicrosoftDNS_MDType.MDHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7641fda7a223fed7c2dc9229c5a3449c575e84ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905226"
---
# <a name="microsoftdns_mdtype-class"></a><span data-ttu-id="d4981-105">MicrosoftDNS ( \_ clase MDType)</span><span class="sxs-lookup"><span data-stu-id="d4981-105">MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="d4981-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro del agente de correo para el dominio (MD).</span><span class="sxs-lookup"><span data-stu-id="d4981-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Agent for Domain (MD) record.</span></span>

<span data-ttu-id="d4981-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="d4981-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4981-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4981-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MDType : MicrosoftDNS_ResourceRecord
{
  string MDHost;
};
```

## <a name="members"></a><span data-ttu-id="d4981-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d4981-109">Members</span></span>

<span data-ttu-id="d4981-110">La clase **MicrosoftDNS \_ MDType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d4981-110">The **MicrosoftDNS\_MDType** class has these types of members:</span></span>

-   [<span data-ttu-id="d4981-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d4981-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d4981-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4981-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d4981-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d4981-113">Methods</span></span>

<span data-ttu-id="d4981-114">La clase **MicrosoftDNS \_ MDType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d4981-114">The **MicrosoftDNS\_MDType** class has these methods.</span></span>



| <span data-ttu-id="d4981-115">Método</span><span class="sxs-lookup"><span data-stu-id="d4981-115">Method</span></span>                             | <span data-ttu-id="d4981-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4981-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4981-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="d4981-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="d4981-118">Crea una instancia de un registro de recursos de DNS MD en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario del dominio, la clase (valor predeterminado = IN), el valor de período de vida y el host del agente de correo.</span><span class="sxs-lookup"><span data-stu-id="d4981-118">Instantiates a DNS MD Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="d4981-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="d4981-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="d4981-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="d4981-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="d4981-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="d4981-121">**Modify**</span></span>                         | <span data-ttu-id="d4981-122">Actualiza el host TTL y MD a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="d4981-122">Updates the TTL and MD host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="d4981-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="d4981-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="d4981-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="d4981-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="d4981-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="d4981-125">Qualifiers: Implemented</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="d4981-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4981-126">Properties</span></span>

<span data-ttu-id="d4981-127">La clase **MicrosoftDNS \_ MDType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d4981-127">The **MicrosoftDNS\_MDType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4981-128">**MDHost**</span><span class="sxs-lookup"><span data-stu-id="d4981-128">**MDHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4981-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d4981-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4981-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4981-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4981-131">FQDN que especifica un host con un agente de correo capaz de entregar correo para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="d4981-131">FQDN that specifies a host with a mail agent capable of delivering mail for the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4981-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4981-132">Requirements</span></span>



| <span data-ttu-id="d4981-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4981-133">Requirement</span></span> | <span data-ttu-id="d4981-134">Value</span><span class="sxs-lookup"><span data-stu-id="d4981-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4981-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4981-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d4981-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d4981-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d4981-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4981-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d4981-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d4981-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d4981-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d4981-139">Namespace</span></span><br/>                | <span data-ttu-id="d4981-140">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="d4981-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d4981-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d4981-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4981-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4981-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4981-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4981-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4981-144">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MDType**</span><span class="sxs-lookup"><span data-stu-id="d4981-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d4981-145">**Método Modify de la \_ clase MicrosoftDNS MDType**</span><span class="sxs-lookup"><span data-stu-id="d4981-145">**Modify Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-modify.md)
</dt> <dt>

[<span data-ttu-id="d4981-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d4981-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





