---
description: Recupera información del certificado.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: 'ICertificate2:: GetInfo (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670577"
---
# <a name="icertificate2getinfo-method"></a><span data-ttu-id="40325-103">ICertificate2:: GetInfo (método)</span><span class="sxs-lookup"><span data-stu-id="40325-103">ICertificate2::GetInfo method</span></span>

<span data-ttu-id="40325-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="40325-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="40325-105">En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="40325-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="40325-106">El método **GetInfo** recupera información del [*certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="40325-106">The **GetInfo** method retrieves information from the [*certificate*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="40325-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40325-107">Syntax</span></span>


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a><span data-ttu-id="40325-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40325-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40325-109">*InfoType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="40325-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40325-110">Un valor de la enumeración de tipo de información de certificado de CAPICOM que especifica qué tipo de datos se recupera del certificado. [**\_ \_ \_**](capicom-cert-info-type.md)</span><span class="sxs-lookup"><span data-stu-id="40325-110">A value of the [**CAPICOM\_CERT\_INFO\_TYPE**](capicom-cert-info-type.md) enumeration that specifies what type of data is retrieved from the certificate.</span></span> <span data-ttu-id="40325-111">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="40325-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="40325-112">Valor</span><span class="sxs-lookup"><span data-stu-id="40325-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="40325-113">Significado</span><span class="sxs-lookup"><span data-stu-id="40325-113">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <span data-ttu-id="40325-114"><dt>**\_ \_ \_ nombre simple del asunto de información \_ de certificado de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="40325-114"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</dt></span></span> </dl> | <span data-ttu-id="40325-115">Devuelve el nombre para mostrar del asunto del certificado.</span><span class="sxs-lookup"><span data-stu-id="40325-115">Returns the display name from the certificate subject.</span></span><br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <span data-ttu-id="40325-116"><dt>**\_ \_ \_ nombre simple del emisor de información de \_ certificado de \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="40325-116"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="40325-117">Devuelve el nombre para mostrar del emisor del certificado.</span><span class="sxs-lookup"><span data-stu-id="40325-117">Returns the display name of the issuer of the certificate.</span></span><br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <span data-ttu-id="40325-118"><dt>**\_nombre de \_ \_ \_ correo electrónico del asunto de información de certificado de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="40325-118"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="40325-119">Devuelve la dirección de correo electrónico del firmante del certificado.</span><span class="sxs-lookup"><span data-stu-id="40325-119">Returns the email address of the certificate subject.</span></span><br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <span data-ttu-id="40325-120"><dt>**\_nombre de \_ \_ \_ correo electrónico del emisor de información \_ de certificado de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="40325-120"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</dt></span></span> </dl>       | <span data-ttu-id="40325-121">Devuelve la dirección de correo electrónico del emisor del certificado.</span><span class="sxs-lookup"><span data-stu-id="40325-121">Returns the email address of the issuer of the certificate.</span></span><br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <span data-ttu-id="40325-122"><dt>**\_UPN de \_ asunto de información de certificado de CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="40325-122"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</dt></span></span> </dl>                          | <span data-ttu-id="40325-123">Devuelve el UPN del firmante del certificado.</span><span class="sxs-lookup"><span data-stu-id="40325-123">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="40325-124">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="40325-124">Introduced in CAPICOM 2.0.</span></span><br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <span data-ttu-id="40325-125"><dt>**\_UPN del \_ emisor de información de certificado de \_ CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="40325-125"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</dt></span></span> </dl>                             | <span data-ttu-id="40325-126">Devuelve el UPN del emisor del certificado.</span><span class="sxs-lookup"><span data-stu-id="40325-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="40325-127">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="40325-127">Introduced in CAPICOM 2.0.</span></span><br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <span data-ttu-id="40325-128"><dt>**\_ \_ \_ nombre DNS del asunto de información \_ de certificado de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="40325-128"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="40325-129">Devuelve el nombre DNS del firmante del certificado.</span><span class="sxs-lookup"><span data-stu-id="40325-129">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="40325-130">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="40325-130">Introduced in CAPICOM 2.0.</span></span><br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <span data-ttu-id="40325-131"><dt>**\_ \_ \_ nombre DNS del emisor de información de \_ certificado de \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="40325-131"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</dt></span></span> </dl>             | <span data-ttu-id="40325-132">Devuelve el nombre DNS del emisor del certificado.</span><span class="sxs-lookup"><span data-stu-id="40325-132">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="40325-133">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="40325-133">Introduced in CAPICOM 2.0.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40325-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40325-134">Return value</span></span>

<span data-ttu-id="40325-135">Cadena que contiene la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="40325-135">A string that contains the requested information.</span></span>

## <a name="requirements"></a><span data-ttu-id="40325-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40325-136">Requirements</span></span>



| <span data-ttu-id="40325-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="40325-137">Requirement</span></span> | <span data-ttu-id="40325-138">Value</span><span class="sxs-lookup"><span data-stu-id="40325-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40325-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="40325-139">End of client support</span></span><br/> | <span data-ttu-id="40325-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40325-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="40325-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="40325-141">End of server support</span></span><br/> | <span data-ttu-id="40325-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40325-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="40325-143">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="40325-143">Redistributable</span></span><br/>       | <span data-ttu-id="40325-144">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="40325-144">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="40325-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40325-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="40325-146"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40325-146"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40325-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="40325-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40325-148">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="40325-148">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="40325-149">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="40325-149">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
