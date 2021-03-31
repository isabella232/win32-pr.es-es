---
description: Recupera el nombre de la entidad de certificación (CA) especificada para una plantilla de certificado determinada.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: 'ISCrdEnr:: getCAName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278803"
---
# <a name="iscrdenrgetcaname-method"></a><span data-ttu-id="b7124-103">ISCrdEnr:: getCAName (método)</span><span class="sxs-lookup"><span data-stu-id="b7124-103">ISCrdEnr::getCAName method</span></span>

<span data-ttu-id="b7124-104">El método **getCAName** recupera el nombre de la entidad de [*certificación*](../secgloss/c-gly.md) (CA) especificada para una plantilla de certificado determinada.</span><span class="sxs-lookup"><span data-stu-id="b7124-104">The **getCAName** method retrieves the name of the specified [*certification authority*](../secgloss/c-gly.md) (CA) for a given certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7124-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7124-105">Syntax</span></span>


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="b7124-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7124-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7124-107">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7124-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7124-108">Un valor que determina si el nombre hace referencia al nombre de la entidad de certificación o al nombre del equipo de la CA.</span><span class="sxs-lookup"><span data-stu-id="b7124-108">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="b7124-109">Si este valor es PPAC \_ ENROLL \_ CA nombre del \_ equipo \_ (definido como 0x01), el nombre hace referencia al nombre del equipo de la CA; de lo contrario, el nombre hace referencia al nombre de la CA.</span><span class="sxs-lookup"><span data-stu-id="b7124-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01) then the name refers to the CA's machine name; otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="b7124-110">*bstrCertTemplateName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7124-110">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7124-111">Nombre de la plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="b7124-111">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="b7124-112">*pbstrCAName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b7124-112">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7124-113">Puntero a una cadena que devuelve el nombre de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="b7124-113">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7124-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7124-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="b7124-115">C++</span><span class="sxs-lookup"><span data-stu-id="b7124-115">C++</span></span>

<span data-ttu-id="b7124-116">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="b7124-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="b7124-117">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="b7124-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="b7124-118">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="b7124-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="b7124-119">VB</span><span class="sxs-lookup"><span data-stu-id="b7124-119">VB</span></span>

<span data-ttu-id="b7124-120">Cadena que representa el nombre de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="b7124-120">A string that represents the name of the CA.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7124-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7124-121">Remarks</span></span>

<span data-ttu-id="b7124-122">El nombre predeterminado de la entidad de certificación es el nombre de la lista de entidades de certificación disponibles.</span><span class="sxs-lookup"><span data-stu-id="b7124-122">The default CA name is the first name in the available list of CAs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7124-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7124-123">Requirements</span></span>



| <span data-ttu-id="b7124-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7124-124">Requirement</span></span> | <span data-ttu-id="b7124-125">Value</span><span class="sxs-lookup"><span data-stu-id="b7124-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7124-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7124-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b7124-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b7124-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b7124-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7124-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b7124-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7124-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b7124-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7124-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7124-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7124-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="b7124-132">IID</span><span class="sxs-lookup"><span data-stu-id="b7124-132">IID</span></span><br/>                      | <span data-ttu-id="b7124-133">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="b7124-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b7124-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7124-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7124-135">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="b7124-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="b7124-136">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="b7124-136">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="b7124-137">**ISCrdEnr::getCACount**</span><span class="sxs-lookup"><span data-stu-id="b7124-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="b7124-138">**ISCrdEnr::setCAName**</span><span class="sxs-lookup"><span data-stu-id="b7124-138">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 
