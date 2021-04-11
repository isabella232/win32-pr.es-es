---
description: Recupera el nombre de la plantilla de certificado.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: 'ISCrdEnr:: getCertTemplateName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278801"
---
# <a name="iscrdenrgetcerttemplatename-method"></a><span data-ttu-id="f9272-103">ISCrdEnr:: getCertTemplateName (método)</span><span class="sxs-lookup"><span data-stu-id="f9272-103">ISCrdEnr::getCertTemplateName method</span></span>

<span data-ttu-id="f9272-104">El método **getCertTemplateName** recupera el nombre de la plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="f9272-104">The **getCertTemplateName** method retrieves the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9272-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9272-105">Syntax</span></span>


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="f9272-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9272-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9272-107">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f9272-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9272-108">Valor que determina si se devuelve el nombre real o el nombre para mostrar de la plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="f9272-108">A value that determines whether the certificate template's real name or display name is returned.</span></span> <span data-ttu-id="f9272-109">Si *dwFlags* tiene el valor PPAC inscribir el nombre para mostrar de la plantilla de certificado \_ \_ \_ \_ \_ , se recupera el nombre para mostrar de la plantilla de certificado; de lo contrario, se muestra el nombre real de la plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="f9272-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is retrieved; otherwise, the real name of the certificate template is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="f9272-110">*pbstrCertTemplateName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9272-110">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9272-111">Un puntero a una cadena que devuelve el nombre de la plantilla de certificado que se utilizará en la [*solicitud de certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f9272-111">A pointer to a string that returns the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9272-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9272-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="f9272-113">C++</span><span class="sxs-lookup"><span data-stu-id="f9272-113">C++</span></span>

<span data-ttu-id="f9272-114">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="f9272-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="f9272-115">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="f9272-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="f9272-116">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="f9272-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="f9272-117">VB</span><span class="sxs-lookup"><span data-stu-id="f9272-117">VB</span></span>

<span data-ttu-id="f9272-118">Cadena que representa el nombre de la plantilla de certificado que se utilizará en la [*solicitud de certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f9272-118">A string that represents the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f9272-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9272-119">Remarks</span></span>

<span data-ttu-id="f9272-120">Si no establece el nombre de la plantilla de certificado mediante una llamada a [**ISCrdEnr:: setCertTemplateName**](iscrdenr-setcerttemplatename.md), el nombre tiene como valor predeterminado el nombre en la lista de plantillas de certificado disponibles.</span><span class="sxs-lookup"><span data-stu-id="f9272-120">If you do not set the certificate template name by calling [**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md), the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9272-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9272-121">Requirements</span></span>



| <span data-ttu-id="f9272-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9272-122">Requirement</span></span> | <span data-ttu-id="f9272-123">Value</span><span class="sxs-lookup"><span data-stu-id="f9272-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9272-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9272-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f9272-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f9272-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f9272-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9272-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f9272-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9272-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9272-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9272-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9272-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9272-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="f9272-130">IID</span><span class="sxs-lookup"><span data-stu-id="f9272-130">IID</span></span><br/>                      | <span data-ttu-id="f9272-131">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="f9272-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f9272-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9272-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9272-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="f9272-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="f9272-134">**ISCrdEnr::setCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="f9272-134">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
