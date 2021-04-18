---
description: Enumera el nombre de las entidades de certificación (CA) para un nombre de plantilla de certificado determinado.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: 'ISCrdEnr:: enumCAName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: c23df2f74cdf3791f1280e38cbff8ddd48f924b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688432"
---
# <a name="iscrdenrenumcaname-method"></a><span data-ttu-id="0d73d-103">ISCrdEnr:: enumCAName (método)</span><span class="sxs-lookup"><span data-stu-id="0d73d-103">ISCrdEnr::enumCAName method</span></span>

<span data-ttu-id="0d73d-104">El método **enumCAName** enumera el nombre de las [*entidades de certificación*](../secgloss/c-gly.md) (CA) para un nombre de plantilla de certificado determinado.</span><span class="sxs-lookup"><span data-stu-id="0d73d-104">The **enumCAName** method enumerates the name of the [*certification authorities*](../secgloss/c-gly.md) (CAs) for a given certificate template name.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d73d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d73d-105">Syntax</span></span>


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="0d73d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d73d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d73d-107">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d73d-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d73d-108">Índice de base cero de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="0d73d-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="0d73d-109">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d73d-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d73d-110">Un valor que determina si el nombre hace referencia al nombre de la entidad de certificación o al nombre del equipo de la CA.</span><span class="sxs-lookup"><span data-stu-id="0d73d-110">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="0d73d-111">Si este valor es PPAC \_ ENROLL \_ CA nombre del \_ equipo \_ (definido como 0x01), el nombre hace referencia al nombre del equipo de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="0d73d-111">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="0d73d-112">De lo contrario, el nombre hace referencia al nombre de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="0d73d-112">Otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="0d73d-113">*bstrCertTemplateName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d73d-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d73d-114">Nombre de la plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="0d73d-114">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="0d73d-115">*pbstrCAName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0d73d-115">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d73d-116">Puntero a una cadena que devuelve el nombre de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="0d73d-116">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d73d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d73d-117">Return value</span></span>

### <a name="c"></a><span data-ttu-id="0d73d-118">C++</span><span class="sxs-lookup"><span data-stu-id="0d73d-118">C++</span></span>

<span data-ttu-id="0d73d-119">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="0d73d-119">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="0d73d-120">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="0d73d-120">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="0d73d-121">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="0d73d-121">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="0d73d-122">VB</span><span class="sxs-lookup"><span data-stu-id="0d73d-122">VB</span></span>

<span data-ttu-id="0d73d-123">Cadena que representa el nombre de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="0d73d-123">A string that represents the name of the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d73d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d73d-124">Requirements</span></span>



| <span data-ttu-id="0d73d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d73d-125">Requirement</span></span> | <span data-ttu-id="0d73d-126">Value</span><span class="sxs-lookup"><span data-stu-id="0d73d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d73d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d73d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0d73d-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0d73d-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0d73d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d73d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0d73d-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d73d-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0d73d-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d73d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d73d-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d73d-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d73d-133">IID</span><span class="sxs-lookup"><span data-stu-id="0d73d-133">IID</span></span><br/>                      | <span data-ttu-id="0d73d-134">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="0d73d-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="0d73d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d73d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d73d-136">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="0d73d-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="0d73d-137">**ISCrdEnr::getCACount**</span><span class="sxs-lookup"><span data-stu-id="0d73d-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="0d73d-138">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="0d73d-138">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> <dt>

[<span data-ttu-id="0d73d-139">**ISCrdEnr::setCAName**</span><span class="sxs-lookup"><span data-stu-id="0d73d-139">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 
