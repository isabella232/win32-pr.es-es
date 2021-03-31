---
title: Método Modify de la clase MicrosoftDNS_KEYType
description: El método Modify actualiza un registro de recursos de clave.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_KEYType clase
- MicrosoftDNS_KEYType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ee9182925f3f1d53fb90a4beefeb421f01c24f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151101"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="cda40-106">Método Modify de la \_ clase MicrosoftDNS KEYType</span><span class="sxs-lookup"><span data-stu-id="cda40-106">Modify method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="cda40-107">El método **Modify** actualiza un registro de recursos de clave.</span><span class="sxs-lookup"><span data-stu-id="cda40-107">The **Modify** method updates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda40-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cda40-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="cda40-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cda40-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda40-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cda40-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cda40-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="cda40-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="cda40-112">*Marcas* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cda40-112">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cda40-113">Marcas usadas para especificar la asignación, como se describe en IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="cda40-113">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="cda40-114">*Protocolo* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cda40-114">*Protocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cda40-115">Protocolo para el que se puede usar la clave especificada en el RR.</span><span class="sxs-lookup"><span data-stu-id="cda40-115">Protocol for which the key specified in the RR can be used.</span></span> <span data-ttu-id="cda40-116">Los valores asignados se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cda40-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="cda40-117">Value</span><span class="sxs-lookup"><span data-stu-id="cda40-117">Value</span></span>                                                                                                    | <span data-ttu-id="cda40-118">Significado</span><span class="sxs-lookup"><span data-stu-id="cda40-118">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="cda40-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="cda40-119"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="cda40-120">TLS</span><span class="sxs-lookup"><span data-stu-id="cda40-120">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="cda40-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="cda40-121"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="cda40-122">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="cda40-122">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="cda40-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="cda40-123"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="cda40-124">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="cda40-124">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="cda40-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="cda40-125"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="cda40-126">IPsec</span><span class="sxs-lookup"><span data-stu-id="cda40-126">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="cda40-127"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="cda40-127"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="cda40-128">Todos los protocolos</span><span class="sxs-lookup"><span data-stu-id="cda40-128">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cda40-129">*Algoritmo* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cda40-129">*Algorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cda40-130">Algoritmo usado con la clave especificada en el registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="cda40-130">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="cda40-131">Los valores asignados se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cda40-131">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="cda40-132">Value</span><span class="sxs-lookup"><span data-stu-id="cda40-132">Value</span></span>                                                                                                | <span data-ttu-id="cda40-133">Significado</span><span class="sxs-lookup"><span data-stu-id="cda40-133">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="cda40-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="cda40-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="cda40-135">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="cda40-135">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="cda40-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="cda40-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="cda40-137">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="cda40-137">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="cda40-138"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="cda40-138"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="cda40-139">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="cda40-139">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="cda40-140"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="cda40-140"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="cda40-141">Criptografía de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="cda40-141">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cda40-142">*PublicKey* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cda40-142">*PublicKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cda40-143">Clave pública, representada en base 64 como se describe en el Apéndice A de RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="cda40-143">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="cda40-144">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="cda40-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cda40-145">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="cda40-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cda40-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cda40-146">Return value</span></span>

<span data-ttu-id="cda40-147">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cda40-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cda40-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cda40-148">Remarks</span></span>

<span data-ttu-id="cda40-149">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="cda40-149">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="cda40-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cda40-150">Requirements</span></span>



| <span data-ttu-id="cda40-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="cda40-151">Requirement</span></span> | <span data-ttu-id="cda40-152">Value</span><span class="sxs-lookup"><span data-stu-id="cda40-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cda40-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cda40-153">Minimum supported client</span></span><br/> | <span data-ttu-id="cda40-154">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cda40-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cda40-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cda40-155">Minimum supported server</span></span><br/> | <span data-ttu-id="cda40-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cda40-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cda40-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cda40-157">Namespace</span></span><br/>                | <span data-ttu-id="cda40-158">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="cda40-158">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cda40-159">MOF</span><span class="sxs-lookup"><span data-stu-id="cda40-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cda40-160"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cda40-160"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda40-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="cda40-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda40-162">**El \_ KEYType de MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cda40-162">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="cda40-163">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS KEYType**</span><span class="sxs-lookup"><span data-stu-id="cda40-163">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="cda40-164">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="cda40-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





