---
title: MicrosoftDNS_ISDNType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro ISDN (RDSI).
ms.assetid: 8925042c-65d3-465f-aedd-9f7c862620b5
keywords:
- DNS de la clase MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
- MicrosoftDNS_ISDNType.Modify
- MicrosoftDNS_ISDNType.ISDNNumber
- MicrosoftDNS_ISDNType.SubAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4e8b50d75f7b6d57226247c978ced45e07b1acc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149932"
---
# <a name="microsoftdns_isdntype-class"></a><span data-ttu-id="13dbd-105">MicrosoftDNS ( \_ clase ISDNType)</span><span class="sxs-lookup"><span data-stu-id="13dbd-105">MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="13dbd-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro ISDN (RDSI).</span><span class="sxs-lookup"><span data-stu-id="13dbd-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ISDN record.</span></span>

<span data-ttu-id="13dbd-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="13dbd-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="13dbd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13dbd-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ISDNType : MicrosoftDNS_ResourceRecord
{
  string ISDNNumber;
  string SubAddress;
};
```

## <a name="members"></a><span data-ttu-id="13dbd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="13dbd-109">Members</span></span>

<span data-ttu-id="13dbd-110">La clase **MicrosoftDNS \_ ISDNType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="13dbd-110">The **MicrosoftDNS\_ISDNType** class has these types of members:</span></span>

-   [<span data-ttu-id="13dbd-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="13dbd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="13dbd-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13dbd-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="13dbd-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="13dbd-113">Methods</span></span>

<span data-ttu-id="13dbd-114">La clase **MicrosoftDNS \_ ISDNType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="13dbd-114">The **MicrosoftDNS\_ISDNType** class has these methods.</span></span>



| <span data-ttu-id="13dbd-115">Método</span><span class="sxs-lookup"><span data-stu-id="13dbd-115">Method</span></span>                             | <span data-ttu-id="13dbd-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="13dbd-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13dbd-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="13dbd-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="13dbd-118">Crea una instancia de un registro de recursos ISDN basado en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y el número y la Subdirección ISDN del propietario.</span><span class="sxs-lookup"><span data-stu-id="13dbd-118">Instantiates an ISDN Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the ISDN number and subaddress of the owner.</span></span> <span data-ttu-id="13dbd-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="13dbd-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="13dbd-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="13dbd-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="13dbd-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="13dbd-121">**Modify**</span></span>                         | <span data-ttu-id="13dbd-122">Actualiza el TTL, el número ISDN (RDSI) y la Subdirección a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="13dbd-122">Updates the TTL, ISDN Number, and Subaddress to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="13dbd-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="13dbd-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="13dbd-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="13dbd-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="13dbd-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="13dbd-125">Qualifiers: Implemented</span></span><br/>                   |



 

### <a name="properties"></a><span data-ttu-id="13dbd-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13dbd-126">Properties</span></span>

<span data-ttu-id="13dbd-127">La clase **MicrosoftDNS \_ ISDNType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="13dbd-127">The **MicrosoftDNS\_ISDNType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13dbd-128">**ISDNNumber**</span><span class="sxs-lookup"><span data-stu-id="13dbd-128">**ISDNNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13dbd-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="13dbd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13dbd-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13dbd-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13dbd-131">Número ISDN y DDI del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="13dbd-131">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="13dbd-132">**Subdirección**</span><span class="sxs-lookup"><span data-stu-id="13dbd-132">**SubAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13dbd-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="13dbd-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13dbd-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13dbd-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13dbd-135">Subdirección del propietario, si está definido.</span><span class="sxs-lookup"><span data-stu-id="13dbd-135">Subaddress of the owner, if defined.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13dbd-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13dbd-136">Requirements</span></span>



| <span data-ttu-id="13dbd-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="13dbd-137">Requirement</span></span> | <span data-ttu-id="13dbd-138">Value</span><span class="sxs-lookup"><span data-stu-id="13dbd-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13dbd-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13dbd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="13dbd-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="13dbd-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="13dbd-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13dbd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="13dbd-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13dbd-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="13dbd-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="13dbd-143">Namespace</span></span><br/>                | <span data-ttu-id="13dbd-144">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="13dbd-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="13dbd-145">MOF</span><span class="sxs-lookup"><span data-stu-id="13dbd-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13dbd-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13dbd-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13dbd-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="13dbd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13dbd-148">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS ISDNType**</span><span class="sxs-lookup"><span data-stu-id="13dbd-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="13dbd-149">**Método Modify de la \_ clase MicrosoftDNS ISDNType**</span><span class="sxs-lookup"><span data-stu-id="13dbd-149">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="13dbd-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="13dbd-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





