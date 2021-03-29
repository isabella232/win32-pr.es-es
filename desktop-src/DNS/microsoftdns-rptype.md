---
title: MicrosoftDNS_RPType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de persona responsable (RP).
ms.assetid: 2b1c1bbc-a69f-4480-a7f2-6420240d4ad8
keywords:
- DNS de la clase MicrosoftDNS_RPType
- MicrosoftDNS_RPType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
- MicrosoftDNS_RPType.Modify
- MicrosoftDNS_RPType.RPMailbox
- MicrosoftDNS_RPType.TXTDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aae8686016d26cb9007b21a06c125d56ed5207f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905340"
---
# <a name="microsoftdns_rptype-class"></a><span data-ttu-id="fd501-105">MicrosoftDNS ( \_ clase RPType)</span><span class="sxs-lookup"><span data-stu-id="fd501-105">MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="fd501-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de persona responsable (RP).</span><span class="sxs-lookup"><span data-stu-id="fd501-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Responsible Person (RP) record.</span></span>

<span data-ttu-id="fd501-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="fd501-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd501-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd501-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RPType : MicrosoftDNS_ResourceRecord
{
  string RPMailbox;
  string TXTDomainName;
};
```

## <a name="members"></a><span data-ttu-id="fd501-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd501-109">Members</span></span>

<span data-ttu-id="fd501-110">La clase **MicrosoftDNS \_ RPType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fd501-110">The **MicrosoftDNS\_RPType** class has these types of members:</span></span>

-   [<span data-ttu-id="fd501-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="fd501-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fd501-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd501-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fd501-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="fd501-113">Methods</span></span>

<span data-ttu-id="fd501-114">La clase **MicrosoftDNS \_ RPType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fd501-114">The **MicrosoftDNS\_RPType** class has these methods.</span></span>



| <span data-ttu-id="fd501-115">Método</span><span class="sxs-lookup"><span data-stu-id="fd501-115">Method</span></span>                             | <span data-ttu-id="fd501-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd501-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd501-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="fd501-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="fd501-118">Crea una instancia de un tipo RP de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el propietario o el nombre de la persona responsable, la clase (valor predeterminado = IN), el valor de período de vida y los nombres de dominio de las ubicaciones de RR de TXT y el buzón de la persona.</span><span class="sxs-lookup"><span data-stu-id="fd501-118">Instantiates an RP Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/responsible person Name, class (default = IN), time-to-live value and the domain names for the person's mailbox and TXT RR locations.</span></span> <span data-ttu-id="fd501-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="fd501-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="fd501-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="fd501-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="fd501-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="fd501-121">**Modify**</span></span>                         | <span data-ttu-id="fd501-122">Este método actualiza el nombre de dominio TTL, el buzón RP y el nombre de dominio TXT a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="fd501-122">This method updates the TTL, RP Mailbox and TXT Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="fd501-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="fd501-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="fd501-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="fd501-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="fd501-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="fd501-125">Qualifiers: Implemented</span></span><br/>                                  |



 

### <a name="properties"></a><span data-ttu-id="fd501-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd501-126">Properties</span></span>

<span data-ttu-id="fd501-127">La clase **MicrosoftDNS \_ RPType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fd501-127">The **MicrosoftDNS\_RPType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd501-128">**RPMailbox**</span><span class="sxs-lookup"><span data-stu-id="fd501-128">**RPMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd501-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd501-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd501-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd501-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd501-131">FQDN que especifica el buzón de correo para la persona responsable.</span><span class="sxs-lookup"><span data-stu-id="fd501-131">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="fd501-132">**TXTDomainName**</span><span class="sxs-lookup"><span data-stu-id="fd501-132">**TXTDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd501-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd501-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd501-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd501-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd501-135">FQDN para el que existen registros de recursos TXT.</span><span class="sxs-lookup"><span data-stu-id="fd501-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd501-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd501-136">Requirements</span></span>



| <span data-ttu-id="fd501-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd501-137">Requirement</span></span> | <span data-ttu-id="fd501-138">Value</span><span class="sxs-lookup"><span data-stu-id="fd501-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd501-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd501-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fd501-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fd501-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fd501-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd501-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fd501-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd501-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fd501-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fd501-143">Namespace</span></span><br/>                | <span data-ttu-id="fd501-144">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="fd501-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fd501-145">MOF</span><span class="sxs-lookup"><span data-stu-id="fd501-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd501-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd501-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd501-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd501-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd501-148">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS RPType**</span><span class="sxs-lookup"><span data-stu-id="fd501-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fd501-149">**Método Modify de la \_ clase MicrosoftDNS RPType**</span><span class="sxs-lookup"><span data-stu-id="fd501-149">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="fd501-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="fd501-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





