---
description: Convierte una estructura IMECOLORSTY en una estructura COLORREF.
ms.assetid: f7a3eab0-16ca-4c4e-9eda-bead8d1a91b8
title: RGBFromIMEColorStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RGBFromIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 7993253e5e11c45cae3e062467db080201bc1228
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649533"
---
# <a name="rgbfromimecolorstyle-function"></a><span data-ttu-id="7c08c-103">RGBFromIMEColorStyle función)</span><span class="sxs-lookup"><span data-stu-id="7c08c-103">RGBFromIMEColorStyle function</span></span>

<span data-ttu-id="7c08c-104">Convierte una estructura **IMECOLORSTY** en una estructura [**COLORREF**](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="7c08c-104">Converts an **IMECOLORSTY** structure to a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c08c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c08c-105">Syntax</span></span>


```C++
COLORREF RGBFromIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="7c08c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c08c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c08c-107">*pcolorstyle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7c08c-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c08c-108">Una estructura **IMECOLORSTY** devuelta por una función [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="7c08c-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c08c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c08c-109">Return value</span></span>

<span data-ttu-id="7c08c-110">Devuelve una estructura [**COLORREF**](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="7c08c-110">Returns a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c08c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c08c-111">Remarks</span></span>

<span data-ttu-id="7c08c-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7c08c-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c08c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c08c-113">Requirements</span></span>



| <span data-ttu-id="7c08c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c08c-114">Requirement</span></span> | <span data-ttu-id="7c08c-115">Value</span><span class="sxs-lookup"><span data-stu-id="7c08c-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c08c-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c08c-116">DLL</span></span><br/> | <dl> <span data-ttu-id="7c08c-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c08c-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c08c-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c08c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c08c-119">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="7c08c-119">**COLORREF**</span></span>](../gdi/colorref.md)
</dt> <dt>

[<span data-ttu-id="7c08c-120">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="7c08c-120">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="7c08c-121">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="7c08c-121">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
