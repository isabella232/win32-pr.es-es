---
description: Se produce cuando el cursor se mueve sobre el digitalizador de Tablet PC.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: 'ITabletEventSink:: CursorMove (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688500"
---
# <a name="itableteventsinkcursormove-method"></a><span data-ttu-id="0742b-103">ITabletEventSink:: CursorMove (método)</span><span class="sxs-lookup"><span data-stu-id="0742b-103">ITabletEventSink::CursorMove method</span></span>

<span data-ttu-id="0742b-104">Se produce cuando el cursor se mueve sobre el digitalizador de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0742b-104">Occurs when the cursor moves over the tablet digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0742b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0742b-105">Syntax</span></span>


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a><span data-ttu-id="0742b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0742b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0742b-107">*tcid*</span><span class="sxs-lookup"><span data-stu-id="0742b-107">*tcid*</span></span> 
</dt> <dd>

<span data-ttu-id="0742b-108">Dentifier único del digitalizador de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0742b-108">Unique dentifier of the tablet digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="0742b-109">*Cid*</span><span class="sxs-lookup"><span data-stu-id="0742b-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="0742b-110">Identificador único del lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0742b-110">Unique identifier of the tablet stylus.</span></span>

</dd> <dt>

<span data-ttu-id="0742b-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="0742b-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0742b-112">Ventana en la que se ha desplace el cursor.</span><span class="sxs-lookup"><span data-stu-id="0742b-112">The window over which the cursor moved.</span></span>

</dd> <dt>

<span data-ttu-id="0742b-113">*xPos*</span><span class="sxs-lookup"><span data-stu-id="0742b-113">*xPos*</span></span> 
</dt> <dd>

<span data-ttu-id="0742b-114">Posición X del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="0742b-114">The X position of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="0742b-115">*yPos*</span><span class="sxs-lookup"><span data-stu-id="0742b-115">*yPos*</span></span> 
</dt> <dd>

<span data-ttu-id="0742b-116">Posición Y del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="0742b-116">The Y position of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0742b-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0742b-117">Return value</span></span>

<span data-ttu-id="0742b-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0742b-118">This method can return one of these values.</span></span>



| <span data-ttu-id="0742b-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0742b-119">Return code</span></span>                                                                            | <span data-ttu-id="0742b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="0742b-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0742b-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0742b-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0742b-122">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0742b-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="0742b-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="0742b-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0742b-124">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="0742b-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0742b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0742b-125">Requirements</span></span>



| <span data-ttu-id="0742b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0742b-126">Requirement</span></span> | <span data-ttu-id="0742b-127">Value</span><span class="sxs-lookup"><span data-stu-id="0742b-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0742b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0742b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0742b-129">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0742b-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0742b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0742b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0742b-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0742b-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0742b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0742b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="0742b-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0742b-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0742b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="0742b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0742b-135">**Interfaz ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="0742b-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




