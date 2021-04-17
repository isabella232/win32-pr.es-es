---
description: Marca que especifica si la ventana envía o envía su mensaje de destrucción.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'Miembro CBaseWindow:: m_bDoPostToDestroy (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660972"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a><span data-ttu-id="210da-103">Miembro bDoPostToDestroy CBaseWindow:: m \_</span><span class="sxs-lookup"><span data-stu-id="210da-103">CBaseWindow::m\_bDoPostToDestroy member</span></span>

<span data-ttu-id="210da-104">Marca que especifica si la ventana envía o envía su mensaje de destrucción.</span><span class="sxs-lookup"><span data-stu-id="210da-104">Flag that specifies whether the window posts or sends its destruction message.</span></span> <span data-ttu-id="210da-105">Si **es true**, el método [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) usa la función **PostMessage** para enviarse a sí mismo un mensaje de destrucción privado.</span><span class="sxs-lookup"><span data-stu-id="210da-105">If **TRUE**, the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method uses the **PostMessage** function to send itself a private destruction message.</span></span> <span data-ttu-id="210da-106">Si **es false**, **DoneWithWindow** usa la función **SendMessage** para enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="210da-106">If **FALSE**, **DoneWithWindow** uses the **SendMessage** function to send the message.</span></span> <span data-ttu-id="210da-107">De forma predeterminada, el valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="210da-107">By default, the value is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="210da-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="210da-108">Syntax</span></span>


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a><span data-ttu-id="210da-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="210da-109">Requirements</span></span>



| <span data-ttu-id="210da-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="210da-110">Requirement</span></span> | <span data-ttu-id="210da-111">Value</span><span class="sxs-lookup"><span data-stu-id="210da-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="210da-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="210da-112">Header</span></span><br/>  | <dl> <span data-ttu-id="210da-113"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="210da-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="210da-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="210da-114">Library</span></span><br/> | <dl> <span data-ttu-id="210da-115"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="210da-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="210da-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="210da-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="210da-117">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="210da-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




