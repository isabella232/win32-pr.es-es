---
description: El método RefreshDisplayType actualiza el formato de vídeo del objeto para que coincida con la presentación especificada.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Método CImageDisplay. RefreshDisplayType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f8010dcfe490363903ff455bedb61254b69b825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680460"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a><span data-ttu-id="2f5e2-103">CImageDisplay. RefreshDisplayType, método</span><span class="sxs-lookup"><span data-stu-id="2f5e2-103">CImageDisplay.RefreshDisplayType method</span></span>

<span data-ttu-id="2f5e2-104">El `RefreshDisplayType` método actualiza el formato de vídeo del objeto para que coincida con la presentación especificada.</span><span class="sxs-lookup"><span data-stu-id="2f5e2-104">The `RefreshDisplayType` method updates the object's video format to match the specified display.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f5e2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f5e2-105">Syntax</span></span>


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a><span data-ttu-id="2f5e2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f5e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f5e2-107">*szDeviceName*</span><span class="sxs-lookup"><span data-stu-id="2f5e2-107">*szDeviceName*</span></span> 
</dt> <dd>

<span data-ttu-id="2f5e2-108">Puntero a una cadena que contiene el nombre del dispositivo de pantalla, devuelto por la función **EnumDisplayDevices** de GDI.</span><span class="sxs-lookup"><span data-stu-id="2f5e2-108">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="2f5e2-109">Para usar el dispositivo de pantalla principal, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="2f5e2-109">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f5e2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f5e2-110">Return value</span></span>

<span data-ttu-id="2f5e2-111">Devuelve \_ si es correcto, o E \_ produce un error si no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="2f5e2-111">Returns S\_OK if successful, or E\_FAIL if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f5e2-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f5e2-112">Remarks</span></span>

<span data-ttu-id="2f5e2-113">Este método inicializa el miembro **de \_ visualización m** en un tipo de vídeo que corresponde al modo de presentación en el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2f5e2-113">This method initializes the **m\_Display** member to a video type that corresponds to the display mode on the specified device.</span></span>

<span data-ttu-id="2f5e2-114">Llame a este método cada vez que \_ se reciba un mensaje de DISPLAYCHANGED de WM, o para especificar un dispositivo de pantalla secundario.</span><span class="sxs-lookup"><span data-stu-id="2f5e2-114">Call this method whenever a WM\_DISPLAYCHANGED message is received, or to specify a secondary display device.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f5e2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f5e2-115">Requirements</span></span>



| <span data-ttu-id="2f5e2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f5e2-116">Requirement</span></span> | <span data-ttu-id="2f5e2-117">Value</span><span class="sxs-lookup"><span data-stu-id="2f5e2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f5e2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f5e2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2f5e2-119"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f5e2-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f5e2-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f5e2-120">Library</span></span><br/> | <dl> <span data-ttu-id="2f5e2-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2f5e2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f5e2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f5e2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f5e2-123">**Clase CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="2f5e2-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




