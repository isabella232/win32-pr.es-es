---
description: Se usa para determinar si una plantilla de certificado contiene el uso de la \_ clave de \_ protección del correo electrónico szOID PKIX KP \_ \_ .
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: 'ISCrdEnr:: getCertTemplateSMIME (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4ed66af6a8a91855fbfc5a972a8bf00358314663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912017"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a><span data-ttu-id="33367-103">ISCrdEnr:: getCertTemplateSMIME (método)</span><span class="sxs-lookup"><span data-stu-id="33367-103">ISCrdEnr::getCertTemplateSMIME method</span></span>

<span data-ttu-id="33367-104">El método **getCertTemplateSMIME** se usa para determinar si una plantilla de certificado contiene el \_ uso de claves de protección de correo electrónico de szOID PKIX \_ PK \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="33367-104">The **getCertTemplateSMIME** method is used to determine whether a certificate template contains the szOID\_PKIX\_KP\_EMAIL\_PROTECTION key usage.</span></span>

<span data-ttu-id="33367-105">Si el uso de esta clave forma parte de la plantilla de certificado, la plantilla de certificado admite operaciones de [*extensiones seguras multipropósito de correo Internet*](../secgloss/s-gly.md) (S/MIME).</span><span class="sxs-lookup"><span data-stu-id="33367-105">If this key usage is part of the certificate template, the certificate template supports [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="33367-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33367-106">Syntax</span></span>


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a><span data-ttu-id="33367-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33367-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33367-108">*bstrCertTemplateName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33367-108">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33367-109">Nombre del certificado que se consulta para el uso de la clave S/MIME.</span><span class="sxs-lookup"><span data-stu-id="33367-109">The name of the certificate being queried for the S/MIME key usage.</span></span>

</dd> <dt>

<span data-ttu-id="33367-110">*pdwCertTemplateSMIME* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="33367-110">*pdwCertTemplateSMIME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33367-111">Un puntero a un **DWORD** que devuelve un valor de uno si *bstrCertTemplateName* admite S/MIME; en caso contrario, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="33367-111">A pointer to a **DWORD** that returns a value of one if *bstrCertTemplateName* supports S/MIME; otherwise it returns zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33367-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33367-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="33367-113">C++</span><span class="sxs-lookup"><span data-stu-id="33367-113">C++</span></span>

<span data-ttu-id="33367-114">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="33367-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="33367-115">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="33367-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="33367-116">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="33367-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="33367-117">VB</span><span class="sxs-lookup"><span data-stu-id="33367-117">VB</span></span>

<span data-ttu-id="33367-118">Valor **Long** de uno si *bstrCertTemplateName* admite S/MIME; de lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="33367-118">**Long** value of one if *bstrCertTemplateName* supports S/MIME; otherwise zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="33367-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33367-119">Remarks</span></span>

<span data-ttu-id="33367-120">La constante para la \_ \_ protección de correo electrónico szOID PKIX KP \_ \_ se define en Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="33367-120">The constant for szOID\_PKIX\_KP\_EMAIL\_PROTECTION is defined in Wincrypt.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="33367-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33367-121">Requirements</span></span>



| <span data-ttu-id="33367-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="33367-122">Requirement</span></span> | <span data-ttu-id="33367-123">Value</span><span class="sxs-lookup"><span data-stu-id="33367-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33367-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33367-124">Minimum supported client</span></span><br/> | <span data-ttu-id="33367-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="33367-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="33367-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33367-126">Minimum supported server</span></span><br/> | <span data-ttu-id="33367-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="33367-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="33367-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="33367-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33367-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33367-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="33367-130">IID</span><span class="sxs-lookup"><span data-stu-id="33367-130">IID</span></span><br/>                      | <span data-ttu-id="33367-131">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="33367-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="33367-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="33367-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33367-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="33367-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="33367-134">[**ISCrdEnr:: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33367-134">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 
