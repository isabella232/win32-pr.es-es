---
description: Recupera el número de botones del lápiz de Tablet PC.
ms.assetid: ae4ce670-769a-4f00-b728-285020f09934
title: 'ITabletCursor:: GetButtonCount (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButtonCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 08fdf24b2a0b69b7830a683786f18fc5df0805b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720718"
---
# <a name="itabletcursorgetbuttoncount-method"></a><span data-ttu-id="4f6d8-103">ITabletCursor:: GetButtonCount (método)</span><span class="sxs-lookup"><span data-stu-id="4f6d8-103">ITabletCursor::GetButtonCount method</span></span>

<span data-ttu-id="4f6d8-104">Recupera el número de botones del lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4f6d8-104">Retrieves the number of buttons on the tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f6d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f6d8-105">Syntax</span></span>


```C++
HRESULT GetButtonCount(
  [out] ULONG *pcButtons
);
```



## <a name="parameters"></a><span data-ttu-id="4f6d8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f6d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f6d8-107">*pcButtons* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4f6d8-107">*pcButtons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f6d8-108">Recuento de botones del lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4f6d8-108">The count of buttons on the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f6d8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f6d8-109">Return value</span></span>

<span data-ttu-id="4f6d8-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="4f6d8-110">This method can return one of these values.</span></span>



| <span data-ttu-id="4f6d8-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4f6d8-111">Return code</span></span>                                                                            | <span data-ttu-id="4f6d8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f6d8-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="4f6d8-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4f6d8-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="4f6d8-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="4f6d8-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="4f6d8-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="4f6d8-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="4f6d8-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="4f6d8-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4f6d8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f6d8-117">Requirements</span></span>



| <span data-ttu-id="4f6d8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f6d8-118">Requirement</span></span> | <span data-ttu-id="4f6d8-119">Value</span><span class="sxs-lookup"><span data-stu-id="4f6d8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6d8-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f6d8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4f6d8-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4f6d8-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4f6d8-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f6d8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4f6d8-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4f6d8-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4f6d8-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f6d8-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f6d8-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f6d8-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f6d8-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f6d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f6d8-127">**Interfaz ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="4f6d8-127">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




