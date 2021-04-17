---
description: Firma el archivo especificado.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: SignerSign función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687908"
---
# <a name="signersign-function"></a><span data-ttu-id="c4fe9-103">SignerSign función)</span><span class="sxs-lookup"><span data-stu-id="c4fe9-103">SignerSign function</span></span>

<span data-ttu-id="c4fe9-104">La función **SignerSign** firma el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-104">The **SignerSign** function signs the specified file.</span></span>

> [!Note]  
> <span data-ttu-id="c4fe9-105">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="c4fe9-106">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c4fe9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4fe9-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="c4fe9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4fe9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4fe9-109">*pSubjectInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4fe9-109">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fe9-110">Puntero a una estructura de [**\_ \_ información de asunto del firmante**](signer-subject-info.md) que especifica el sujeto que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-110">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="c4fe9-111">*pSignerCert* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4fe9-111">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fe9-112">Puntero a una estructura de [**\_ certificado de firmante**](signer-cert.md) que especifica el certificado que se va a utilizar para crear la firma digital.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-112">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="c4fe9-113">*pSignatureInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4fe9-113">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fe9-114">Puntero a una estructura de [**\_ \_ información de firma de firmante**](signer-signature-info.md) que contiene información sobre la firma digital.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-114">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="c4fe9-115">*pProviderInfo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c4fe9-115">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fe9-116">Puntero a una estructura de [**\_ \_ información del proveedor de firmante**](signer-provider-info.md) que especifica el proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) y la información de [*clave privada*](../secgloss/p-gly.md) que se usa para crear la firma digital.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-116">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and [*private key*](../secgloss/p-gly.md) information used to create the digital signature.</span></span>

<span data-ttu-id="c4fe9-117">Si el valor de este parámetro es **null**, el valor del parámetro *pSignerCert* debe especificar un certificado asociado a un CSP.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-117">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="c4fe9-118">*pwszHttpTimeStamp* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c4fe9-118">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fe9-119">Dirección URL de un servidor de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-119">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="c4fe9-120">*psRequest* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c4fe9-120">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fe9-121">Puntero a una matriz de estructuras [**de \_ atributo de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) que se agregan a una solicitud de firma.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-121">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="c4fe9-122">Este parámetro se omite si el parámetro *pwszHttpTimeStamp* no contiene un valor válido que no sea **null**.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-122">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c4fe9-123">*pSipData* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c4fe9-123">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fe9-124">Valor de 32 bits que se pasa como datos adicionales a las funciones de SIP.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-124">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="c4fe9-125">El proveedor SIP define el formato y el contenido de este.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-125">The format and content of this is defined by the SIP provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4fe9-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4fe9-126">Return value</span></span>

<span data-ttu-id="c4fe9-127">Si la función se ejecuta correctamente, la función devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-127">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="c4fe9-128">Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-128">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="c4fe9-129">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="c4fe9-129">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4fe9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4fe9-130">Requirements</span></span>



| <span data-ttu-id="c4fe9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4fe9-131">Requirement</span></span> | <span data-ttu-id="c4fe9-132">Value</span><span class="sxs-lookup"><span data-stu-id="c4fe9-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fe9-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4fe9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c4fe9-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c4fe9-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c4fe9-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4fe9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c4fe9-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4fe9-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c4fe9-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4fe9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4fe9-138"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4fe9-138"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4fe9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4fe9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4fe9-140">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="c4fe9-140">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
