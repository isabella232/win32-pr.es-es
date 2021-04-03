---
description: Recupera el identificador único del botón del lápiz óptico.
ms.assetid: 06bd6a84-46cd-4c62-92d6-50caae359e43
title: 'ITabletCursorButton:: GetGuid (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetGuid
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 21d63ef0c934e96bc93b5384cab1e67f9dd452d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083107"
---
# <a name="itabletcursorbuttongetguid-method"></a><span data-ttu-id="b9885-103">ITabletCursorButton:: GetGuid (método)</span><span class="sxs-lookup"><span data-stu-id="b9885-103">ITabletCursorButton::GetGuid method</span></span>

<span data-ttu-id="b9885-104">Recupera el identificador único del botón del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="b9885-104">Retrieves the unique identifier of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9885-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9885-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pguidBtn
);
```



## <a name="parameters"></a><span data-ttu-id="b9885-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9885-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9885-107">*pguidBtn* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b9885-107">*pguidBtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9885-108">Un valor único que identifica el botón del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="b9885-108">A unique value that identifies the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9885-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9885-109">Return value</span></span>

<span data-ttu-id="b9885-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b9885-110">This method can return one of these values.</span></span>



| <span data-ttu-id="b9885-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b9885-111">Return code</span></span>                                                                            | <span data-ttu-id="b9885-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9885-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="b9885-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b9885-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="b9885-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b9885-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="b9885-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="b9885-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="b9885-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="b9885-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b9885-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9885-117">Requirements</span></span>



| <span data-ttu-id="b9885-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9885-118">Requirement</span></span> | <span data-ttu-id="b9885-119">Value</span><span class="sxs-lookup"><span data-stu-id="b9885-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9885-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9885-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b9885-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b9885-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b9885-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9885-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b9885-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b9885-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b9885-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9885-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9885-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b9885-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9885-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9885-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9885-127">**Interfaz ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="b9885-127">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 




