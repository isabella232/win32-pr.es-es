---
description: El \_ método put estiloVentana establece los estilos de ventana estándar.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: Método CBaseControlWindow.put_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661340"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a><span data-ttu-id="39992-103">CBaseControlWindow. put \_ estiloVentana (método)</span><span class="sxs-lookup"><span data-stu-id="39992-103">CBaseControlWindow.put\_WindowStyle method</span></span>

<span data-ttu-id="39992-104">El `put_WindowStyle` método establece los estilos de ventana estándar.</span><span class="sxs-lookup"><span data-stu-id="39992-104">The `put_WindowStyle` method sets the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="39992-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39992-105">Syntax</span></span>


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="39992-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39992-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39992-107">*WindowStyle*</span><span class="sxs-lookup"><span data-stu-id="39992-107">*WindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="39992-108">Nuevos estilos de ventana.</span><span class="sxs-lookup"><span data-stu-id="39992-108">New window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39992-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39992-109">Return value</span></span>

<span data-ttu-id="39992-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="39992-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="39992-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39992-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="39992-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39992-112">Remarks</span></span>

<span data-ttu-id="39992-113">Tenga cuidado al cambiar los estilos de ventana.</span><span class="sxs-lookup"><span data-stu-id="39992-113">Take care when changing the window styles.</span></span> <span data-ttu-id="39992-114">En la mayoría de los casos, una aplicación debe recuperar el estilo actual y, a continuación, agregar o quitar los bits inapropiados.</span><span class="sxs-lookup"><span data-stu-id="39992-114">In most cases, an application should retrieve the current style and then add or remove the inappropriate bits.</span></span> <span data-ttu-id="39992-115">Este procedimiento permite que los distintos estilos de ventana internos utilizados por Windows permanezcan intactos.</span><span class="sxs-lookup"><span data-stu-id="39992-115">This procedure allows various internal window styles used by Windows to remain intact.</span></span>

## <a name="requirements"></a><span data-ttu-id="39992-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39992-116">Requirements</span></span>



| <span data-ttu-id="39992-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="39992-117">Requirement</span></span> | <span data-ttu-id="39992-118">Value</span><span class="sxs-lookup"><span data-stu-id="39992-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39992-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39992-119">Header</span></span><br/>  | <dl> <span data-ttu-id="39992-120"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39992-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="39992-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39992-121">Library</span></span><br/> | <dl> <span data-ttu-id="39992-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="39992-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39992-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="39992-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39992-124">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="39992-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




