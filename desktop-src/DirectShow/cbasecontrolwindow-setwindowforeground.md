---
description: El método SetWindowForeground mueve la ventana de vídeo al primer plano y, opcionalmente, le da el foco.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Método CBaseControlWindow. SetWindowForeground (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661336"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a><span data-ttu-id="e6ae7-103">CBaseControlWindow. SetWindowForeground, método</span><span class="sxs-lookup"><span data-stu-id="e6ae7-103">CBaseControlWindow.SetWindowForeground method</span></span>

<span data-ttu-id="e6ae7-104">El `SetWindowForeground` método mueve la ventana de vídeo al primer plano y, opcionalmente, le da el foco.</span><span class="sxs-lookup"><span data-stu-id="e6ae7-104">The `SetWindowForeground` method moves the video window to the foreground and optionally gives it focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6ae7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6ae7-105">Syntax</span></span>


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a><span data-ttu-id="e6ae7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6ae7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6ae7-107">*Foco*</span><span class="sxs-lookup"><span data-stu-id="e6ae7-107">*Focus*</span></span> 
</dt> <dd>

<span data-ttu-id="e6ae7-108">Valor que especifica si la ventana de vídeo obtendrá el foco.</span><span class="sxs-lookup"><span data-stu-id="e6ae7-108">Value that specifies whether the video window will get focus.</span></span> <span data-ttu-id="e6ae7-109">Un valor de 1 proporciona el foco de la ventana y 0 no.</span><span class="sxs-lookup"><span data-stu-id="e6ae7-109">A value of  1 gives the window focus and 0 does not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6ae7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6ae7-110">Return value</span></span>

<span data-ttu-id="e6ae7-111">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e6ae7-111">Returns one of the following values.</span></span>



| <span data-ttu-id="e6ae7-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e6ae7-112">Return code</span></span>                                                                                           | <span data-ttu-id="e6ae7-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6ae7-113">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6ae7-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="e6ae7-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="e6ae7-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="e6ae7-115">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="e6ae7-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e6ae7-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="e6ae7-117">El foco no es igual a 1 o 0.</span><span class="sxs-lookup"><span data-stu-id="e6ae7-117">Focus doesn't equal  1 or 0.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e6ae7-118"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="e6ae7-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e6ae7-119">El filtro actual no está conectado a un gráfico de filtro completo.</span><span class="sxs-lookup"><span data-stu-id="e6ae7-119">The current filter isn't connected to a complete filter graph.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e6ae7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6ae7-120">Requirements</span></span>



| <span data-ttu-id="e6ae7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6ae7-121">Requirement</span></span> | <span data-ttu-id="e6ae7-122">Value</span><span class="sxs-lookup"><span data-stu-id="e6ae7-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ae7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6ae7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e6ae7-124"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6ae7-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6ae7-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6ae7-125">Library</span></span><br/> | <dl> <span data-ttu-id="e6ae7-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e6ae7-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6ae7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6ae7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ae7-128">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="e6ae7-128">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




