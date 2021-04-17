---
description: Especifica el nombre de la plantilla de certificado.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: 'ISCrdEnr:: setCertTemplateName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 53ba18626a7d2bb703ed4d11953fb4872cf9257c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687596"
---
# <a name="iscrdenrsetcerttemplatename-method"></a><span data-ttu-id="49d0f-103">ISCrdEnr:: setCertTemplateName (método)</span><span class="sxs-lookup"><span data-stu-id="49d0f-103">ISCrdEnr::setCertTemplateName method</span></span>

<span data-ttu-id="49d0f-104">El método **setCertTemplateName** especifica el nombre de la plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="49d0f-104">The **setCertTemplateName** method specifies the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="49d0f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49d0f-105">Syntax</span></span>


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="49d0f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49d0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49d0f-107">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49d0f-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49d0f-108">Valor que determina si se está configurando el nombre real o el nombre para mostrar de la plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="49d0f-108">Value which determines if the certificate template's real name or display name is being set.</span></span> <span data-ttu-id="49d0f-109">Si *dwFlags* tiene el valor de la \_ \_ \_ plantilla de certificado \_ \_ de inscripción, se establece el nombre para mostrar de la plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="49d0f-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is set.</span></span> <span data-ttu-id="49d0f-110">De lo contrario, se establece el nombre real de la plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="49d0f-110">Otherwise, the real name of the certificate template is set.</span></span>

</dd> <dt>

<span data-ttu-id="49d0f-111">*bstrCertTemplateName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49d0f-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49d0f-112">Nombre de la plantilla de certificado que se utilizará en la solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="49d0f-112">Name of the certificate template which will be used in the certificate request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49d0f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49d0f-113">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="49d0f-114">VB</span><span class="sxs-lookup"><span data-stu-id="49d0f-114">VB</span></span>

<span data-ttu-id="49d0f-115">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="49d0f-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="49d0f-116">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="49d0f-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="49d0f-117">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="49d0f-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="49d0f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49d0f-118">Remarks</span></span>

<span data-ttu-id="49d0f-119">Si no establece el nombre de la plantilla de certificado mediante una llamada a **ISCrdEnr:: setCertTemplateName**, el nombre tiene como valor predeterminado el nombre en la lista de plantillas de certificado disponibles.</span><span class="sxs-lookup"><span data-stu-id="49d0f-119">If you do not set the certificate template name by calling **ISCrdEnr::setCertTemplateName**, the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="49d0f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49d0f-120">Requirements</span></span>



| <span data-ttu-id="49d0f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="49d0f-121">Requirement</span></span> | <span data-ttu-id="49d0f-122">Value</span><span class="sxs-lookup"><span data-stu-id="49d0f-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49d0f-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49d0f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="49d0f-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="49d0f-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="49d0f-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49d0f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="49d0f-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="49d0f-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="49d0f-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49d0f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49d0f-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49d0f-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="49d0f-129">IID</span><span class="sxs-lookup"><span data-stu-id="49d0f-129">IID</span></span><br/>                      | <span data-ttu-id="49d0f-130">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="49d0f-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="49d0f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="49d0f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d0f-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="49d0f-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="49d0f-133">**ISCrdEnr::getCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="49d0f-133">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




