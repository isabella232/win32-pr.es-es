---
description: El método GetRequestId devuelve un valor de identificador único global (GUID) para una solicitud. Un GUID es un número único de 128 bits.
ms.assetid: c8df15cf-ab48-491f-ac18-1dad567bbc0b
ms.tgt_platform: multiple
title: 'IWbemCausalityAccess:: GetRequestId (método) (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.GetRequestId
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 075be627b26d99a8b4f03c5a4a962b41f153c8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687984"
---
# <a name="iwbemcausalityaccessgetrequestid-method"></a><span data-ttu-id="9ced1-104">IWbemCausalityAccess:: GetRequestId (método)</span><span class="sxs-lookup"><span data-stu-id="9ced1-104">IWbemCausalityAccess::GetRequestId method</span></span>

<span data-ttu-id="9ced1-105">El método **GetRequestId** devuelve un valor de identificador único global (GUID) para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ced1-105">The **GetRequestId** method returns a Globally Unique Identifier (GUID) value for a request.</span></span> <span data-ttu-id="9ced1-106">Un GUID es un número único de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="9ced1-106">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ced1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ced1-107">Syntax</span></span>


```C++
HRESULT GetRequestId(
  [out] REQUESTID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="9ced1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ced1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ced1-109">*pId* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9ced1-109">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ced1-110">Valor GUID que identifica de forma única una solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ced1-110">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="9ced1-111">Por ejemplo, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="9ced1-111">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ced1-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ced1-112">Return value</span></span>

<span data-ttu-id="9ced1-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9ced1-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ced1-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ced1-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ced1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ced1-115">Requirements</span></span>



| <span data-ttu-id="9ced1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ced1-116">Requirement</span></span> | <span data-ttu-id="9ced1-117">Value</span><span class="sxs-lookup"><span data-stu-id="9ced1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ced1-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ced1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ced1-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ced1-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ced1-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ced1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ced1-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ced1-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ced1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ced1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ced1-123"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ced1-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="9ced1-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ced1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ced1-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ced1-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ced1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ced1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ced1-127">**IWbemCausalityAccess**</span><span class="sxs-lookup"><span data-stu-id="9ced1-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




