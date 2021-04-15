---
description: Devuelve el número de entidades de certificación (CA) que están dispuestos a emitir un certificado basado en la plantilla de certificado especificada.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: 'ISCrdEnr:: getCACount (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669659"
---
# <a name="iscrdenrgetcacount-method"></a><span data-ttu-id="0db76-103">ISCrdEnr:: getCACount (método)</span><span class="sxs-lookup"><span data-stu-id="0db76-103">ISCrdEnr::getCACount method</span></span>

<span data-ttu-id="0db76-104">El método **getCACount** devuelve el número de [*entidades de certificación*](../secgloss/c-gly.md) (CA) que están dispuestos a emitir un certificado basado en la plantilla de certificado especificada.</span><span class="sxs-lookup"><span data-stu-id="0db76-104">The **getCACount** method returns the number of [*certification authorities*](../secgloss/c-gly.md) (CAs) willing to issue a certificate based on the specified certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db76-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0db76-105">Syntax</span></span>


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a><span data-ttu-id="0db76-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0db76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db76-107">*bstrCertTemplateName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0db76-107">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db76-108">Cadena que representa el nombre de la plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="0db76-108">A string that represents the name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="0db76-109">*pdwCACount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0db76-109">*pdwCACount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0db76-110">Un puntero a un **valor Long** que devuelve el número de entidades de certificación disponibles que emitirá un certificado para la plantilla de certificado especificada en *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="0db76-110">A pointer to a **LONG** that returns the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0db76-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0db76-111">Return value</span></span>

### <a name="c"></a><span data-ttu-id="0db76-112">C++</span><span class="sxs-lookup"><span data-stu-id="0db76-112">C++</span></span>

<span data-ttu-id="0db76-113">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="0db76-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="0db76-114">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="0db76-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="0db76-115">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="0db76-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="0db76-116">VB</span><span class="sxs-lookup"><span data-stu-id="0db76-116">VB</span></span>

<span data-ttu-id="0db76-117">Un valor **Long** que representa el número de entidades de certificación disponibles que emitirá un certificado para la plantilla de certificado especificada en *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="0db76-117">A **Long** value that represents the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db76-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0db76-118">Requirements</span></span>



| <span data-ttu-id="0db76-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0db76-119">Requirement</span></span> | <span data-ttu-id="0db76-120">Value</span><span class="sxs-lookup"><span data-stu-id="0db76-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0db76-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0db76-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0db76-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0db76-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0db76-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0db76-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0db76-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0db76-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0db76-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0db76-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0db76-126"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0db76-126"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="0db76-127">IID</span><span class="sxs-lookup"><span data-stu-id="0db76-127">IID</span></span><br/>                      | <span data-ttu-id="0db76-128">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="0db76-128">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="0db76-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0db76-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db76-130">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="0db76-130">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="0db76-131">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="0db76-131">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="0db76-132">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="0db76-132">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 
