---
description: Especifica un certificado de firma (también conocido como certificado de agente de inscripción).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: 'ISCrdEnr:: setSigningCertificate (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669890"
---
# <a name="iscrdenrsetsigningcertificate-method"></a><span data-ttu-id="0ddad-103">ISCrdEnr:: setSigningCertificate (método)</span><span class="sxs-lookup"><span data-stu-id="0ddad-103">ISCrdEnr::setSigningCertificate method</span></span>

<span data-ttu-id="0ddad-104">El método **setSigningCertificate** especifica un certificado de firma (también conocido como *certificado de agente de inscripción*).</span><span class="sxs-lookup"><span data-stu-id="0ddad-104">The **setSigningCertificate** method specifies a signing certificate (also known as the *enrollment agent certificate*).</span></span>

<span data-ttu-id="0ddad-105">Antes de inscribirse en nombre de los usuarios, debe seleccionar o establecer un certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="0ddad-105">Before enrolling on behalf of users, you must select or set a signing certificate.</span></span> <span data-ttu-id="0ddad-106">La [*clave privada*](../secgloss/p-gly.md) asociada a este certificado de firma se usa para firmar una \# solicitud PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="0ddad-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="0ddad-107">El archivo PKCS \# 7, a su vez, contiene la solicitud PKCS 10 del usuario \# (que está firmada con la clave privada del usuario).</span><span class="sxs-lookup"><span data-stu-id="0ddad-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ddad-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ddad-108">Syntax</span></span>


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="0ddad-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ddad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ddad-110">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ddad-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ddad-111">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0ddad-111">Reserved for future use.</span></span> <span data-ttu-id="0ddad-112">Establezca este valor en cero.</span><span class="sxs-lookup"><span data-stu-id="0ddad-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="0ddad-113">*bstrCertTemplateName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ddad-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ddad-114">Nombre de la plantilla de certificado para el certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="0ddad-114">Name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="0ddad-115">Puede usar el valor "EnrollmentAgent" Si ha obtenido un certificado EnrollmentAgent.</span><span class="sxs-lookup"><span data-stu-id="0ddad-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ddad-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ddad-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="0ddad-117">VB</span><span class="sxs-lookup"><span data-stu-id="0ddad-117">VB</span></span>

<span data-ttu-id="0ddad-118">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="0ddad-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="0ddad-119">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="0ddad-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="0ddad-120">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="0ddad-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ddad-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ddad-121">Remarks</span></span>

<span data-ttu-id="0ddad-122">Antes de inscribirse en nombre de un usuario, primero debe obtener un certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="0ddad-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="0ddad-123">Puede obtener un certificado de firma mediante el complemento MMC del administrador de certificados.</span><span class="sxs-lookup"><span data-stu-id="0ddad-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="0ddad-124">El método **setSigningCertificate** no obtiene el certificado de firma, pero informa al control de inscripción de tarjetas inteligentes que ha obtenido previamente el certificado de firma que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="0ddad-124">The **setSigningCertificate** method does not obtain the signing certificate but informs the Smart Card Enrollment Control which previously obtained signing certificate to use.</span></span> <span data-ttu-id="0ddad-125">El método **setSigningCertificate** busca el certificado de firma más reciente correspondiente a la plantilla de certificado especificada por *bstrCertTemplateName* en el almacén "My" del llamador.</span><span class="sxs-lookup"><span data-stu-id="0ddad-125">The **setSigningCertificate** method searches the caller's "My" store for the most recent signing certificate corresponding to the certificate template specified by *bstrCertTemplateName*.</span></span>

<span data-ttu-id="0ddad-126">Una alternativa a **setSigningCertificate** es **ISCrdEnr:: setSigningCertificate**.</span><span class="sxs-lookup"><span data-stu-id="0ddad-126">An alternative to **setSigningCertificate** is **ISCrdEnr::setSigningCertificate**.</span></span>

<span data-ttu-id="0ddad-127">Después de establecer un certificado de firma, su nombre se puede recuperar llamando a [**ISCrdEnr:: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span><span class="sxs-lookup"><span data-stu-id="0ddad-127">After a signing certificate is set, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ddad-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ddad-128">Requirements</span></span>



| <span data-ttu-id="0ddad-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ddad-129">Requirement</span></span> | <span data-ttu-id="0ddad-130">Value</span><span class="sxs-lookup"><span data-stu-id="0ddad-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ddad-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ddad-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0ddad-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0ddad-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0ddad-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ddad-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0ddad-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ddad-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0ddad-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0ddad-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ddad-136"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ddad-136"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="0ddad-137">IID</span><span class="sxs-lookup"><span data-stu-id="0ddad-137">IID</span></span><br/>                      | <span data-ttu-id="0ddad-138">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="0ddad-138">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="0ddad-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ddad-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ddad-140">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="0ddad-140">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="0ddad-141">**ISCrdEnr::getSigningCertificateName**</span><span class="sxs-lookup"><span data-stu-id="0ddad-141">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
