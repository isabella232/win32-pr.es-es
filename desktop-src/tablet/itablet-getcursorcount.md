---
description: Devuelve el número de objetos cursor asociados a la tableta.
ms.assetid: 7aa5802c-1255-41a4-b1fa-23e5f56c0b80
title: 'ITablet:: GetCursorCount (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetCursorCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2309384e4aa36383277ba72cc407cabef7ab4b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720679"
---
# <a name="itabletgetcursorcount-method"></a><span data-ttu-id="7fa8c-103">ITablet:: GetCursorCount (método)</span><span class="sxs-lookup"><span data-stu-id="7fa8c-103">ITablet::GetCursorCount method</span></span>

<span data-ttu-id="7fa8c-104">Devuelve el número de objetos cursor asociados a la tableta.</span><span class="sxs-lookup"><span data-stu-id="7fa8c-104">Returns the number of cursor objects associated with the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa8c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fa8c-105">Syntax</span></span>


```C++
HRESULT GetCursorCount(
  [out] ULONG *pcCurs
);
```



## <a name="parameters"></a><span data-ttu-id="7fa8c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fa8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fa8c-107">*pcCurs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7fa8c-107">*pcCurs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fa8c-108">El número de objetos cursor asociados a la tableta.</span><span class="sxs-lookup"><span data-stu-id="7fa8c-108">The number of cursor objects associated with the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fa8c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fa8c-109">Return value</span></span>

<span data-ttu-id="7fa8c-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="7fa8c-110">This method can return one of these values.</span></span>



| <span data-ttu-id="7fa8c-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7fa8c-111">Return code</span></span>                                                                            | <span data-ttu-id="7fa8c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fa8c-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="7fa8c-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7fa8c-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="7fa8c-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="7fa8c-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="7fa8c-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="7fa8c-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="7fa8c-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="7fa8c-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7fa8c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fa8c-117">Requirements</span></span>



| <span data-ttu-id="7fa8c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fa8c-118">Requirement</span></span> | <span data-ttu-id="7fa8c-119">Value</span><span class="sxs-lookup"><span data-stu-id="7fa8c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa8c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fa8c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7fa8c-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7fa8c-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7fa8c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fa8c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7fa8c-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7fa8c-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7fa8c-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7fa8c-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="7fa8c-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7fa8c-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fa8c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fa8c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa8c-127">**Interfaz ITablet**</span><span class="sxs-lookup"><span data-stu-id="7fa8c-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




