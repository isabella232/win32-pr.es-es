---
description: El método UpdateColourTable actualiza la tabla de colores con una nueva paleta.
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: Método CDrawImage. UpdateColourTable (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UpdateColourTable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcffdf9e7deaaac5a01f6559ee557c978fcda88f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671824"
---
# <a name="cdrawimageupdatecolourtable-method"></a><span data-ttu-id="fed05-103">CDrawImage. UpdateColourTable, método</span><span class="sxs-lookup"><span data-stu-id="fed05-103">CDrawImage.UpdateColourTable method</span></span>

<span data-ttu-id="fed05-104">El `UpdateColourTable` método actualiza la tabla de colores con una nueva paleta.</span><span class="sxs-lookup"><span data-stu-id="fed05-104">The `UpdateColourTable` method updates the color table with a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="fed05-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fed05-105">Syntax</span></span>


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a><span data-ttu-id="fed05-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fed05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fed05-107">*cámaras*</span><span class="sxs-lookup"><span data-stu-id="fed05-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="fed05-108">Contexto de dispositivo que contiene la imagen.</span><span class="sxs-lookup"><span data-stu-id="fed05-108">Device context containing the image.</span></span>

</dd> <dt>

<span data-ttu-id="fed05-109">*pbmi*</span><span class="sxs-lookup"><span data-stu-id="fed05-109">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="fed05-110">Puntero a una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que contiene la nueva paleta.</span><span class="sxs-lookup"><span data-stu-id="fed05-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure containing the new palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fed05-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fed05-111">Return value</span></span>

<span data-ttu-id="fed05-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fed05-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fed05-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fed05-113">Requirements</span></span>



| <span data-ttu-id="fed05-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fed05-114">Requirement</span></span> | <span data-ttu-id="fed05-115">Value</span><span class="sxs-lookup"><span data-stu-id="fed05-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed05-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fed05-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fed05-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fed05-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fed05-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fed05-118">Library</span></span><br/> | <dl> <span data-ttu-id="fed05-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fed05-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fed05-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="fed05-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed05-121">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="fed05-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




