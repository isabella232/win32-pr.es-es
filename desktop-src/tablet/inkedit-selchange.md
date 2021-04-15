---
description: Se produce cuando cambia la selección actual de texto en el control InkEdit o se mueve el punto de inserción.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Evento InkEdit. SelChange (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648471"
---
# <a name="inkeditselchange-event"></a><span data-ttu-id="c57ea-103">Evento InkEdit. SelChange</span><span class="sxs-lookup"><span data-stu-id="c57ea-103">InkEdit.SelChange event</span></span>

<span data-ttu-id="c57ea-104">Se produce cuando cambia la selección actual de texto en el control [InkEdit](inkedit-control-reference.md) o se mueve el punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="c57ea-104">Occurs when the current selection of text in the [InkEdit](inkedit-control-reference.md) control has changed or the insertion point has moved.</span></span>

## <a name="syntax"></a><span data-ttu-id="c57ea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c57ea-105">Syntax</span></span>


```C++
void SelChange();
```



## <a name="parameters"></a><span data-ttu-id="c57ea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c57ea-106">Parameters</span></span>

<span data-ttu-id="c57ea-107">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c57ea-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c57ea-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c57ea-108">Return value</span></span>

<span data-ttu-id="c57ea-109">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="c57ea-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c57ea-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c57ea-110">Remarks</span></span>

<span data-ttu-id="c57ea-111">Puede usar el evento **SelChange** para comprobar las distintas propiedades que proporcionan información sobre la selección actual (como [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) para que pueda actualizar los botones de una barra de herramientas, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c57ea-111">You can use the **SelChange** event to check the various properties that give information about the current selection (such as [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) so you can update buttons in a toolbar, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="c57ea-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c57ea-112">Requirements</span></span>



| <span data-ttu-id="c57ea-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c57ea-113">Requirement</span></span> | <span data-ttu-id="c57ea-114">Value</span><span class="sxs-lookup"><span data-stu-id="c57ea-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c57ea-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c57ea-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c57ea-116">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c57ea-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c57ea-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c57ea-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c57ea-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c57ea-118">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c57ea-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c57ea-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c57ea-120"><dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c57ea-120"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c57ea-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c57ea-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="c57ea-122"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c57ea-122"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c57ea-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c57ea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c57ea-124">InkEdit</span><span class="sxs-lookup"><span data-stu-id="c57ea-124">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




