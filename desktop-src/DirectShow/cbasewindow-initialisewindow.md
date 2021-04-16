---
description: El método InitialiseWindow inicializa la ventana.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Inimétodo tialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679563"
---
# <a name="cbasewindowinitialisewindow-method"></a><span data-ttu-id="a88ef-103">CBaseWindow.Inimétodo tialiseWindow</span><span class="sxs-lookup"><span data-stu-id="a88ef-103">CBaseWindow.InitialiseWindow method</span></span>

<span data-ttu-id="a88ef-104">El `InitialiseWindow` método inicializa la ventana.</span><span class="sxs-lookup"><span data-stu-id="a88ef-104">The `InitialiseWindow` method initializes the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="a88ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a88ef-105">Syntax</span></span>


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="a88ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a88ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a88ef-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="a88ef-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a88ef-108">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="a88ef-108">Handle to the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a88ef-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a88ef-109">Return value</span></span>

<span data-ttu-id="a88ef-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a88ef-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a88ef-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a88ef-111">Remarks</span></span>

<span data-ttu-id="a88ef-112">De forma predeterminada, este método recupera un identificador para el contexto de dispositivo (DC) de la ventana y crea un controlador de dominio de memoria compatible.</span><span class="sxs-lookup"><span data-stu-id="a88ef-112">By default, this method retrieves a handle to the window's device context (DC) and creates a compatible memory DC.</span></span> <span data-ttu-id="a88ef-113">Sin embargo, si el valor de la marca [**CBaseWindow:: m \_ BDoGetDC**](cbasewindow-m-bdogetdc.md) es **false**, este método no recupera los contextos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a88ef-113">If the value of the [**CBaseWindow::m\_bDoGetDC**](cbasewindow-m-bdogetdc.md) flag is **FALSE**, however, this method does not retrieve the device contexts.</span></span> <span data-ttu-id="a88ef-114">El controlador de dominio de memoria es útil para seleccionar mapas de bits antes de blitting a la ventana.</span><span class="sxs-lookup"><span data-stu-id="a88ef-114">The memory DC is useful for selecting bitmaps before blitting them to the window.</span></span>

<span data-ttu-id="a88ef-115">El método [**CBaseWindow::D ocreatewindow**](cbasewindow-docreatewindow.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="a88ef-115">The [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a88ef-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a88ef-116">Requirements</span></span>



| <span data-ttu-id="a88ef-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a88ef-117">Requirement</span></span> | <span data-ttu-id="a88ef-118">Value</span><span class="sxs-lookup"><span data-stu-id="a88ef-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a88ef-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a88ef-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a88ef-120"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a88ef-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a88ef-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a88ef-121">Library</span></span><br/> | <dl> <span data-ttu-id="a88ef-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a88ef-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a88ef-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a88ef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88ef-124">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="a88ef-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




