---
description: El método DoSetWindowForeground coloca la ventana en primer plano.
ms.assetid: 5aace88b-14c0-41ce-95a3-0e255ca56ae6
title: Método CBaseWindow. DoSetWindowForeground (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoSetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16a4c8bf41c042c99624289fa26fe252dee62747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660227"
---
# <a name="cbasewindowdosetwindowforeground-method"></a><span data-ttu-id="ec16a-103">CBaseWindow. DoSetWindowForeground, método</span><span class="sxs-lookup"><span data-stu-id="ec16a-103">CBaseWindow.DoSetWindowForeground method</span></span>

<span data-ttu-id="ec16a-104">El `DoSetWindowForeground` método pone la ventana en primer plano.</span><span class="sxs-lookup"><span data-stu-id="ec16a-104">The `DoSetWindowForeground` method brings the window to the foreground.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec16a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec16a-105">Syntax</span></span>


```C++
void DoSetWindowForeground(
   BOOL bFocus
);
```



## <a name="parameters"></a><span data-ttu-id="ec16a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec16a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec16a-107">*bFocus*</span><span class="sxs-lookup"><span data-stu-id="ec16a-107">*bFocus*</span></span> 
</dt> <dd>

<span data-ttu-id="ec16a-108">Valor booleano que especifica si se debe dar el foco a la ventana.</span><span class="sxs-lookup"><span data-stu-id="ec16a-108">Boolean value that specifies whether to give the window focus.</span></span> <span data-ttu-id="ec16a-109">Si el valor es **true**, la ventana obtiene el foco.</span><span class="sxs-lookup"><span data-stu-id="ec16a-109">If the value is **TRUE**, the window gains focus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec16a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec16a-110">Return value</span></span>

<span data-ttu-id="ec16a-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ec16a-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec16a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec16a-112">Requirements</span></span>



| <span data-ttu-id="ec16a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec16a-113">Requirement</span></span> | <span data-ttu-id="ec16a-114">Value</span><span class="sxs-lookup"><span data-stu-id="ec16a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec16a-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec16a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ec16a-116"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec16a-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec16a-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec16a-117">Library</span></span><br/> | <dl> <span data-ttu-id="ec16a-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ec16a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec16a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec16a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec16a-120">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="ec16a-120">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




