---
description: Enumera los nombres de las plantillas de certificado.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: 'ISCrdEnr:: enumCertTemplateName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a0a4850143cac48ef9b9b853f99153d4daeb4366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669660"
---
# <a name="iscrdenrenumcerttemplatename-method"></a><span data-ttu-id="23fe4-103">ISCrdEnr:: enumCertTemplateName (método)</span><span class="sxs-lookup"><span data-stu-id="23fe4-103">ISCrdEnr::enumCertTemplateName method</span></span>

<span data-ttu-id="23fe4-104">El método **enumCertTemplateName** enumera los nombres de las plantillas de certificado.</span><span class="sxs-lookup"><span data-stu-id="23fe4-104">The **enumCertTemplateName** method enumerates the certificate template names.</span></span>

## <a name="syntax"></a><span data-ttu-id="23fe4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23fe4-105">Syntax</span></span>


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="23fe4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23fe4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23fe4-107">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23fe4-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23fe4-108">Índice de base cero de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="23fe4-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="23fe4-109">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23fe4-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23fe4-110">Un valor que determina si la plantilla de certificado enumerada se aplica a los certificados de usuario o de equipo.</span><span class="sxs-lookup"><span data-stu-id="23fe4-110">A value that determines whether the enumerated certificate template applies to user or machine certificates.</span></span> <span data-ttu-id="23fe4-111">Si este valor es una plantilla de certificado de \_ usuario de inscripción PPAC \_ \_ \_ (definida como 1), la enumeración se aplica a las plantillas de certificado de usuario.</span><span class="sxs-lookup"><span data-stu-id="23fe4-111">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1), the enumeration applies to user certificate templates.</span></span> <span data-ttu-id="23fe4-112">Si este valor es PPAC inscribir la plantilla de certificado de la \_ \_ máquina \_ \_ (definida como 2), la enumeración se aplica a las plantillas de certificado de equipo.</span><span class="sxs-lookup"><span data-stu-id="23fe4-112">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2), the enumeration applies to machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="23fe4-113">*pbstrCertTemplateName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="23fe4-113">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23fe4-114">Puntero a una cadena que devuelve el nombre de la plantilla de certificado enumerada.</span><span class="sxs-lookup"><span data-stu-id="23fe4-114">A pointer to a string that returns the name of the enumerated certificate template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23fe4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23fe4-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="23fe4-116">C++</span><span class="sxs-lookup"><span data-stu-id="23fe4-116">C++</span></span>

<span data-ttu-id="23fe4-117">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="23fe4-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="23fe4-118">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="23fe4-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="23fe4-119">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="23fe4-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="23fe4-120">VB</span><span class="sxs-lookup"><span data-stu-id="23fe4-120">VB</span></span>

<span data-ttu-id="23fe4-121">Cadena que contiene el nombre de la plantilla de certificado enumerada.</span><span class="sxs-lookup"><span data-stu-id="23fe4-121">A string that contains the name of the enumerated certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="23fe4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23fe4-122">Requirements</span></span>



| <span data-ttu-id="23fe4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="23fe4-123">Requirement</span></span> | <span data-ttu-id="23fe4-124">Value</span><span class="sxs-lookup"><span data-stu-id="23fe4-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23fe4-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23fe4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="23fe4-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="23fe4-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="23fe4-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23fe4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="23fe4-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="23fe4-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23fe4-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23fe4-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23fe4-130"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23fe4-130"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="23fe4-131">IID</span><span class="sxs-lookup"><span data-stu-id="23fe4-131">IID</span></span><br/>                      | <span data-ttu-id="23fe4-132">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="23fe4-132">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="23fe4-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="23fe4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23fe4-134">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="23fe4-134">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="23fe4-135">**ISCrdEnr::getCertTemplateCount**</span><span class="sxs-lookup"><span data-stu-id="23fe4-135">**ISCrdEnr::getCertTemplateCount**</span></span>](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[<span data-ttu-id="23fe4-136">**ISCrdEnr::getCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="23fe4-136">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[<span data-ttu-id="23fe4-137">**ISCrdEnr::setCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="23fe4-137">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




