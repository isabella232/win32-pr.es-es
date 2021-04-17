---
description: El método DoRealisePalette observa la paleta actual de la ventana.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Método CBaseWindow. DoRealisePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660229"
---
# <a name="cbasewindowdorealisepalette-method"></a><span data-ttu-id="1ec2c-103">CBaseWindow. DoRealisePalette, método</span><span class="sxs-lookup"><span data-stu-id="1ec2c-103">CBaseWindow.DoRealisePalette method</span></span>

<span data-ttu-id="1ec2c-104">El `DoRealisePalette` método se obtiene de la paleta actual de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-104">The `DoRealisePalette` method realizes the window's current palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec2c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ec2c-105">Syntax</span></span>


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a><span data-ttu-id="1ec2c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ec2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec2c-107">*bForceBackground*</span><span class="sxs-lookup"><span data-stu-id="1ec2c-107">*bForceBackground*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec2c-108">Valor booleano que especifica si la paleta se ve obligada a ser una paleta de fondo.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-108">Boolean value that specifies whether the palette is forced to be a background palette.</span></span> <span data-ttu-id="1ec2c-109">Para obtener más información, vea **SelectPalette** en el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-109">For more information, see **SelectPalette** in the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec2c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ec2c-110">Return value</span></span>

<span data-ttu-id="1ec2c-111">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="1ec2c-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1ec2c-112">Return code</span></span>                                                                             | <span data-ttu-id="1ec2c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ec2c-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="1ec2c-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1ec2c-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="1ec2c-115">Una llamada interna a **GdiFlush** devolvió un error.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="1ec2c-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1ec2c-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="1ec2c-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="1ec2c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ec2c-118">Remarks</span></span>

<span data-ttu-id="1ec2c-119">El método [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-119">The [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method calls this method.</span></span> <span data-ttu-id="1ec2c-120">Para establecer una nueva paleta, llame al método [**CBaseWindow:: SetPalette**](cbasewindow-setpalette.md) .</span><span class="sxs-lookup"><span data-stu-id="1ec2c-120">To set a new palette, call the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec2c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ec2c-121">Requirements</span></span>



| <span data-ttu-id="1ec2c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ec2c-122">Requirement</span></span> | <span data-ttu-id="1ec2c-123">Value</span><span class="sxs-lookup"><span data-stu-id="1ec2c-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec2c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ec2c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1ec2c-125"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec2c-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ec2c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ec2c-126">Library</span></span><br/> | <dl> <span data-ttu-id="1ec2c-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec2c-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec2c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ec2c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec2c-129">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="1ec2c-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




