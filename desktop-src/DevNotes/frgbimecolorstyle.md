---
description: Especifica si el color especificado es un color RGB.
ms.assetid: 16b48644-c2d5-4383-836a-122f44504638
title: FRGBIMEColorStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRGBIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: df11a2ad972791eaf7049bdef5fa927aaa4119da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649838"
---
# <a name="frgbimecolorstyle-function"></a><span data-ttu-id="dc2dc-103">FRGBIMEColorStyle función)</span><span class="sxs-lookup"><span data-stu-id="dc2dc-103">FRGBIMEColorStyle function</span></span>

<span data-ttu-id="dc2dc-104">Especifica si el color especificado es un color RGB.</span><span class="sxs-lookup"><span data-stu-id="dc2dc-104">Specifies whether the specified color is an RGB color.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc2dc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc2dc-105">Syntax</span></span>


```C++
BOOL __cdecl FRGBIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="dc2dc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc2dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc2dc-107">*pcolorstyle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc2dc-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc2dc-108">Una estructura **IMECOLORSTY** devuelta por una función [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="dc2dc-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc2dc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc2dc-109">Return value</span></span>

<span data-ttu-id="dc2dc-110">Devuelve **verdadero** cuando el color es un color RGB.</span><span class="sxs-lookup"><span data-stu-id="dc2dc-110">Returns **TRUE** when the color is an RGB color.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc2dc-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc2dc-111">Remarks</span></span>

<span data-ttu-id="dc2dc-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="dc2dc-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc2dc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc2dc-113">Requirements</span></span>



| <span data-ttu-id="dc2dc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc2dc-114">Requirement</span></span> | <span data-ttu-id="dc2dc-115">Value</span><span class="sxs-lookup"><span data-stu-id="dc2dc-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2dc-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc2dc-116">DLL</span></span><br/> | <dl> <span data-ttu-id="dc2dc-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc2dc-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc2dc-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc2dc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc2dc-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="dc2dc-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="dc2dc-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="dc2dc-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
