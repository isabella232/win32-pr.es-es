---
description: Recupera el nombre del botón del lápiz óptico.
ms.assetid: 26fad9bc-43c2-4b00-b76b-bf9f1242da77
title: 'ITabletCursorButton:: GetName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b21fd92823fb0f60c0936f662982d176a938b4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687732"
---
# <a name="itabletcursorbuttongetname-method"></a><span data-ttu-id="2b44b-103">ITabletCursorButton:: GetName (método)</span><span class="sxs-lookup"><span data-stu-id="2b44b-103">ITabletCursorButton::GetName method</span></span>

<span data-ttu-id="2b44b-104">Recupera el nombre del botón del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="2b44b-104">Retrieves the name of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b44b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b44b-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="2b44b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b44b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b44b-107">*ppwszName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2b44b-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b44b-108">El nombre del botón del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="2b44b-108">The name of the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b44b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b44b-109">Return value</span></span>

<span data-ttu-id="2b44b-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2b44b-110">This method can return one of these values.</span></span>



| <span data-ttu-id="2b44b-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2b44b-111">Return code</span></span>                                                                            | <span data-ttu-id="2b44b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b44b-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="2b44b-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2b44b-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="2b44b-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="2b44b-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="2b44b-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="2b44b-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="2b44b-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="2b44b-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2b44b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b44b-117">Remarks</span></span>

<span data-ttu-id="2b44b-118">Es responsabilidad del llamador liberar la memoria devuelta desde este método mediante [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="2b44b-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b44b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b44b-119">Requirements</span></span>



| <span data-ttu-id="2b44b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b44b-120">Requirement</span></span> | <span data-ttu-id="2b44b-121">Value</span><span class="sxs-lookup"><span data-stu-id="2b44b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b44b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b44b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2b44b-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2b44b-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2b44b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b44b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2b44b-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2b44b-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2b44b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b44b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b44b-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b44b-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b44b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b44b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b44b-129">**Interfaz ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="2b44b-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

