---
description: 'Recupera el nombre del certificado resultante de una llamada correcta anterior a ISCrdEnr:: ENROLL.'
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: 'ISCrdEnr:: getEnrolledCertificateName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3c9640e7719d2b5ac0e576384246cda5e1b2bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688189"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a><span data-ttu-id="8ceba-103">ISCrdEnr:: getEnrolledCertificateName (método)</span><span class="sxs-lookup"><span data-stu-id="8ceba-103">ISCrdEnr::getEnrolledCertificateName method</span></span>

<span data-ttu-id="8ceba-104">El método **getEnrolledCertificateName** recupera el nombre del certificado resultante de una llamada correcta anterior a [**ISCrdEnr:: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ceba-104">The **getEnrolledCertificateName** method retrieves the name of the certificate resulting from an earlier successful call to [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).</span></span>

<span data-ttu-id="8ceba-105">Este método también se puede utilizar para mostrar el certificado en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8ceba-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="8ceba-106">Este método llama a la función [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)de [*CryptoAPI*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8ceba-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ceba-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ceba-107">Syntax</span></span>


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="8ceba-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ceba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ceba-109">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ceba-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ceba-110">Valor que determina si el certificado se muestra en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8ceba-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="8ceba-111">Si este valor es PPAC \_ inscribir \_ no \_ Mostrar \_ certificado (definido como 0x01), no se muestra el certificado inscrito; cualquier otro valor hace que el certificado inscrito se muestre en el cuadro de diálogo **certificado** .</span><span class="sxs-lookup"><span data-stu-id="8ceba-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the enrolled certificate is not displayed; any other values cause the enrolled certificate to be displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="8ceba-112">*pBstrCertName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8ceba-112">*pBstrCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ceba-113">Puntero a una cadena que devuelve el nombre del certificado recuperado.</span><span class="sxs-lookup"><span data-stu-id="8ceba-113">A pointer to a string that returns the retrieved certificate name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ceba-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ceba-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="8ceba-115">C++</span><span class="sxs-lookup"><span data-stu-id="8ceba-115">C++</span></span>

<span data-ttu-id="8ceba-116">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="8ceba-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="8ceba-117">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="8ceba-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="8ceba-118">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="8ceba-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="8ceba-119">VB</span><span class="sxs-lookup"><span data-stu-id="8ceba-119">VB</span></span>

<span data-ttu-id="8ceba-120">Cadena que representa el nombre del certificado recuperado.</span><span class="sxs-lookup"><span data-stu-id="8ceba-120">A string that represents the retrieved certificate name.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ceba-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ceba-121">Remarks</span></span>

<span data-ttu-id="8ceba-122">Dado que este método funciona en un certificado existente, debe haber llamado correctamente a [**ISCrdEnr:: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) antes de poder llamar a **getEnrolledCertificateName**.</span><span class="sxs-lookup"><span data-stu-id="8ceba-122">Because this method operates on an existing certificate, you must have successfully called [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) before you can call **getEnrolledCertificateName**.</span></span>

<span data-ttu-id="8ceba-123">El método **getEnrolledCertificateName** llama a la función [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para recuperar el nombre del certificado según la secuencia descrita para el \_ \_ \_ \_ valor de tipo de presentación simple de nombre de certificado del parámetro *dwType* de **CertGetNameString**.</span><span class="sxs-lookup"><span data-stu-id="8ceba-123">The **getEnrolledCertificateName** method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the certificate name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ceba-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ceba-124">Requirements</span></span>



| <span data-ttu-id="8ceba-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ceba-125">Requirement</span></span> | <span data-ttu-id="8ceba-126">Value</span><span class="sxs-lookup"><span data-stu-id="8ceba-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ceba-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ceba-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8ceba-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8ceba-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8ceba-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ceba-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8ceba-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ceba-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8ceba-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ceba-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ceba-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ceba-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="8ceba-133">IID</span><span class="sxs-lookup"><span data-stu-id="8ceba-133">IID</span></span><br/>                      | <span data-ttu-id="8ceba-134">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="8ceba-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="8ceba-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ceba-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ceba-136">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="8ceba-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="8ceba-137">[**ISCrdEnr:: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8ceba-137">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 
