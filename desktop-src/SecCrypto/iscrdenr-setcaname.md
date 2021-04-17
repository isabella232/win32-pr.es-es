---
description: Especifica el nombre de la entidad de certificación (CA).
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: 'ISCrdEnr:: setCAName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668330"
---
# <a name="iscrdenrsetcaname-method"></a><span data-ttu-id="b01f6-103">ISCrdEnr:: setCAName (método)</span><span class="sxs-lookup"><span data-stu-id="b01f6-103">ISCrdEnr::setCAName method</span></span>

<span data-ttu-id="b01f6-104">El método **setCAName** especifica el nombre de la [*entidad de certificación*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="b01f6-104">The **setCAName** method specifies the name of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="b01f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b01f6-105">Syntax</span></span>


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="b01f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b01f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b01f6-107">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b01f6-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b01f6-108">Valor que especifica si el nombre hace referencia al nombre de la entidad de certificación o al nombre del equipo de la CA.</span><span class="sxs-lookup"><span data-stu-id="b01f6-108">Value that specifies whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="b01f6-109">Si este valor es PPAC \_ ENROLL \_ CA nombre del \_ equipo \_ (definido como 0x01), el nombre hace referencia al nombre del equipo de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="b01f6-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="b01f6-110">De lo contrario, el nombre hace referencia al nombre de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="b01f6-110">Otherwise, the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="b01f6-111">*bstrCertTemplateName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b01f6-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b01f6-112">Nombre de la plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="b01f6-112">Name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="b01f6-113">*bstrCAName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b01f6-113">*bstrCAName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b01f6-114">Nombre de la entidad de certificación que se usará con la plantilla de certificado especificada por *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="b01f6-114">CA name to be used with the certificate template specified by *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b01f6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b01f6-115">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="b01f6-116">VB</span><span class="sxs-lookup"><span data-stu-id="b01f6-116">VB</span></span>

<span data-ttu-id="b01f6-117">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b01f6-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="b01f6-118">Un valor de S \_ OK indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b01f6-118">A value of S\_OK indicates that the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b01f6-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b01f6-119">Remarks</span></span>

<span data-ttu-id="b01f6-120">Utilice este método para especificar una CA para una plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="b01f6-120">Use this method to specify a CA for a certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="b01f6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b01f6-121">Requirements</span></span>



| <span data-ttu-id="b01f6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b01f6-122">Requirement</span></span> | <span data-ttu-id="b01f6-123">Value</span><span class="sxs-lookup"><span data-stu-id="b01f6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b01f6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b01f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b01f6-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b01f6-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b01f6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b01f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b01f6-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b01f6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b01f6-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b01f6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b01f6-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b01f6-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="b01f6-130">IID</span><span class="sxs-lookup"><span data-stu-id="b01f6-130">IID</span></span><br/>                      | <span data-ttu-id="b01f6-131">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="b01f6-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b01f6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b01f6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b01f6-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="b01f6-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="b01f6-134">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="b01f6-134">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="b01f6-135">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="b01f6-135">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 
