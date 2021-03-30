---
description: Recupera los valores de contexto predeterminados para la tableta.
ms.assetid: 59d1bab0-a8b8-4e23-9311-2921f9035dc4
title: 'ITablet:: GetDefaultContextSettings (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetDefaultContextSettings
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7e2f0977257553d8405b337dcc1f22d8b0fdff5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814822"
---
# <a name="itabletgetdefaultcontextsettings-method"></a><span data-ttu-id="b830a-103">ITablet:: GetDefaultContextSettings (método)</span><span class="sxs-lookup"><span data-stu-id="b830a-103">ITablet::GetDefaultContextSettings method</span></span>

<span data-ttu-id="b830a-104">Recupera los valores de contexto predeterminados para la tableta.</span><span class="sxs-lookup"><span data-stu-id="b830a-104">Retrieves the default context settings for the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="b830a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b830a-105">Syntax</span></span>


```C++
HRESULT GetDefaultContextSettings(
  [out] TABLET_CONTEXT_SETTINGS **ppTCS
);
```



## <a name="parameters"></a><span data-ttu-id="b830a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b830a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b830a-107">*ppTCS* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b830a-107">*ppTCS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b830a-108">Los valores de contexto predeterminados para la tableta.</span><span class="sxs-lookup"><span data-stu-id="b830a-108">The default context settings for the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b830a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b830a-109">Return value</span></span>

<span data-ttu-id="b830a-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b830a-110">This method can return one of these values.</span></span>



| <span data-ttu-id="b830a-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b830a-111">Return code</span></span>                                                                            | <span data-ttu-id="b830a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b830a-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="b830a-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b830a-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="b830a-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b830a-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="b830a-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="b830a-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="b830a-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="b830a-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b830a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b830a-117">Remarks</span></span>

<span data-ttu-id="b830a-118">Es responsabilidad del llamador liberar la memoria devuelta desde este método mediante [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="b830a-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="b830a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b830a-119">Requirements</span></span>



| <span data-ttu-id="b830a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b830a-120">Requirement</span></span> | <span data-ttu-id="b830a-121">Value</span><span class="sxs-lookup"><span data-stu-id="b830a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b830a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b830a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b830a-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b830a-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b830a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b830a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b830a-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b830a-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b830a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b830a-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="b830a-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b830a-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b830a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b830a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b830a-129">**Interfaz ITablet**</span><span class="sxs-lookup"><span data-stu-id="b830a-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

