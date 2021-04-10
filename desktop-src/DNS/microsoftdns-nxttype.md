---
title: MicrosoftDNS_NXTType (clase)
description: Subclase de MicrosoftDNS \_ ResourceRecord que representa un RR siguiente (NXT).
ms.assetid: bb24509e-083b-4432-89e3-501167f12299
keywords:
- DNS de la clase MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_NXTType.Modify
- MicrosoftDNS_NXTType.NextDomainName
- MicrosoftDNS_NXTType.Types
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79db82b3ae760c31d4e6fef80eb01469cb2bb41d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150447"
---
# <a name="microsoftdns_nxttype-class"></a><span data-ttu-id="94e61-105">MicrosoftDNS ( \_ clase NXTType)</span><span class="sxs-lookup"><span data-stu-id="94e61-105">MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="94e61-106">Subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un RR siguiente (NXT).</span><span class="sxs-lookup"><span data-stu-id="94e61-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Next (NXT) RR.</span></span>

<span data-ttu-id="94e61-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="94e61-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e61-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94e61-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_NXTType : MicrosoftDNS_ResourceRecord
{
  string NextDomainName;
  string Types;
};
```

## <a name="members"></a><span data-ttu-id="94e61-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="94e61-109">Members</span></span>

<span data-ttu-id="94e61-110">La clase **MicrosoftDNS \_ NXTType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="94e61-110">The **MicrosoftDNS\_NXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="94e61-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="94e61-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="94e61-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94e61-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="94e61-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="94e61-113">Methods</span></span>

<span data-ttu-id="94e61-114">La clase **MicrosoftDNS \_ NXTType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="94e61-114">The **MicrosoftDNS\_NXTType** class has these methods.</span></span>



| <span data-ttu-id="94e61-115">Método</span><span class="sxs-lookup"><span data-stu-id="94e61-115">Method</span></span>                             | <span data-ttu-id="94e61-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="94e61-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94e61-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="94e61-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="94e61-118">Crea una instancia de un registro de recursos NXT en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y el marcador de asignación WINS, el tiempo de espera de búsqueda inversa, el tiempo de espera de caché WINS y el nombre</span><span class="sxs-lookup"><span data-stu-id="94e61-118">Instantiates an NXT Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out, and domain name to append.</span></span> <span data-ttu-id="94e61-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="94e61-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="94e61-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="94e61-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="94e61-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="94e61-121">**Modify**</span></span>                         | <span data-ttu-id="94e61-122">Actualiza el TTL, la marca de asignación, el tiempo de espera de búsqueda, el tiempo de espera de caché y el dominio de resultado a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="94e61-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="94e61-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="94e61-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="94e61-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="94e61-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="94e61-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="94e61-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="94e61-126">**Windows Server 2003:** Este método también actualiza los tipos NextDomainName y a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="94e61-126">**Windows Server 2003:** This method also updates the NextDomainName and Types to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="94e61-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94e61-127">Properties</span></span>

<span data-ttu-id="94e61-128">La clase **MicrosoftDNS \_ NXTType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="94e61-128">The **MicrosoftDNS\_NXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94e61-129">**NextDomainName**</span><span class="sxs-lookup"><span data-stu-id="94e61-129">**NextDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e61-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="94e61-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e61-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94e61-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e61-132">Siguiente nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="94e61-132">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="94e61-133">**Tipos**</span><span class="sxs-lookup"><span data-stu-id="94e61-133">**Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e61-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="94e61-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e61-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94e61-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e61-136">Lista separada por espacios de los códigos mnemónicos del tipo RR para el nombre del propietario del registro de recursos NXT.</span><span class="sxs-lookup"><span data-stu-id="94e61-136">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94e61-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94e61-137">Requirements</span></span>



| <span data-ttu-id="94e61-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="94e61-138">Requirement</span></span> | <span data-ttu-id="94e61-139">Value</span><span class="sxs-lookup"><span data-stu-id="94e61-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94e61-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94e61-140">Minimum supported client</span></span><br/> | <span data-ttu-id="94e61-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="94e61-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="94e61-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94e61-142">Minimum supported server</span></span><br/> | <span data-ttu-id="94e61-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="94e61-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="94e61-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94e61-144">Namespace</span></span><br/>                | <span data-ttu-id="94e61-145">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="94e61-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="94e61-146">MOF</span><span class="sxs-lookup"><span data-stu-id="94e61-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94e61-147"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94e61-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94e61-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="94e61-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e61-149">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS NXTType**</span><span class="sxs-lookup"><span data-stu-id="94e61-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="94e61-150">**Método Modify de la \_ clase MicrosoftDNS NXTType**</span><span class="sxs-lookup"><span data-stu-id="94e61-150">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="94e61-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="94e61-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





