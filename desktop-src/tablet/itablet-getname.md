---
description: Devuelve una cadena que contiene el nombre del dispositivo de tableta gráfica.
ms.assetid: 025620b5-ab68-4e36-ae26-2226a2fdeb61
title: 'ITablet:: GetName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c2d6bd20a011b1bf5cfbe7582445de45728bbd7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277216"
---
# <a name="itabletgetname-method"></a><span data-ttu-id="839a5-103">ITablet:: GetName (método)</span><span class="sxs-lookup"><span data-stu-id="839a5-103">ITablet::GetName method</span></span>

<span data-ttu-id="839a5-104">Devuelve una cadena que contiene el nombre del dispositivo de tableta gráfica.</span><span class="sxs-lookup"><span data-stu-id="839a5-104">Returns a string containing the name of the tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="839a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="839a5-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="839a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="839a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="839a5-107">*ppwszName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="839a5-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="839a5-108">Puntero a una cadena que contiene el nombre del dispositivo de tableta gráfica.</span><span class="sxs-lookup"><span data-stu-id="839a5-108">Pointer to a string containing the name of the tablet device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="839a5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="839a5-109">Return value</span></span>

<span data-ttu-id="839a5-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="839a5-110">This method can return one of these values.</span></span>



| <span data-ttu-id="839a5-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="839a5-111">Return code</span></span>                                                                            | <span data-ttu-id="839a5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="839a5-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="839a5-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="839a5-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="839a5-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="839a5-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="839a5-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="839a5-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="839a5-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="839a5-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="839a5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="839a5-117">Remarks</span></span>

<span data-ttu-id="839a5-118">Es responsabilidad del llamador liberar la memoria devuelta desde este método mediante [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="839a5-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="839a5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="839a5-119">Requirements</span></span>



| <span data-ttu-id="839a5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="839a5-120">Requirement</span></span> | <span data-ttu-id="839a5-121">Value</span><span class="sxs-lookup"><span data-stu-id="839a5-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="839a5-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="839a5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="839a5-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="839a5-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="839a5-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="839a5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="839a5-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="839a5-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="839a5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="839a5-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="839a5-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="839a5-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="839a5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="839a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="839a5-129">**Interfaz ITablet**</span><span class="sxs-lookup"><span data-stu-id="839a5-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

