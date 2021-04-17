---
description: El método MakeIdentityPalette intenta crear un &\# 0034; paleta de identidad, &\# 0034; definido como uno que se asigna directamente a la paleta seleccionada en el dispositivo de pantalla.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Método CImagePalette. MakeIdentityPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e105652108e74907375408f0bd8946c69194202
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670495"
---
# <a name="cimagepalettemakeidentitypalette-method"></a><span data-ttu-id="2bbe9-103">CImagePalette. MakeIdentityPalette, método</span><span class="sxs-lookup"><span data-stu-id="2bbe9-103">CImagePalette.MakeIdentityPalette method</span></span>

<span data-ttu-id="2bbe9-104">El `MakeIdentityPalette` método intenta crear una "paleta de identidad" definida como una que se asigna directamente a la paleta seleccionada en el dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2bbe9-104">The `MakeIdentityPalette` method attempts to make an "identity palette," defined as one that maps directly to the palette selected in the display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bbe9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bbe9-105">Syntax</span></span>


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="2bbe9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bbe9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bbe9-107">*pEntry*</span><span class="sxs-lookup"><span data-stu-id="2bbe9-107">*pEntry*</span></span> 
</dt> <dd>

<span data-ttu-id="2bbe9-108">Puntero a una matriz de entradas de la paleta.</span><span class="sxs-lookup"><span data-stu-id="2bbe9-108">Pointer to an array of palette entries.</span></span>

</dd> <dt>

<span data-ttu-id="2bbe9-109">*iColours*</span><span class="sxs-lookup"><span data-stu-id="2bbe9-109">*iColours*</span></span> 
</dt> <dd>

<span data-ttu-id="2bbe9-110">Número de entradas de la paleta en *pEntry*.</span><span class="sxs-lookup"><span data-stu-id="2bbe9-110">Number of palette entries in *pEntry*.</span></span>

</dd> <dt>

<span data-ttu-id="2bbe9-111">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="2bbe9-111">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="2bbe9-112">Puntero a una cadena que contiene el nombre del dispositivo de pantalla, devuelto por la función **EnumDisplayDevices** de GDI.</span><span class="sxs-lookup"><span data-stu-id="2bbe9-112">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="2bbe9-113">Para usar el dispositivo de pantalla principal, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="2bbe9-113">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bbe9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bbe9-114">Return value</span></span>

<span data-ttu-id="2bbe9-115">Devuelve S \_ correcto si es correcto o s \_ false si no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="2bbe9-115">Returns S\_OK if successful or S\_FALSE if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bbe9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bbe9-116">Remarks</span></span>

<span data-ttu-id="2bbe9-117">Este método compara las entradas reservadas en la paleta del sistema con las entradas correspondientes de la matriz *pEntry* .</span><span class="sxs-lookup"><span data-stu-id="2bbe9-117">This method compares the reserved entries in the system palette against the corresponding entries in the *pEntry* array.</span></span> <span data-ttu-id="2bbe9-118">Si coinciden exactamente, el método establece la \_ marca PC nocollapse en las entradas de la paleta restantes (no reservadas) en *pEntry*.</span><span class="sxs-lookup"><span data-stu-id="2bbe9-118">If they match exactly, the method sets the PC\_NOCOLLAPSE flag in the remaining (non-reserved) palette entries in *pEntry*.</span></span> <span data-ttu-id="2bbe9-119">Esta marca evita que GDI intente asignar las entradas de la paleta lógica a las entradas de la paleta del sistema.</span><span class="sxs-lookup"><span data-stu-id="2bbe9-119">This flag prevents GDI from trying map logical palette entries to system palette entries.</span></span>

<span data-ttu-id="2bbe9-120">El método [**CImagePalette:: MakePalette**](cimagepalette-makepalette.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="2bbe9-120">The [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bbe9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bbe9-121">Requirements</span></span>



| <span data-ttu-id="2bbe9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bbe9-122">Requirement</span></span> | <span data-ttu-id="2bbe9-123">Value</span><span class="sxs-lookup"><span data-stu-id="2bbe9-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bbe9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bbe9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2bbe9-125"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bbe9-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2bbe9-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2bbe9-126">Library</span></span><br/> | <dl> <span data-ttu-id="2bbe9-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2bbe9-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bbe9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bbe9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bbe9-129">**Clase CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="2bbe9-129">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




