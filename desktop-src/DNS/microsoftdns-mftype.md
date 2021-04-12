---
title: MicrosoftDNS_MFType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro del agente de reenvío de correo para el dominio (MF).
ms.assetid: 0ba0fddd-c316-4a5b-ad65-6344dbe949c1
keywords:
- DNS de la clase MicrosoftDNS_MFType
- MicrosoftDNS_MFType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
- MicrosoftDNS_MFType.Modify
- MicrosoftDNS_MFType.MFHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e030f695e95ee736b1c53a345201e0bd1addfe3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150639"
---
# <a name="microsoftdns_mftype-class"></a><span data-ttu-id="25745-105">MicrosoftDNS ( \_ clase MFType)</span><span class="sxs-lookup"><span data-stu-id="25745-105">MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="25745-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro del agente de reenvío de correo para el dominio (MF).</span><span class="sxs-lookup"><span data-stu-id="25745-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Forwarding Agent for Domain (MF) record.</span></span>

<span data-ttu-id="25745-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="25745-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="25745-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25745-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MFType : MicrosoftDNS_ResourceRecord
{
  string MFHost;
};
```

## <a name="members"></a><span data-ttu-id="25745-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="25745-109">Members</span></span>

<span data-ttu-id="25745-110">La clase **MicrosoftDNS \_ MFType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="25745-110">The **MicrosoftDNS\_MFType** class has these types of members:</span></span>

-   [<span data-ttu-id="25745-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="25745-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="25745-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25745-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="25745-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="25745-113">Methods</span></span>

<span data-ttu-id="25745-114">La clase **MicrosoftDNS \_ MFType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="25745-114">The **MicrosoftDNS\_MFType** class has these methods.</span></span>



| <span data-ttu-id="25745-115">Método</span><span class="sxs-lookup"><span data-stu-id="25745-115">Method</span></span>                             | <span data-ttu-id="25745-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="25745-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25745-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="25745-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="25745-118">Este método crea una instancia de un tipo MF de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario del dominio, la clase (valor predeterminado = IN), el valor de período de vida y el host del agente de correo.</span><span class="sxs-lookup"><span data-stu-id="25745-118">This method instantiates an MF Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="25745-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="25745-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="25745-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="25745-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="25745-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="25745-121">**Modify**</span></span>                         | <span data-ttu-id="25745-122">Este método actualiza el host de TTL y MF a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="25745-122">This method updates the TTL and MF Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="25745-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="25745-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="25745-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="25745-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="25745-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="25745-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="25745-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25745-126">Properties</span></span>

<span data-ttu-id="25745-127">La clase **MicrosoftDNS \_ MFType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="25745-127">The **MicrosoftDNS\_MFType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25745-128">**MFHost**</span><span class="sxs-lookup"><span data-stu-id="25745-128">**MFHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25745-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25745-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25745-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25745-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25745-131">FQDN que especifica un host con un agente de correo que aceptará correo para el reenvío al dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="25745-131">FQDN specifying a host with a mail agent that will accept mail for forwarding to the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25745-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25745-132">Requirements</span></span>



| <span data-ttu-id="25745-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="25745-133">Requirement</span></span> | <span data-ttu-id="25745-134">Value</span><span class="sxs-lookup"><span data-stu-id="25745-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25745-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25745-135">Minimum supported client</span></span><br/> | <span data-ttu-id="25745-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="25745-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="25745-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25745-137">Minimum supported server</span></span><br/> | <span data-ttu-id="25745-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="25745-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="25745-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25745-139">Namespace</span></span><br/>                | <span data-ttu-id="25745-140">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="25745-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="25745-141">MOF</span><span class="sxs-lookup"><span data-stu-id="25745-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25745-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25745-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25745-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="25745-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25745-144">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MFType**</span><span class="sxs-lookup"><span data-stu-id="25745-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="25745-145">**Método Modify de la \_ clase MicrosoftDNS MFType**</span><span class="sxs-lookup"><span data-stu-id="25745-145">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="25745-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="25745-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





