---
description: Recupera un rectángulo que representa el área de entrada máxima de la tableta.
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: 'ITablet:: GetMaxInputRect (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: de2649fe7410e6d335f653c09bfe86a8ddaac813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911717"
---
# <a name="itabletgetmaxinputrect-method"></a><span data-ttu-id="8de87-103">ITablet:: GetMaxInputRect (método)</span><span class="sxs-lookup"><span data-stu-id="8de87-103">ITablet::GetMaxInputRect method</span></span>

<span data-ttu-id="8de87-104">Recupera un rectángulo que representa el área de entrada máxima de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8de87-104">Retrieves a rectangle that represents maximum input area of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="8de87-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8de87-105">Syntax</span></span>


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="8de87-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8de87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8de87-107">*prcInput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8de87-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8de87-108">Puntero al rectángulo que representa el área de entrada máxima de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8de87-108">Pointer to rectangle that represents maximum input area of the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8de87-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8de87-109">Return value</span></span>

<span data-ttu-id="8de87-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8de87-110">This method can return one of these values.</span></span>



| <span data-ttu-id="8de87-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8de87-111">Return code</span></span>                                                                            | <span data-ttu-id="8de87-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8de87-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="8de87-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8de87-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="8de87-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="8de87-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="8de87-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="8de87-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="8de87-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8de87-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8de87-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8de87-117">Requirements</span></span>



| <span data-ttu-id="8de87-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8de87-118">Requirement</span></span> | <span data-ttu-id="8de87-119">Value</span><span class="sxs-lookup"><span data-stu-id="8de87-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8de87-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8de87-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8de87-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8de87-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8de87-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8de87-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8de87-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8de87-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8de87-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8de87-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="8de87-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8de87-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8de87-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8de87-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de87-127">**Interfaz ITablet**</span><span class="sxs-lookup"><span data-stu-id="8de87-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




