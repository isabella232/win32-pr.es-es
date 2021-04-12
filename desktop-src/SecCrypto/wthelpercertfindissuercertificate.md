---
description: Busca un certificado de emisor de los almacenes de certificados especificados que coincide con el certificado de sujeto especificado.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: WTHelperCertFindIssuerCertificate función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277003"
---
# <a name="wthelpercertfindissuercertificate-function"></a><span data-ttu-id="f2f67-103">WTHelperCertFindIssuerCertificate función)</span><span class="sxs-lookup"><span data-stu-id="f2f67-103">WTHelperCertFindIssuerCertificate function</span></span>

<span data-ttu-id="f2f67-104">\[La función **WTHelperCertFindIssuerCertificate** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="f2f67-104">\[The **WTHelperCertFindIssuerCertificate** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f2f67-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="f2f67-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="f2f67-106">La función **WTHelperCertFindIssuerCertificate** busca un certificado de emisor de los almacenes de certificados especificados que coincide con el certificado de sujeto especificado.</span><span class="sxs-lookup"><span data-stu-id="f2f67-106">The **WTHelperCertFindIssuerCertificate** function finds an issuer certificate from the specified certificate stores that matches the specified subject certificate.</span></span>

> [!Note]  
> <span data-ttu-id="f2f67-107">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="f2f67-107">This function has no associated import library.</span></span> <span data-ttu-id="f2f67-108">Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Wintrust.dll.</span><span class="sxs-lookup"><span data-stu-id="f2f67-108">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f2f67-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2f67-109">Syntax</span></span>


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a><span data-ttu-id="f2f67-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2f67-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2f67-111">*pChildContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f67-111">*pChildContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f67-112">Certificado del firmante para el que se va a buscar un certificado de emisor coincidente.</span><span class="sxs-lookup"><span data-stu-id="f2f67-112">The subject certificate for which to find a matching issuer certificate.</span></span>

</dd> <dt>

<span data-ttu-id="f2f67-113">*chStores* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f67-113">*chStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f67-114">Número de elementos de la matriz *pahStores* .</span><span class="sxs-lookup"><span data-stu-id="f2f67-114">The number of elements in the *pahStores* array.</span></span>

</dd> <dt>

<span data-ttu-id="f2f67-115">*pahStores* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f67-115">*pahStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f67-116">Matriz de almacenes de certificados en los que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="f2f67-116">An array of certificate stores in which to search.</span></span>

</dd> <dt>

<span data-ttu-id="f2f67-117">*psftVerifyAsOf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f67-117">*psftVerifyAsOf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f67-118">Hora de comprobación.</span><span class="sxs-lookup"><span data-stu-id="f2f67-118">The time of verification.</span></span>

</dd> <dt>

<span data-ttu-id="f2f67-119">*dwEncoding* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f67-119">*dwEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f67-120">Valor **DWORD** que especifica los tipos de codificación del certificado que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="f2f67-120">A **DWORD** value that specifies the encoding types of the certificate to check.</span></span> <span data-ttu-id="f2f67-121">Para obtener información sobre los posibles tipos de codificación, consulte [certificados y tipos de codificación de mensajes](certificate-and-message-encoding-types.md).</span><span class="sxs-lookup"><span data-stu-id="f2f67-121">For information about possible encoding types, see [Certificate and Message Encoding Types](certificate-and-message-encoding-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2f67-122">*pdwConfidence* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f2f67-122">*pdwConfidence* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f67-123">Este parámetro puede ser una combinación bit a bit de cero o más de los siguientes valores de confianza.</span><span class="sxs-lookup"><span data-stu-id="f2f67-123">This parameter can be a bitwise combination of zero or more of the following confidence values.</span></span>



| <span data-ttu-id="f2f67-124">Value</span><span class="sxs-lookup"><span data-stu-id="f2f67-124">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="f2f67-125">Significado</span><span class="sxs-lookup"><span data-stu-id="f2f67-125">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <span data-ttu-id="f2f67-126"><dt>**Certificado \_ de \_Firma de confianza**</dt> <dt> 0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="f2f67-126"><dt>**CERT\_CONFIDENCE\_SIG**</dt> <dt> 0x10000000</dt></span></span> </dl>                     | <span data-ttu-id="f2f67-127">La firma del certificado es válida.</span><span class="sxs-lookup"><span data-stu-id="f2f67-127">The signature of the certificate is valid.</span></span><br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <span data-ttu-id="f2f67-128"><dt>**Certificado \_ de 0x01000000 de \_ tiempo de confianza**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f2f67-128"><dt>**CERT\_CONFIDENCE\_TIME**</dt> <dt> 0x01000000</dt></span></span> </dl>                  | <span data-ttu-id="f2f67-129">La hora del emisor del certificado es válida.</span><span class="sxs-lookup"><span data-stu-id="f2f67-129">The time of the certificate issuer is valid.</span></span><br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <span data-ttu-id="f2f67-130"><dt> **Confianza de CERT \_ \_ TIMENEST**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="f2f67-130"><dt> **CERT\_CONFIDENCE\_TIMENEST**</dt> <dt>0x00100000</dt></span></span> </dl>    | <span data-ttu-id="f2f67-131">La hora del certificado es válida.</span><span class="sxs-lookup"><span data-stu-id="f2f67-131">The time of the certificate is valid.</span></span><br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <span data-ttu-id="f2f67-132"><dt> **Confianza de CERT \_ \_ AUTHIDEXT**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="f2f67-132"><dt> **CERT\_CONFIDENCE\_AUTHIDEXT**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="f2f67-133">La extensión de ID. de entidad es válida.</span><span class="sxs-lookup"><span data-stu-id="f2f67-133">The authority ID extension is valid.</span></span><br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <span data-ttu-id="f2f67-134"><dt>0x00001000</dt> de <dt> **\_ \_ higiene de confianza de certificados**</dt></span><span class="sxs-lookup"><span data-stu-id="f2f67-134"><dt> **CERT\_CONFIDENCE\_HYGIENE**</dt> <dt>0x00001000</dt></span></span> </dl>       | <span data-ttu-id="f2f67-135">Como mínimo, la firma de la extensión de identificador de entidad y certificado es válida.</span><span class="sxs-lookup"><span data-stu-id="f2f67-135">At a minimum, the signature of the certificate and authority ID extension are valid.</span></span><br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <span data-ttu-id="f2f67-136"><dt> **Confianza de certificado \_ \_ más alta**</dt> <dt>0x11111000</dt></span><span class="sxs-lookup"><span data-stu-id="f2f67-136"><dt> **CERT\_CONFIDENCE\_HIGHEST**</dt> <dt>0x11111000</dt></span></span> </dl>       | <span data-ttu-id="f2f67-137">Una combinación de todos los demás valores de confianza.</span><span class="sxs-lookup"><span data-stu-id="f2f67-137">A combination of all of the other confidence values.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="f2f67-138">*dwError* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f2f67-138">*dwError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f67-139">Un puntero a una variable **DWORD** que contiene el valor de error de este certificado, si procede.</span><span class="sxs-lookup"><span data-stu-id="f2f67-139">A pointer to a **DWORD** variable that contains the error value for this certificate, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2f67-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2f67-140">Return value</span></span>

<span data-ttu-id="f2f67-141">Un certificado de emisor que coincida con el certificado de firmante especificado por el parámetro *pChildContext* .</span><span class="sxs-lookup"><span data-stu-id="f2f67-141">An issuer certificate that matches the subject certificate specified by the *pChildContext* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2f67-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2f67-142">Remarks</span></span>

<span data-ttu-id="f2f67-143">Para encontrar correctamente un certificado de emisor coincidente, deben cumplirse los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="f2f67-143">To successfully find a matching issuer certificate, the following requirements must be met:</span></span>

-   <span data-ttu-id="f2f67-144">La firma del certificado de sujeto especificado por el parámetro *pChildContext* debe ser válida.</span><span class="sxs-lookup"><span data-stu-id="f2f67-144">The signature of the subject certificate specified by the *pChildContext* parameter must be valid.</span></span>
-   <span data-ttu-id="f2f67-145">El miembro **rgExtension** del miembro **PCertInfo** del parámetro *pChildContext* debe contener una estructura de [**\_ \_ \_ \_ información de identificador de clave de entidad emisora de certificados**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) .</span><span class="sxs-lookup"><span data-stu-id="f2f67-145">The **rgExtension** member of the **pCertInfo** member of the *pChildContext* parameter must contain a [**CERT\_AUTHORITY\_KEY\_ID\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) structure.</span></span> <span data-ttu-id="f2f67-146">Los miembros **CertIssuer** y **CertSerialMember** de esta estructura coinciden mucho con los miembros correspondientes del certificado del emisor.</span><span class="sxs-lookup"><span data-stu-id="f2f67-146">The **CertIssuer** and **CertSerialMember** members of this structure much match the corresponding members for the issuer certificate.</span></span>
-   <span data-ttu-id="f2f67-147">El valor del parámetro *psftVerifyAsOf* debe estar dentro del período de validez del certificado del firmante.</span><span class="sxs-lookup"><span data-stu-id="f2f67-147">The value of the *psftVerifyAsOf* parameter must be within the period of validity of the subject certificate.</span></span>
-   <span data-ttu-id="f2f67-148">El período de validez del certificado del firmante debe estar dentro del período de validez del certificado del emisor.</span><span class="sxs-lookup"><span data-stu-id="f2f67-148">The period of validity of the subject certificate must be within the period of validity of the issuer certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2f67-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2f67-149">Requirements</span></span>



| <span data-ttu-id="f2f67-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2f67-150">Requirement</span></span> | <span data-ttu-id="f2f67-151">Value</span><span class="sxs-lookup"><span data-stu-id="f2f67-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f67-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2f67-152">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f67-153">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f2f67-153">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f2f67-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2f67-154">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f67-155">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2f67-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2f67-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2f67-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2f67-157"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2f67-157"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 
