---
description: Muestra un cuadro de diálogo Seleccionar certificado, que permite seleccionar un certificado de firma (también conocido como certificado de agente de inscripción).
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: 'ISCrdEnr:: selectSigningCertificate (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912825"
---
# <a name="iscrdenrselectsigningcertificate-method"></a><span data-ttu-id="9a0dd-103">ISCrdEnr:: selectSigningCertificate (método)</span><span class="sxs-lookup"><span data-stu-id="9a0dd-103">ISCrdEnr::selectSigningCertificate method</span></span>

<span data-ttu-id="9a0dd-104">El método **selectSigningCertificate** muestra el cuadro de diálogo **seleccionar certificado** , que permite seleccionar un certificado de firma (también conocido como *certificado de agente de inscripción*).</span><span class="sxs-lookup"><span data-stu-id="9a0dd-104">The **selectSigningCertificate** method displays a **Select Certificate** dialog box, allowing a signing certificate (also known as the *enrollment agent certificate*) to be selected.</span></span>

<span data-ttu-id="9a0dd-105">Antes de inscribirse en nombre de los usuarios, debe seleccionar un certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="9a0dd-105">Before enrolling on behalf of users, you must select a signing certificate.</span></span> <span data-ttu-id="9a0dd-106">La [*clave privada*](../secgloss/p-gly.md) asociada a este certificado de firma se usa para firmar una \# solicitud PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="9a0dd-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="9a0dd-107">El archivo PKCS \# 7, a su vez, contiene la solicitud PKCS 10 del usuario \# (que está firmada con la clave privada del usuario).</span><span class="sxs-lookup"><span data-stu-id="9a0dd-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a0dd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a0dd-108">Syntax</span></span>


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="9a0dd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a0dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a0dd-110">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9a0dd-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a0dd-111">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="9a0dd-111">Reserved for future use.</span></span> <span data-ttu-id="9a0dd-112">Establezca este valor en cero.</span><span class="sxs-lookup"><span data-stu-id="9a0dd-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="9a0dd-113">*bstrCertTemplateName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9a0dd-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a0dd-114">Cadena que representa el nombre de la plantilla de certificado para el certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="9a0dd-114">A string that represents the name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="9a0dd-115">Puede usar el valor "EnrollmentAgent" Si ha obtenido un certificado EnrollmentAgent.</span><span class="sxs-lookup"><span data-stu-id="9a0dd-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a0dd-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a0dd-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="9a0dd-117">VB</span><span class="sxs-lookup"><span data-stu-id="9a0dd-117">VB</span></span>

<span data-ttu-id="9a0dd-118">Si el método se ejecuta correctamente, el método devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9a0dd-118">If the method succeeds, the method returns **S\_OK**.</span></span>

<span data-ttu-id="9a0dd-119">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="9a0dd-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="9a0dd-120">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="9a0dd-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a0dd-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a0dd-121">Remarks</span></span>

<span data-ttu-id="9a0dd-122">Antes de inscribirse en nombre de un usuario, primero debe obtener un certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="9a0dd-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="9a0dd-123">Puede obtener un certificado de firma mediante el complemento MMC del administrador de certificados.</span><span class="sxs-lookup"><span data-stu-id="9a0dd-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="9a0dd-124">El método **selectSigningCertificate** no obtiene el certificado de firma, pero muestra un cuadro de diálogo de certificados de firma previamente obtenidos, lo que le permite elegir qué certificado se usará para firmar las solicitudes de inscripción en nombre.</span><span class="sxs-lookup"><span data-stu-id="9a0dd-124">The **selectSigningCertificate** method does not obtain the signing certificate but displays a dialog box of previously obtained signing certificates, allowing you to choose which certificate will be used to sign the enroll-on-behalf requests.</span></span>

<span data-ttu-id="9a0dd-125">Una alternativa a **selectSigningCertificate** es [**ISCrdEnr:: setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="9a0dd-125">An alternative to **selectSigningCertificate** is [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span>

<span data-ttu-id="9a0dd-126">Una vez que se selecciona un certificado de firma, su nombre se puede recuperar llamando a [**ISCrdEnr:: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span><span class="sxs-lookup"><span data-stu-id="9a0dd-126">After a signing certificate is selected, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0dd-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a0dd-127">Requirements</span></span>



| <span data-ttu-id="9a0dd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a0dd-128">Requirement</span></span> | <span data-ttu-id="9a0dd-129">Value</span><span class="sxs-lookup"><span data-stu-id="9a0dd-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0dd-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a0dd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9a0dd-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9a0dd-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9a0dd-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a0dd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9a0dd-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a0dd-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9a0dd-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a0dd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a0dd-135"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a0dd-135"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="9a0dd-136">IID</span><span class="sxs-lookup"><span data-stu-id="9a0dd-136">IID</span></span><br/>                      | <span data-ttu-id="9a0dd-137">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="9a0dd-137">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="9a0dd-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a0dd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0dd-139">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="9a0dd-139">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="9a0dd-140">**ISCrdEnr::getSigningCertificateName**</span><span class="sxs-lookup"><span data-stu-id="9a0dd-140">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
