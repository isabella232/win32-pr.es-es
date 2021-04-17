---
description: El método DoCreateWindow crea la ventana.
ms.assetid: bbe38a71-bbf7-4380-96a3-074b992a1d1e
title: CBaseWindow.DoCmétodo reateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoCreateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76bea1523f48a6e22a3c2d9370fa32bcea022621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660234"
---
# <a name="cbasewindowdocreatewindow-method"></a><span data-ttu-id="f0ef8-103">CBaseWindow.DoCmétodo reateWindow</span><span class="sxs-lookup"><span data-stu-id="f0ef8-103">CBaseWindow.DoCreateWindow method</span></span>

<span data-ttu-id="f0ef8-104">El `DoCreateWindow` método crea la ventana.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-104">The `DoCreateWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ef8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0ef8-105">Syntax</span></span>


```C++
HRESULT DoCreateWindow();
```



## <a name="parameters"></a><span data-ttu-id="f0ef8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0ef8-106">Parameters</span></span>

<span data-ttu-id="f0ef8-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0ef8-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0ef8-108">Return value</span></span>

<span data-ttu-id="f0ef8-109">Devuelve S \_ correcto si se realiza correctamente o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0ef8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0ef8-110">Remarks</span></span>

<span data-ttu-id="f0ef8-111">El método [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-111">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ef8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0ef8-112">Requirements</span></span>



| <span data-ttu-id="f0ef8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0ef8-113">Requirement</span></span> | <span data-ttu-id="f0ef8-114">Value</span><span class="sxs-lookup"><span data-stu-id="f0ef8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ef8-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0ef8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f0ef8-116"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ef8-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f0ef8-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0ef8-117">Library</span></span><br/> | <dl> <span data-ttu-id="f0ef8-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ef8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ef8-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0ef8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ef8-120">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="f0ef8-120">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




