---
description: Indica si el lápiz está en la parte inferior.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: 'ITabletCursor:: IsInverted (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659919"
---
# <a name="itabletcursorisinverted-method"></a><span data-ttu-id="ea04a-103">ITabletCursor:: IsInverted (método)</span><span class="sxs-lookup"><span data-stu-id="ea04a-103">ITabletCursor::IsInverted method</span></span>

<span data-ttu-id="ea04a-104">Indica si el lápiz está en la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="ea04a-104">Indicates if the stylus is upside down.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea04a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea04a-105">Syntax</span></span>


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a><span data-ttu-id="ea04a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea04a-106">Parameters</span></span>

<span data-ttu-id="ea04a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ea04a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea04a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea04a-108">Return value</span></span>

<span data-ttu-id="ea04a-109">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ea04a-109">This method can return one of these values.</span></span>



| <span data-ttu-id="ea04a-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ea04a-110">Return code</span></span>                                                                             | <span data-ttu-id="ea04a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea04a-111">Description</span></span>                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="ea04a-112"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ea04a-112"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ea04a-113">Se invierte el lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="ea04a-113">The stylus is inverted.</span></span><br/>        |
| <dl> <span data-ttu-id="ea04a-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ea04a-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ea04a-115">No se invierte el lápiz.</span><span class="sxs-lookup"><span data-stu-id="ea04a-115">The stylus is not inverted.</span></span><br/>    |
| <dl> <span data-ttu-id="ea04a-116"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="ea04a-116"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="ea04a-117">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="ea04a-117">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ea04a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea04a-118">Requirements</span></span>



| <span data-ttu-id="ea04a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea04a-119">Requirement</span></span> | <span data-ttu-id="ea04a-120">Value</span><span class="sxs-lookup"><span data-stu-id="ea04a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea04a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea04a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea04a-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ea04a-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ea04a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea04a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea04a-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ea04a-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ea04a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea04a-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea04a-126"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ea04a-126"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea04a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea04a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea04a-128">**ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="ea04a-128">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="ea04a-129">**Interfaz ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="ea04a-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 




