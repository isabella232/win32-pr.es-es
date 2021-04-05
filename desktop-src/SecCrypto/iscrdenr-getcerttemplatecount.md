---
description: Recupera el número de plantillas de certificado.
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: 'ISCrdEnr:: getCertTemplateCount (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 86a78f03929bc6cdcfc7b611944b81c59a1c9fc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912826"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a><span data-ttu-id="5e0f7-103">ISCrdEnr:: getCertTemplateCount (método)</span><span class="sxs-lookup"><span data-stu-id="5e0f7-103">ISCrdEnr::getCertTemplateCount method</span></span>

<span data-ttu-id="5e0f7-104">El método **getCertTemplateCount** recupera el número de plantillas de certificado.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-104">The **getCertTemplateCount** method retrieves the number of certificate templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e0f7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e0f7-105">Syntax</span></span>


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a><span data-ttu-id="5e0f7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e0f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e0f7-107">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e0f7-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0f7-108">Un valor que determina si la plantilla es para certificados de usuario o de equipo.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-108">A value that determines whether the template is for user or machine certificates.</span></span> <span data-ttu-id="5e0f7-109">Si este valor es \_ \_ la plantilla de certificado de usuario SCard ENROLL \_ \_ (definida como 1), el recuento devuelto será para las plantillas de certificado de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-109">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1) then the returned count will be for user certificate templates.</span></span> <span data-ttu-id="5e0f7-110">Si este valor es PPAC \_ inscribir \_ \_ la plantilla de certificado de la máquina \_ (definida como 2), el recuento devuelto será para las plantillas de certificado de equipo.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-110">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2) then the returned count will be for machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="5e0f7-111">*pdwCertTemplateCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5e0f7-111">*pdwCertTemplateCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0f7-112">Un puntero a un **Long** que devuelve el número de plantillas de certificado.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-112">A pointer to a **LONG** that returns the number of certificate templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e0f7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e0f7-113">Return value</span></span>

### <a name="c"></a><span data-ttu-id="5e0f7-114">C++</span><span class="sxs-lookup"><span data-stu-id="5e0f7-114">C++</span></span>

<span data-ttu-id="5e0f7-115">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="5e0f7-116">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="5e0f7-117">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="5e0f7-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="5e0f7-118">VB</span><span class="sxs-lookup"><span data-stu-id="5e0f7-118">VB</span></span>

<span data-ttu-id="5e0f7-119">Un valor de **tipo Long** que representa el número de plantillas de certificado.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-119">A **Long** value that represents the number of certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e0f7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e0f7-120">Requirements</span></span>



| <span data-ttu-id="5e0f7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e0f7-121">Requirement</span></span> | <span data-ttu-id="5e0f7-122">Value</span><span class="sxs-lookup"><span data-stu-id="5e0f7-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e0f7-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e0f7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5e0f7-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5e0f7-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5e0f7-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e0f7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5e0f7-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e0f7-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5e0f7-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e0f7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e0f7-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e0f7-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="5e0f7-129">IID</span><span class="sxs-lookup"><span data-stu-id="5e0f7-129">IID</span></span><br/>                      | <span data-ttu-id="5e0f7-130">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="5e0f7-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="5e0f7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e0f7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e0f7-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="5e0f7-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="5e0f7-133">**ISCrdEnr::enumCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="5e0f7-133">**ISCrdEnr::enumCertTemplateName**</span></span>](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 




