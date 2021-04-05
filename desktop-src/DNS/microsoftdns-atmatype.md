---
title: MicrosoftDNS_ATMAType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de dirección ATM a nombre (Atma).
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- DNS de la clase MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
- MicrosoftDNS_ATMAType.Modify
- MicrosoftDNS_ATMAType.Format
- MicrosoftDNS_ATMAType.ATMAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237dc4ecb657e79e835abcfdacf90844fb05c5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996398"
---
# <a name="microsoftdns_atmatype-class"></a><span data-ttu-id="16dfc-105">MicrosoftDNS ( \_ clase ATMAType)</span><span class="sxs-lookup"><span data-stu-id="16dfc-105">MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="16dfc-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de dirección ATM a nombre (Atma).</span><span class="sxs-lookup"><span data-stu-id="16dfc-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ATM Address to Name (ATMA) record.</span></span>

<span data-ttu-id="16dfc-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="16dfc-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="16dfc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16dfc-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a><span data-ttu-id="16dfc-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="16dfc-109">Members</span></span>

<span data-ttu-id="16dfc-110">La clase **MicrosoftDNS \_ ATMAType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="16dfc-110">The **MicrosoftDNS\_ATMAType** class has these types of members:</span></span>

-   [<span data-ttu-id="16dfc-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="16dfc-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="16dfc-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16dfc-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="16dfc-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="16dfc-113">Methods</span></span>

<span data-ttu-id="16dfc-114">La clase **MicrosoftDNS \_ ATMAType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="16dfc-114">The **MicrosoftDNS\_ATMAType** class has these methods.</span></span>



| <span data-ttu-id="16dfc-115">Método</span><span class="sxs-lookup"><span data-stu-id="16dfc-115">Method</span></span>                             | <span data-ttu-id="16dfc-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="16dfc-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16dfc-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="16dfc-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="16dfc-118">Crea una instancia de un registro de recursos ATMA en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el propietario o el nombre del nodo, la clase (valor predeterminado = IN), el valor de período de vida y el formato y la dirección ATM.</span><span class="sxs-lookup"><span data-stu-id="16dfc-118">Instantiates an ATMA Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Node Name, class (default = IN), time-to-live value, and ATM format and address.</span></span> <span data-ttu-id="16dfc-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="16dfc-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="16dfc-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="16dfc-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="16dfc-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="16dfc-121">**Modify**</span></span>                         | <span data-ttu-id="16dfc-122">Actualiza el TTL, el formato y la dirección ATMA a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="16dfc-122">Updates the TTL, Format and ATMA Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="16dfc-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="16dfc-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="16dfc-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="16dfc-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="16dfc-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="16dfc-125">Qualifiers: Implemented</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="16dfc-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16dfc-126">Properties</span></span>

<span data-ttu-id="16dfc-127">La clase **MicrosoftDNS \_ ATMAType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="16dfc-127">The **MicrosoftDNS\_ATMAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16dfc-128">**ATMAddress**</span><span class="sxs-lookup"><span data-stu-id="16dfc-128">**ATMAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dfc-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="16dfc-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16dfc-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16dfc-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16dfc-131">Cadena de longitud variable de octetos que contiene la dirección ATM del nodo/propietario al que pertenece este RR.</span><span class="sxs-lookup"><span data-stu-id="16dfc-131">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="16dfc-132">Los primeros 4 bytes de la matriz se utilizan para almacenar el tamaño de la cadena de octeto.</span><span class="sxs-lookup"><span data-stu-id="16dfc-132">The first 4 bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="16dfc-133">El byte más significativo se almacena en byte 0.</span><span class="sxs-lookup"><span data-stu-id="16dfc-133">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="16dfc-134">**Format**</span><span class="sxs-lookup"><span data-stu-id="16dfc-134">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16dfc-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16dfc-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16dfc-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16dfc-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16dfc-137">Formato de dirección ATM.</span><span class="sxs-lookup"><span data-stu-id="16dfc-137">ATM address format.</span></span> <span data-ttu-id="16dfc-138">Los valores válidos son: 0 indica el formato de dirección del sistema de finalización (AESA) de ATM y 1 indica el formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="16dfc-138">Valid values are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16dfc-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16dfc-139">Requirements</span></span>



| <span data-ttu-id="16dfc-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="16dfc-140">Requirement</span></span> | <span data-ttu-id="16dfc-141">Value</span><span class="sxs-lookup"><span data-stu-id="16dfc-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16dfc-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16dfc-142">Minimum supported client</span></span><br/> | <span data-ttu-id="16dfc-143">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="16dfc-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="16dfc-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16dfc-144">Minimum supported server</span></span><br/> | <span data-ttu-id="16dfc-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="16dfc-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="16dfc-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="16dfc-146">Namespace</span></span><br/>                | <span data-ttu-id="16dfc-147">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="16dfc-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="16dfc-148">MOF</span><span class="sxs-lookup"><span data-stu-id="16dfc-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16dfc-149"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16dfc-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16dfc-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="16dfc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16dfc-151">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS ATMAType**</span><span class="sxs-lookup"><span data-stu-id="16dfc-151">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="16dfc-152">**Método Modify de la \_ clase MicrosoftDNS ATMAType**</span><span class="sxs-lookup"><span data-stu-id="16dfc-152">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="16dfc-153">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="16dfc-153">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





