---
description: Recupera el nombre del lápiz de Tablet PC.
ms.assetid: 94955c04-f699-428b-b4bf-53919b61b1ab
title: 'ITabletCursor:: GetName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b9d984d5eb711c2344ba0f9fb2dbf410a7d49bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002880"
---
# <a name="itabletcursorgetname-method"></a><span data-ttu-id="3b7ea-103">ITabletCursor:: GetName (método)</span><span class="sxs-lookup"><span data-stu-id="3b7ea-103">ITabletCursor::GetName method</span></span>

<span data-ttu-id="3b7ea-104">Recupera el nombre del lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="3b7ea-104">Retrieves the name of the tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b7ea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b7ea-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="3b7ea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b7ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b7ea-107">*ppwszName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3b7ea-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7ea-108">Nombre del lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="3b7ea-108">The name of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b7ea-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b7ea-109">Return value</span></span>

<span data-ttu-id="3b7ea-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3b7ea-110">This method can return one of these values.</span></span>



| <span data-ttu-id="3b7ea-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3b7ea-111">Return code</span></span>                                                                            | <span data-ttu-id="3b7ea-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b7ea-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3b7ea-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3b7ea-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3b7ea-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="3b7ea-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3b7ea-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="3b7ea-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3b7ea-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="3b7ea-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b7ea-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b7ea-117">Remarks</span></span>

<span data-ttu-id="3b7ea-118">Es responsabilidad del llamador liberar la memoria devuelta desde este método mediante [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="3b7ea-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b7ea-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b7ea-119">Requirements</span></span>



| <span data-ttu-id="3b7ea-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b7ea-120">Requirement</span></span> | <span data-ttu-id="3b7ea-121">Value</span><span class="sxs-lookup"><span data-stu-id="3b7ea-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b7ea-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b7ea-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3b7ea-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3b7ea-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3b7ea-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b7ea-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3b7ea-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3b7ea-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3b7ea-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b7ea-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b7ea-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b7ea-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b7ea-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b7ea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b7ea-129">**ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="3b7ea-129">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="3b7ea-130">**Interfaz ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="3b7ea-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

