---
description: Recupera el estado de validez de la cadena o de un certificado específico de la cadena.
title: 'IChain2:: status (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Status
- IChain.Status
- Chain.Status
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23673289e2ff39d4180a4be8dc0be61f4a5cffc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690530"
---
# <a name="ichain2status-property"></a><span data-ttu-id="d20d0-103">IChain2:: status (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d20d0-103">IChain2::Status property</span></span>

<span data-ttu-id="d20d0-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d20d0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d20d0-105">En su lugar, use la [**clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d20d0-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d20d0-106">La propiedad **status** recupera el estado de validez de la cadena o de un certificado específico de la cadena.</span><span class="sxs-lookup"><span data-stu-id="d20d0-106">The **Status** property retrieves the validity status of the chain or a specific certificate in the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="d20d0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d20d0-107">Syntax</span></span>


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a><span data-ttu-id="d20d0-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d20d0-108">Property value</span></span>

<span data-ttu-id="d20d0-109">Un valor de **tipo Long** que representa el indicador de estado de validez de la cadena o del certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="d20d0-109">A **LONG** value that represents the validity status indicator of the chain or the specified certificate.</span></span> <span data-ttu-id="d20d0-110">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="d20d0-110">The following table shows the possible values.</span></span> <span data-ttu-id="d20d0-111">Esta propiedad contendrá cero si la cadena o el certificado especificado son válidos.</span><span class="sxs-lookup"><span data-stu-id="d20d0-111">This property will contain zero if the chain or specified certificate is valid.</span></span> <span data-ttu-id="d20d0-112">De lo contrario, esta propiedad contendrá una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d20d0-112">Otherwise, this property will contain a combination of one or more of the following values.</span></span>

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span data-ttu-id="d20d0-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ La \_ confianza \_ no es una \_ hora \_ válida** (&H00000001)</span><span class="sxs-lookup"><span data-stu-id="d20d0-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_VALID** (&H00000001)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-114">Este certificado o uno de los certificados de la cadena de certificados no es válido en tiempo.</span><span class="sxs-lookup"><span data-stu-id="d20d0-114">This certificate or one of the certificates in the certificate chain is not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span data-ttu-id="d20d0-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ La \_ confianza \_ no \_ está \_ anidada en tiempo** (&H00000002)</span><span class="sxs-lookup"><span data-stu-id="d20d0-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_NESTED** (&H00000002)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-116">Los certificados de la cadena no están correctamente anidados.</span><span class="sxs-lookup"><span data-stu-id="d20d0-116">Certificates in the chain are not properly time nested.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span data-ttu-id="d20d0-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ \_Se \_ revoca la confianza** (&H00000004)</span><span class="sxs-lookup"><span data-stu-id="d20d0-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM\_TRUST\_IS\_REVOKED** (&H00000004)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-118">Se ha revocado la confianza de este certificado o de uno de los certificados de la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="d20d0-118">Trust for this certificate or one of the certificates in the certificate chain has been revoked.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span data-ttu-id="d20d0-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ La \_ confianza \_ no \_ es \_ válida** para la firma (&H00000008)</span><span class="sxs-lookup"><span data-stu-id="d20d0-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_SIGNATURE\_VALID** (&H00000008)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-120">El certificado o uno de los certificados de la cadena de certificados no tiene una firma válida.</span><span class="sxs-lookup"><span data-stu-id="d20d0-120">The certificate or one of the certificates in the certificate chain does not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span data-ttu-id="d20d0-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ La \_ confianza \_ no es \_ válida \_ para el \_ uso** (&H00000010)</span><span class="sxs-lookup"><span data-stu-id="d20d0-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00000010)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-122">El certificado o la cadena de certificados no es válido para su uso propuesto.</span><span class="sxs-lookup"><span data-stu-id="d20d0-122">The certificate or certificate chain is not valid for its proposed usage.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span data-ttu-id="d20d0-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ La confianza \_ es una \_ \_ raíz que no es de confianza** (&H00000020)</span><span class="sxs-lookup"><span data-stu-id="d20d0-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM\_TRUST\_IS\_UNTRUSTED\_ROOT** (&H00000020)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-124">El certificado o la cadena de certificados se basa en una raíz que no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="d20d0-124">The certificate or certificate chain is based on an untrusted root.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span data-ttu-id="d20d0-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ \_Estado de REvocación de confianza \_ \_ desconocido** (&H00000040)</span><span class="sxs-lookup"><span data-stu-id="d20d0-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM\_TRUST\_REVOCATION\_STATUS\_UNKNOWN** (&H00000040)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-126">Se desconoce el estado de revocación del certificado o uno de los certificados de la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="d20d0-126">The revocation status of the certificate or one of the certificates in the certificate chain is unknown.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span data-ttu-id="d20d0-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ La confianza \_ es \_ cíclica** (&H00000080)</span><span class="sxs-lookup"><span data-stu-id="d20d0-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM\_TRUST\_IS\_CYCLIC** (&H00000080)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-128">Uno de los certificados de la cadena fue emitido por una [*entidad de certificación*](../secgloss/c-gly.md) que el certificado original había certificado.</span><span class="sxs-lookup"><span data-stu-id="d20d0-128">One of the certificates in the chain was issued by a [*certification authority*](../secgloss/c-gly.md) that the original certificate had certified.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span data-ttu-id="d20d0-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ CONFIAR en una \_ \_ extensión no válida** (&H00000100)</span><span class="sxs-lookup"><span data-stu-id="d20d0-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM\_TRUST\_INVALID\_EXTENSION** (&H00000100)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-130">Uno de los certificados tiene una extensión no válida.</span><span class="sxs-lookup"><span data-stu-id="d20d0-130">One of the certificates has an extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span data-ttu-id="d20d0-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ CONFIAR en las \_ \_ \_ restricciones de Directiva no válidas** (&H00000200)</span><span class="sxs-lookup"><span data-stu-id="d20d0-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM\_TRUST\_INVALID\_POLICY\_CONSTRAINTS** (&H00000200)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-132">El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de directiva y uno de los certificados emitidos tiene una extensión de asignación de directivas no permitida o no tiene una extensión de directivas de emisión requerida.</span><span class="sxs-lookup"><span data-stu-id="d20d0-132">The certificate or one of the certificates in the certificate chain has a policy constraints extension, and one of the issued certificates has a disallowed policy mapping extension or does not have a required issuance policies extension.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span data-ttu-id="d20d0-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ CONFIAR \_ en \_ \_ Restricciones básicas no válidas** (&H00000400)</span><span class="sxs-lookup"><span data-stu-id="d20d0-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM\_TRUST\_INVALID\_BASIC\_CONSTRAINTS** (&H00000400)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-134">El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones básicas y el certificado no se puede usar para emitir otros certificados, o bien se ha superado la longitud de la ruta de acceso de la cadena.</span><span class="sxs-lookup"><span data-stu-id="d20d0-134">The certificate or one of the certificates in the certificate chain has a basic constraints extension, and either the certificate cannot be used to issue other certificates, or the chain path length has been exceeded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span data-ttu-id="d20d0-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ CONFIAR \_ en \_ \_ restricciones de nombre no válidas** (&H00000800)</span><span class="sxs-lookup"><span data-stu-id="d20d0-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM\_TRUST\_INVALID\_NAME\_CONSTRAINTS** (&H00000800)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-136">El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre que no es válida.</span><span class="sxs-lookup"><span data-stu-id="d20d0-136">The certificate or one of the certificates in the certificate chain has a name constraints extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span data-ttu-id="d20d0-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ La \_ confianza \_ no \_ admite \_ la \_ restricción de nombre** (&H00001000)</span><span class="sxs-lookup"><span data-stu-id="d20d0-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_SUPPORTED\_NAME\_CONSTRAINT** (&H00001000)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-138">El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre que contiene campos no compatibles.</span><span class="sxs-lookup"><span data-stu-id="d20d0-138">The certificate or one of the certificates in the certificate chain has a name constraints extension that contains unsupported fields.</span></span> <span data-ttu-id="d20d0-139">No se admiten los campos mínimo y máximo.</span><span class="sxs-lookup"><span data-stu-id="d20d0-139">The minimum and maximum fields are not supported.</span></span> <span data-ttu-id="d20d0-140">Por lo tanto, el mínimo debe ser siempre cero y el máximo siempre debe estar ausente.</span><span class="sxs-lookup"><span data-stu-id="d20d0-140">Thus minimum must always be zero and maximum must always be absent.</span></span> <span data-ttu-id="d20d0-141">Solo se admite UPN para otro nombre.</span><span class="sxs-lookup"><span data-stu-id="d20d0-141">Only UPN is supported for an Other Name.</span></span> <span data-ttu-id="d20d0-142">No se admiten las siguientes opciones de nombre alternativo:</span><span class="sxs-lookup"><span data-stu-id="d20d0-142">The following alternative name choices are not supported:</span></span>

-   <span data-ttu-id="d20d0-143">Dirección X400</span><span class="sxs-lookup"><span data-stu-id="d20d0-143">X400 Address</span></span>
-   <span data-ttu-id="d20d0-144">Nombre de entidad de EDI</span><span class="sxs-lookup"><span data-stu-id="d20d0-144">EDI Party Name</span></span>
-   <span data-ttu-id="d20d0-145">ID. registrado</span><span class="sxs-lookup"><span data-stu-id="d20d0-145">Registered Id</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span data-ttu-id="d20d0-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ La \_ confianza \_ no ha \_ definido una \_ \_ restricción de nombre** (&H00002000)</span><span class="sxs-lookup"><span data-stu-id="d20d0-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_DEFINED\_NAME\_CONSTRAINT** (&H00002000)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-147">El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre y falta una restricción de nombre para una de las opciones de nombre del certificado final.</span><span class="sxs-lookup"><span data-stu-id="d20d0-147">The certificate or one of the certificates in the certificate chain has a name constraints extension, and a name constraint is missing for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span data-ttu-id="d20d0-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ La \_ confianza \_ no ha \_ permitido la \_ \_ restricción de nombre** (&H00004000)</span><span class="sxs-lookup"><span data-stu-id="d20d0-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_PERMITTED\_NAME\_CONSTRAINT** (&H00004000)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-149">El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre y no hay una restricción de nombre permitida para una de las opciones de nombre del certificado final.</span><span class="sxs-lookup"><span data-stu-id="d20d0-149">The certificate or one of the certificates in the certificate chain has a name constraints extension, and there is not a permitted name constraint for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span data-ttu-id="d20d0-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ La confianza \_ tiene una \_ \_ \_ restricción de nombre excluida** (&H00008000)</span><span class="sxs-lookup"><span data-stu-id="d20d0-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_EXCLUDED\_NAME\_CONSTRAINT** (&H00008000)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-151">El certificado o uno de los certificados de la cadena de certificados tiene una extensión de restricciones de nombre, y una de las opciones de nombre del certificado final se excluye explícitamente.</span><span class="sxs-lookup"><span data-stu-id="d20d0-151">The certificate or one of the certificates in the certificate chain has a name constraints extension, and one of the name choices in the end certificate is explicitly excluded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span data-ttu-id="d20d0-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ La \_ confianza \_ es \_ revocación sin conexión** (&H01000000)</span><span class="sxs-lookup"><span data-stu-id="d20d0-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM\_TRUST\_IS\_OFFLINE\_REVOCATION** (&H01000000)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-153">El estado de revocación del certificado o uno de los certificados de la cadena de certificados está sin conexión o obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d20d0-153">The revocation status of the certificate or one of the certificates in the certificate chain is either offline or stale.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span data-ttu-id="d20d0-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ NO confiar en la \_ \_ Directiva de \_ cadena \_ de emisión** (&H02000000)</span><span class="sxs-lookup"><span data-stu-id="d20d0-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM\_TRUST\_NO\_ISSUANCE\_CHAIN\_POLICY** (&H02000000)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-155">El certificado final no tiene ninguna directiva de emisión resultante y uno de los certificados de la CA emisora tiene una extensión de restricciones de directivas que lo requiere.</span><span class="sxs-lookup"><span data-stu-id="d20d0-155">The end certificate does not have any resultant issuance policies, and one of the issuing CA certificates has a policy constraints extension requiring it.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span data-ttu-id="d20d0-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ La confianza \_ es una \_ \_ cadena parcial** (&H00010000)</span><span class="sxs-lookup"><span data-stu-id="d20d0-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM\_TRUST\_IS\_PARTIAL\_CHAIN** (&H00010000)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-157">La cadena de certificados no compite.</span><span class="sxs-lookup"><span data-stu-id="d20d0-157">The certificate chain is not compete.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span data-ttu-id="d20d0-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ CONFIAR en \_ CTL \_ no es una \_ \_ hora \_ válida** (&H00020000)</span><span class="sxs-lookup"><span data-stu-id="d20d0-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_TIME\_VALID** (&H00020000)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-159">Una CTL utilizada para crear esta cadena no era válida.</span><span class="sxs-lookup"><span data-stu-id="d20d0-159">A CTL used to create this chain was not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span data-ttu-id="d20d0-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ La \_ CTL de confianza \_ \_ no es \_ \_ válida** para la firma (&H00040000)</span><span class="sxs-lookup"><span data-stu-id="d20d0-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_SIGNATURE\_VALID** (&H00040000)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-161">Una CTL utilizada para crear esta cadena no tenía una signatura válida.</span><span class="sxs-lookup"><span data-stu-id="d20d0-161">A CTL used to create this chain did not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span data-ttu-id="d20d0-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ La \_ CTL \_ \_ de confianza no es \_ válida para el \_ \_ uso** (&H00080000)</span><span class="sxs-lookup"><span data-stu-id="d20d0-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00080000)</span></span>


</dt> <dd>

<span data-ttu-id="d20d0-163">Una CTL utilizada para crear esta cadena no es válida para este uso.</span><span class="sxs-lookup"><span data-stu-id="d20d0-163">A CTL used to create this chain is not valid for this usage.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d20d0-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d20d0-164">Requirements</span></span>



| <span data-ttu-id="d20d0-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="d20d0-165">Requirement</span></span> | <span data-ttu-id="d20d0-166">Value</span><span class="sxs-lookup"><span data-stu-id="d20d0-166">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d20d0-167">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d20d0-167">End of client support</span></span><br/> | <span data-ttu-id="d20d0-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d20d0-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d20d0-169">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d20d0-169">End of server support</span></span><br/> | <span data-ttu-id="d20d0-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d20d0-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d20d0-171">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d20d0-171">Redistributable</span></span><br/>       | <span data-ttu-id="d20d0-172">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="d20d0-172">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d20d0-173">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d20d0-173">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d20d0-174"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d20d0-174"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
