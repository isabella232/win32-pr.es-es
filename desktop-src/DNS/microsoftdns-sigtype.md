---
title: MicrosoftDNS_SIGType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de recursos de firma (SIG).
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- DNS de la clase MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
- MicrosoftDNS_SIGType.Modify
- MicrosoftDNS_SIGType.TypeCovered
- MicrosoftDNS_SIGType.Algorithm
- MicrosoftDNS_SIGType.Labels
- MicrosoftDNS_SIGType.OriginalTTL
- MicrosoftDNS_SIGType.SignatureExpiration
- MicrosoftDNS_SIGType.SignatureInception
- MicrosoftDNS_SIGType.KeyTag
- MicrosoftDNS_SIGType.SignerName
- MicrosoftDNS_SIGType.Signature
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172869e90664f88e53fc4cfc89f23b8adbf1e3a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801346"
---
# <a name="microsoftdns_sigtype-class"></a><span data-ttu-id="98268-105">MicrosoftDNS ( \_ clase SIGType)</span><span class="sxs-lookup"><span data-stu-id="98268-105">MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="98268-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de recursos de firma (SIG).</span><span class="sxs-lookup"><span data-stu-id="98268-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Signature (SIG) Resource Record.</span></span>

<span data-ttu-id="98268-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="98268-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="98268-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98268-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SIGType : MicrosoftDNS_ResourceRecord
{
  uint16 TypeCovered;
  uint16 Algorithm;
  uint16 Labels;
  uint32 OriginalTTL;
  uint32 SignatureExpiration;
  uint32 SignatureInception;
  uint16 KeyTag;
  string SignerName;
  string Signature;
};
```

## <a name="members"></a><span data-ttu-id="98268-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="98268-109">Members</span></span>

<span data-ttu-id="98268-110">La clase **MicrosoftDNS \_ SIGType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="98268-110">The **MicrosoftDNS\_SIGType** class has these types of members:</span></span>

-   [<span data-ttu-id="98268-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="98268-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="98268-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="98268-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="98268-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="98268-113">Methods</span></span>

<span data-ttu-id="98268-114">La clase **MicrosoftDNS \_ SIGType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="98268-114">The **MicrosoftDNS\_SIGType** class has these methods.</span></span>



| <span data-ttu-id="98268-115">Método</span><span class="sxs-lookup"><span data-stu-id="98268-115">Method</span></span>                             | <span data-ttu-id="98268-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="98268-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98268-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="98268-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="98268-118">Crea una instancia de un RR SIG basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y la marca de asignación WINS, el tiempo de espera de búsqueda inverso, el tiempo de espera de caché WINS y el nombre de</span><span class="sxs-lookup"><span data-stu-id="98268-118">Instantiates an SIG RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="98268-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="98268-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="98268-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="98268-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="98268-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="98268-121">**Modify**</span></span>                         | <span data-ttu-id="98268-122">Actualiza el TTL, la marca de asignación, el tiempo de espera de búsqueda, el tiempo de espera de caché y el dominio de resultado a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="98268-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="98268-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="98268-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="98268-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="98268-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="98268-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="98268-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="98268-126">**Windows Server 2003:** Este método también actualiza TypeCovered, Algorithm, Labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName y Signature a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="98268-126">**Windows Server 2003:** This method also updates the TypeCovered, Algorithm, Labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName and Signature to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="98268-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="98268-127">Properties</span></span>

<span data-ttu-id="98268-128">La clase **MicrosoftDNS \_ SIGType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="98268-128">The **MicrosoftDNS\_SIGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98268-129">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="98268-129">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98268-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98268-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98268-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98268-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98268-132">Algoritmo usado con la clave especificada en el registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="98268-132">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="98268-133">Los valores asignados se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="98268-133">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="98268-134">Value</span><span class="sxs-lookup"><span data-stu-id="98268-134">Value</span></span>                                                                                                | <span data-ttu-id="98268-135">Significado</span><span class="sxs-lookup"><span data-stu-id="98268-135">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="98268-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="98268-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="98268-137">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="98268-137">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="98268-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="98268-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="98268-139">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="98268-139">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="98268-140"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="98268-140"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="98268-141">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="98268-141">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="98268-142"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="98268-142"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="98268-143">Criptografía de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="98268-143">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="98268-144">**KeyTag**</span><span class="sxs-lookup"><span data-stu-id="98268-144">**KeyTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98268-145">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98268-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98268-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98268-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98268-147">Método usado para elegir una clave que comprueba un SIG.</span><span class="sxs-lookup"><span data-stu-id="98268-147">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="98268-148">Vea RFC 2535, Apéndice C para el método usado para calcular un KeyTag.</span><span class="sxs-lookup"><span data-stu-id="98268-148">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="98268-149">**Etiquetas**</span><span class="sxs-lookup"><span data-stu-id="98268-149">**Labels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98268-150">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98268-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98268-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98268-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98268-152">Recuento sin signo de etiquetas en el nombre de propietario del RR de firma original.</span><span class="sxs-lookup"><span data-stu-id="98268-152">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="98268-153">El recuento no incluye la etiqueta NULL para la raíz ni ningún carácter comodín inicial.</span><span class="sxs-lookup"><span data-stu-id="98268-153">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="98268-154">**OriginalTTL**</span><span class="sxs-lookup"><span data-stu-id="98268-154">**OriginalTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98268-155">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98268-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98268-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98268-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98268-157">TTL del conjunto de RR firmado por el SIG.</span><span class="sxs-lookup"><span data-stu-id="98268-157">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="98268-158">**Signature**</span><span class="sxs-lookup"><span data-stu-id="98268-158">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98268-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="98268-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98268-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98268-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98268-161">Firma, representada en base 64, con el formato definido en RFC 2535, Apéndice A.</span><span class="sxs-lookup"><span data-stu-id="98268-161">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="98268-162">**SignatureExpiration**</span><span class="sxs-lookup"><span data-stu-id="98268-162">**SignatureExpiration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98268-163">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98268-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98268-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98268-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98268-165">Fecha de expiración de la firma, expresada en segundos desde el comienzo del 1 de enero de 1970, hora del meridiano de Greenwich (GMT), excluyendo los segundos bisiestos.</span><span class="sxs-lookup"><span data-stu-id="98268-165">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="98268-166">**SignatureInception**</span><span class="sxs-lookup"><span data-stu-id="98268-166">**SignatureInception**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98268-167">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98268-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98268-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98268-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98268-169">Fecha y hora en las que la firma es válida, expresada en segundos desde el comienzo del 1 de enero de 1970, hora del meridiano de Greenwich (GMT), excluyendo los segundos bisiestos.</span><span class="sxs-lookup"><span data-stu-id="98268-169">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="98268-170">**SignerName**</span><span class="sxs-lookup"><span data-stu-id="98268-170">**SignerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98268-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="98268-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98268-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98268-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98268-173">Nombre de dominio del firmante que generó el RR SIG.</span><span class="sxs-lookup"><span data-stu-id="98268-173">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="98268-174">**TypeCovered**</span><span class="sxs-lookup"><span data-stu-id="98268-174">**TypeCovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98268-175">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98268-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98268-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98268-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98268-177">Tipo de RR que se trata en este SIG.</span><span class="sxs-lookup"><span data-stu-id="98268-177">Type of RR covered by this SIG.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98268-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98268-178">Requirements</span></span>



| <span data-ttu-id="98268-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="98268-179">Requirement</span></span> | <span data-ttu-id="98268-180">Value</span><span class="sxs-lookup"><span data-stu-id="98268-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98268-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98268-181">Minimum supported client</span></span><br/> | <span data-ttu-id="98268-182">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="98268-182">None supported</span></span><br/>                                                              |
| <span data-ttu-id="98268-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98268-183">Minimum supported server</span></span><br/> | <span data-ttu-id="98268-184">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98268-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="98268-185">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="98268-185">Namespace</span></span><br/>                | <span data-ttu-id="98268-186">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="98268-186">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="98268-187">MOF</span><span class="sxs-lookup"><span data-stu-id="98268-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98268-188"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98268-188"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98268-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="98268-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98268-190">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS SIGType**</span><span class="sxs-lookup"><span data-stu-id="98268-190">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="98268-191">**Método Modify de la \_ clase MicrosoftDNS SIGType**</span><span class="sxs-lookup"><span data-stu-id="98268-191">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="98268-192">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="98268-192">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





