---
title: MicrosoftDNS_KEYType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de recursos de clave.
ms.assetid: d3fa1f35-fa0a-47ee-b2be-4464b9b21d80
keywords:
- DNS de la clase MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
- MicrosoftDNS_KEYType.Modify
- MicrosoftDNS_KEYType.Flags
- MicrosoftDNS_KEYType.Protocol
- MicrosoftDNS_KEYType.Algorithm
- MicrosoftDNS_KEYType.PublicKey
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1e814af1d22820f1722e5812dd314dd1c7f6e0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905345"
---
# <a name="microsoftdns_keytype-class"></a><span data-ttu-id="94d8a-105">MicrosoftDNS ( \_ clase)</span><span class="sxs-lookup"><span data-stu-id="94d8a-105">MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="94d8a-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de recursos de clave.</span><span class="sxs-lookup"><span data-stu-id="94d8a-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a KEY Resource Record.</span></span>

<span data-ttu-id="94d8a-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="94d8a-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="94d8a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94d8a-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_KEYType : MicrosoftDNS_ResourceRecord
{
  uint16 Flags;
  uint16 Protocol;
  uint16 Algorithm;
  string PublicKey;
};
```

## <a name="members"></a><span data-ttu-id="94d8a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="94d8a-109">Members</span></span>

<span data-ttu-id="94d8a-110">La clase **MicrosoftDNS \_ KEYType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="94d8a-110">The **MicrosoftDNS\_KEYType** class has these types of members:</span></span>

-   [<span data-ttu-id="94d8a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="94d8a-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="94d8a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94d8a-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="94d8a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="94d8a-113">Methods</span></span>

<span data-ttu-id="94d8a-114">La clase **MicrosoftDNS \_ KEYType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="94d8a-114">The **MicrosoftDNS\_KEYType** class has these methods.</span></span>



| <span data-ttu-id="94d8a-115">Método</span><span class="sxs-lookup"><span data-stu-id="94d8a-115">Method</span></span>                             | <span data-ttu-id="94d8a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="94d8a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94d8a-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="94d8a-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="94d8a-118">Crea una instancia de un registro de recursos de clave basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y la marca de asignación de WINS, el tiempo de espera de búsqueda inverso, el tiempo de espera de la caché</span><span class="sxs-lookup"><span data-stu-id="94d8a-118">Instantiates a KEY Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="94d8a-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="94d8a-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="94d8a-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="94d8a-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="94d8a-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="94d8a-121">**Modify**</span></span>                         | <span data-ttu-id="94d8a-122">Actualiza el TTL, la marca de asignación, el tiempo de espera de búsqueda, el tiempo de espera de caché y el dominio de resultado a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="94d8a-122">Updates the TTL, mapping flag, look-up time out, cache time out, and result domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="94d8a-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="94d8a-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="94d8a-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="94d8a-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="94d8a-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="94d8a-125">Qualifiers: Implemented</span></span><br/>                          |



 

### <a name="properties"></a><span data-ttu-id="94d8a-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94d8a-126">Properties</span></span>

<span data-ttu-id="94d8a-127">La clase ^ **\_ KEYType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="94d8a-127">The **MicrosoftDNS\_KEYType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94d8a-128">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="94d8a-128">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94d8a-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94d8a-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94d8a-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94d8a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94d8a-131">Algoritmo usado con la clave especificada en el registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="94d8a-131">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="94d8a-132">Los valores asignados se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="94d8a-132">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="94d8a-133">Value</span><span class="sxs-lookup"><span data-stu-id="94d8a-133">Value</span></span>                                                                                                | <span data-ttu-id="94d8a-134">Significado</span><span class="sxs-lookup"><span data-stu-id="94d8a-134">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="94d8a-135"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="94d8a-135"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="94d8a-136">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="94d8a-136">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="94d8a-137"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="94d8a-137"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="94d8a-138">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="94d8a-138">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="94d8a-139"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="94d8a-139"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="94d8a-140">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="94d8a-140">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="94d8a-141"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="94d8a-141"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="94d8a-142">Criptografía de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="94d8a-142">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="94d8a-143">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="94d8a-143">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94d8a-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94d8a-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94d8a-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94d8a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94d8a-146">Marcas usadas para especificar la asignación, como se describe en IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="94d8a-146">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="94d8a-147">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="94d8a-147">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94d8a-148">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94d8a-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94d8a-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94d8a-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94d8a-150">Protocolo para el que se puede usar la clave especificada en el registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="94d8a-150">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="94d8a-151">Los valores asignados se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="94d8a-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="94d8a-152">Value</span><span class="sxs-lookup"><span data-stu-id="94d8a-152">Value</span></span>                                                                                                    | <span data-ttu-id="94d8a-153">Significado</span><span class="sxs-lookup"><span data-stu-id="94d8a-153">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="94d8a-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="94d8a-154"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="94d8a-155">TLS</span><span class="sxs-lookup"><span data-stu-id="94d8a-155">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="94d8a-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="94d8a-156"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="94d8a-157">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="94d8a-157">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="94d8a-158"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="94d8a-158"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="94d8a-159">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="94d8a-159">DNSSEC</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="94d8a-160"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="94d8a-160"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="94d8a-161">IPsec</span><span class="sxs-lookup"><span data-stu-id="94d8a-161">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="94d8a-162"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="94d8a-162"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="94d8a-163">Todos los protocolos</span><span class="sxs-lookup"><span data-stu-id="94d8a-163">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="94d8a-164">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="94d8a-164">**PublicKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94d8a-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="94d8a-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94d8a-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94d8a-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94d8a-167">Clave pública, representada en base 64 como se describe en el Apéndice A de RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="94d8a-167">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94d8a-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94d8a-168">Requirements</span></span>



| <span data-ttu-id="94d8a-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="94d8a-169">Requirement</span></span> | <span data-ttu-id="94d8a-170">Value</span><span class="sxs-lookup"><span data-stu-id="94d8a-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94d8a-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94d8a-171">Minimum supported client</span></span><br/> | <span data-ttu-id="94d8a-172">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="94d8a-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="94d8a-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94d8a-173">Minimum supported server</span></span><br/> | <span data-ttu-id="94d8a-174">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="94d8a-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="94d8a-175">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94d8a-175">Namespace</span></span><br/>                | <span data-ttu-id="94d8a-176">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="94d8a-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="94d8a-177">MOF</span><span class="sxs-lookup"><span data-stu-id="94d8a-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94d8a-178"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94d8a-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94d8a-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="94d8a-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d8a-180">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS KEYType**</span><span class="sxs-lookup"><span data-stu-id="94d8a-180">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="94d8a-181">**Método Modify de la \_ clase MicrosoftDNS KEYType**</span><span class="sxs-lookup"><span data-stu-id="94d8a-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="94d8a-182">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="94d8a-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





