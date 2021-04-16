---
description: Recupera el nombre del firmante del certificado de firma.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: 'ISCrdEnr:: getSigningCertificateName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8d9a8a84067e82a18e5066721f3e7f39d075c339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423960"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a><span data-ttu-id="51cbe-103">ISCrdEnr:: getSigningCertificateName (método)</span><span class="sxs-lookup"><span data-stu-id="51cbe-103">ISCrdEnr::getSigningCertificateName method</span></span>

<span data-ttu-id="51cbe-104">El método **getSigningCertificateName** recupera el nombre del firmante del certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="51cbe-104">The **getSigningCertificateName** method retrieves the subject name from the signing certificate.</span></span>

<span data-ttu-id="51cbe-105">Este método también se puede utilizar para mostrar el certificado en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="51cbe-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="51cbe-106">Este método llama a la función [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)de [*CryptoAPI*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="51cbe-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="51cbe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51cbe-107">Syntax</span></span>


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="51cbe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51cbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51cbe-109">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51cbe-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51cbe-110">Valor que determina si el certificado se muestra en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="51cbe-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="51cbe-111">Si este valor es PPAC \_ inscribir \_ no \_ Mostrar \_ certificado (definido como 0x01), no se muestra el certificado de firma; cualquier otro valor da lugar a que el certificado de firma se muestre en el cuadro de diálogo **certificado** .</span><span class="sxs-lookup"><span data-stu-id="51cbe-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the signing certificate is not displayed; any other values result in the signing certificate being displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="51cbe-112">*pbstrSigningCertName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="51cbe-112">*pbstrSigningCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51cbe-113">Puntero a una cadena que devuelve el nombre del certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="51cbe-113">A pointer to a string that returns the name of the signing certificate.</span></span> <span data-ttu-id="51cbe-114">El certificado de firma se usará para firmar la [*solicitud de certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="51cbe-114">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51cbe-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51cbe-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="51cbe-116">C++</span><span class="sxs-lookup"><span data-stu-id="51cbe-116">C++</span></span>

<span data-ttu-id="51cbe-117">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="51cbe-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="51cbe-118">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="51cbe-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="51cbe-119">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="51cbe-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="51cbe-120">VB</span><span class="sxs-lookup"><span data-stu-id="51cbe-120">VB</span></span>

<span data-ttu-id="51cbe-121">Cadena que representa el nombre del certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="51cbe-121">A string that represents the name of the signing certificate.</span></span> <span data-ttu-id="51cbe-122">El certificado de firma se usará para firmar la [*solicitud de certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="51cbe-122">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="51cbe-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51cbe-123">Remarks</span></span>

<span data-ttu-id="51cbe-124">El método **getSigningCertificateName** devuelve el nombre de sujeto del certificado que ha seleccionado (u otro administrador) en una llamada correcta anterior a [**ISCrdEnr:: selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) o [**ISCrdEnr:: setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="51cbe-124">The **getSigningCertificateName** method returns the subject name of the certificate you (or another administrator) have selected in a previous successful call to [**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) or [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span> <span data-ttu-id="51cbe-125">Este método llama a la función [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para recuperar el nombre de sujeto según la secuencia descrita para el \_ \_ \_ \_ valor de tipo de presentación simple de nombre de certificado del parámetro *dwType* de **CertGetNameString**.</span><span class="sxs-lookup"><span data-stu-id="51cbe-125">This method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the subject name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="51cbe-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51cbe-126">Requirements</span></span>



| <span data-ttu-id="51cbe-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="51cbe-127">Requirement</span></span> | <span data-ttu-id="51cbe-128">Value</span><span class="sxs-lookup"><span data-stu-id="51cbe-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51cbe-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51cbe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="51cbe-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="51cbe-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="51cbe-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51cbe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="51cbe-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="51cbe-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="51cbe-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="51cbe-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51cbe-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51cbe-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="51cbe-135">IID</span><span class="sxs-lookup"><span data-stu-id="51cbe-135">IID</span></span><br/>                      | <span data-ttu-id="51cbe-136">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="51cbe-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="51cbe-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="51cbe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51cbe-138">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="51cbe-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="51cbe-139">**ISCrdEnr::selectSigningCertificate**</span><span class="sxs-lookup"><span data-stu-id="51cbe-139">**ISCrdEnr::selectSigningCertificate**</span></span>](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
