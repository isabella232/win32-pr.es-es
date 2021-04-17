---
description: El \_ método get Caption recupera el título de la ventana actual.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: Método CBaseControlWindow.get_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8d743c746f833007d91afd4346f7f48c6218dde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660407"
---
# <a name="cbasecontrolwindowget_caption-method"></a><span data-ttu-id="37621-103">CBaseControlWindow. Get \_ Caption (método)</span><span class="sxs-lookup"><span data-stu-id="37621-103">CBaseControlWindow.get\_Caption method</span></span>

<span data-ttu-id="37621-104">El `get_Caption` método recupera el título de la ventana actual.</span><span class="sxs-lookup"><span data-stu-id="37621-104">The `get_Caption` method retrieves the current window caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="37621-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37621-105">Syntax</span></span>


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a><span data-ttu-id="37621-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37621-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37621-107">*pstrCaption*</span><span class="sxs-lookup"><span data-stu-id="37621-107">*pstrCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="37621-108">Puntero al título de la ventana actual.</span><span class="sxs-lookup"><span data-stu-id="37621-108">Pointer to the current window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37621-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37621-109">Return value</span></span>

<span data-ttu-id="37621-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="37621-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37621-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37621-111">Remarks</span></span>

<span data-ttu-id="37621-112">La mayoría de las ventanas de nivel superior de un escritorio basado en Windows tienen un título (título) asociado.</span><span class="sxs-lookup"><span data-stu-id="37621-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="37621-113">Esta propiedad se puede consultar y establecer a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="37621-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="37621-114">Cualquier conjunto de títulos solo será visible si la ventana tiene aplicado el \_ estilo de leyenda de WS.</span><span class="sxs-lookup"><span data-stu-id="37621-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="37621-115">Si no es así, el título se puede establecer (y recuperar), aunque no será visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="37621-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="37621-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37621-116">Requirements</span></span>



| <span data-ttu-id="37621-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="37621-117">Requirement</span></span> | <span data-ttu-id="37621-118">Value</span><span class="sxs-lookup"><span data-stu-id="37621-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37621-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37621-119">Header</span></span><br/>  | <dl> <span data-ttu-id="37621-120"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37621-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="37621-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37621-121">Library</span></span><br/> | <dl> <span data-ttu-id="37621-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="37621-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37621-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="37621-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37621-124">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="37621-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




