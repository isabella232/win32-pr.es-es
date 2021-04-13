---
title: Método Modify de la clase MicrosoftDNS_SIGType
description: El método Modify actualiza un RR de firma (SIG).
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_SIGType clase
- MicrosoftDNS_SIGType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fbaa25ec3b6a52aae06f99ed02d50430745dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489436"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="be70d-106">Método Modify de la \_ clase MicrosoftDNS SIGType</span><span class="sxs-lookup"><span data-stu-id="be70d-106">Modify method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="be70d-107">El método **Modify** actualiza un RR de firma (SIG).</span><span class="sxs-lookup"><span data-stu-id="be70d-107">The **Modify** method updates a Signature (SIG) RR.</span></span>

## <a name="syntax"></a><span data-ttu-id="be70d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be70d-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="be70d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be70d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be70d-110">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="be70d-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be70d-111">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="be70d-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="be70d-112">*TypeCovered* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be70d-112">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be70d-113">Tipo de RR que se trata en este SIG.</span><span class="sxs-lookup"><span data-stu-id="be70d-113">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="be70d-114">*Algoritmo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="be70d-114">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be70d-115">Algoritmo usado con la clave especificada en el registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="be70d-115">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="be70d-116">Los valores asignados se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="be70d-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="be70d-117">Value</span><span class="sxs-lookup"><span data-stu-id="be70d-117">Value</span></span>                                                                                                | <span data-ttu-id="be70d-118">Significado</span><span class="sxs-lookup"><span data-stu-id="be70d-118">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="be70d-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="be70d-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="be70d-120">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="be70d-120">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="be70d-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="be70d-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="be70d-122">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="be70d-122">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="be70d-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="be70d-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="be70d-124">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="be70d-124">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="be70d-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="be70d-125"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="be70d-126">Criptografía de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="be70d-126">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="be70d-127">*Etiquetas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="be70d-127">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be70d-128">Recuento sin signo de etiquetas en el nombre de propietario del RR de firma original.</span><span class="sxs-lookup"><span data-stu-id="be70d-128">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="be70d-129">El recuento no incluye la etiqueta NULL para la raíz ni ningún carácter comodín inicial.</span><span class="sxs-lookup"><span data-stu-id="be70d-129">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="be70d-130">*OriginalTTL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be70d-130">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be70d-131">TTL del conjunto de RR firmado por el SIG.</span><span class="sxs-lookup"><span data-stu-id="be70d-131">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="be70d-132">*SignatureExpiration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be70d-132">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be70d-133">Fecha de expiración de la firma, expresada en segundos desde el comienzo del 1 de enero de 1970, hora del meridiano de Greenwich (GMT), excluyendo los segundos bisiestos.</span><span class="sxs-lookup"><span data-stu-id="be70d-133">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="be70d-134">*SignatureInception* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be70d-134">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be70d-135">Fecha y hora en las que la firma es válida, expresada en segundos desde el comienzo del 1 de enero de 1970, hora del meridiano de Greenwich (GMT), excluyendo los segundos bisiestos.</span><span class="sxs-lookup"><span data-stu-id="be70d-135">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="be70d-136">*KeyTag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be70d-136">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be70d-137">Método usado para elegir una clave que comprueba un SIG.</span><span class="sxs-lookup"><span data-stu-id="be70d-137">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="be70d-138">Vea RFC 2535, Apéndice C para el método usado para calcular un KeyTag.</span><span class="sxs-lookup"><span data-stu-id="be70d-138">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="be70d-139">*SignerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be70d-139">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be70d-140">Nombre de dominio del firmante que generó el RR SIG.</span><span class="sxs-lookup"><span data-stu-id="be70d-140">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="be70d-141">*Firma* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="be70d-141">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be70d-142">Firma, representada en base 64, con el formato definido en RFC 2535, Apéndice A.</span><span class="sxs-lookup"><span data-stu-id="be70d-142">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="be70d-143">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="be70d-143">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="be70d-144">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="be70d-144">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be70d-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be70d-145">Return value</span></span>

<span data-ttu-id="be70d-146">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="be70d-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be70d-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be70d-147">Remarks</span></span>

<span data-ttu-id="be70d-148">Los parámetros no especificados se dejan sin cambios en el registro modificado.</span><span class="sxs-lookup"><span data-stu-id="be70d-148">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="be70d-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be70d-149">Requirements</span></span>



| <span data-ttu-id="be70d-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="be70d-150">Requirement</span></span> | <span data-ttu-id="be70d-151">Value</span><span class="sxs-lookup"><span data-stu-id="be70d-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be70d-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be70d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="be70d-153">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="be70d-153">None supported</span></span><br/>                                                              |
| <span data-ttu-id="be70d-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be70d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="be70d-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="be70d-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="be70d-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="be70d-156">Namespace</span></span><br/>                | <span data-ttu-id="be70d-157">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="be70d-157">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="be70d-158">MOF</span><span class="sxs-lookup"><span data-stu-id="be70d-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be70d-159"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be70d-159"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be70d-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="be70d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be70d-161">**MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="be70d-161">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="be70d-162">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS SIGType**</span><span class="sxs-lookup"><span data-stu-id="be70d-162">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="be70d-163">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="be70d-163">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





