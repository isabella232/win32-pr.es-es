---
description: El método DoShowWindow establece el estado de presentación de la ventana.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: Método CBaseWindow. DoShowWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2a1f7d4cd9bc4600733d5d33f9df6d3b6998f57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679574"
---
# <a name="cbasewindowdoshowwindow-method"></a><span data-ttu-id="b18fd-103">CBaseWindow. DoShowWindow, método</span><span class="sxs-lookup"><span data-stu-id="b18fd-103">CBaseWindow.DoShowWindow method</span></span>

<span data-ttu-id="b18fd-104">El método **DoShowWindow** establece el estado de presentación de la ventana.</span><span class="sxs-lookup"><span data-stu-id="b18fd-104">The **DoShowWindow** method sets the window's show state.</span></span>

## <a name="syntax"></a><span data-ttu-id="b18fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b18fd-105">Syntax</span></span>


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a><span data-ttu-id="b18fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b18fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b18fd-107">*ShowCmd*</span><span class="sxs-lookup"><span data-stu-id="b18fd-107">*ShowCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="b18fd-108">Marca que especifica cómo se mostrará la ventana.</span><span class="sxs-lookup"><span data-stu-id="b18fd-108">Flag that specifies how the window is to be shown.</span></span> <span data-ttu-id="b18fd-109">El valor puede ser cualquier constante definida para el parámetro *nCmdShow* de la función [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="b18fd-109">The value can be any constant defined for the *nCmdShow* parameter of the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b18fd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b18fd-110">Return value</span></span>

<span data-ttu-id="b18fd-111">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b18fd-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b18fd-112">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b18fd-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b18fd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b18fd-113">Requirements</span></span>



| <span data-ttu-id="b18fd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b18fd-114">Requirement</span></span> | <span data-ttu-id="b18fd-115">Value</span><span class="sxs-lookup"><span data-stu-id="b18fd-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b18fd-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b18fd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b18fd-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b18fd-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b18fd-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b18fd-118">Library</span></span><br/> | <dl> <span data-ttu-id="b18fd-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b18fd-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b18fd-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b18fd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b18fd-121">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="b18fd-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

