---
description: Especifica si el color especificado es un color de Windows.
ms.assetid: 0d2b2039-938c-4f9d-8ddc-9eb711f55009
title: FWinIMEColorStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FWinIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 28731672f5f1aff385f9051ba8b641b7cdcdf83c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649652"
---
# <a name="fwinimecolorstyle-function"></a><span data-ttu-id="ae079-103">FWinIMEColorStyle función)</span><span class="sxs-lookup"><span data-stu-id="ae079-103">FWinIMEColorStyle function</span></span>

<span data-ttu-id="ae079-104">Especifica si el color especificado es un color de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae079-104">Specifies whether the specified color is a Windows color.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae079-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae079-105">Syntax</span></span>


```C++
BOOL __cdecl FWinIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="ae079-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae079-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae079-107">*pcolorstyle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae079-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae079-108">Una estructura **IMECOLORSTY** devuelta por una función [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="ae079-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae079-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae079-109">Return value</span></span>

<span data-ttu-id="ae079-110">Devuelve **verdadero** cuando el color es un color de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae079-110">Returns **TRUE** when the color is a Windows color.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae079-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae079-111">Remarks</span></span>

<span data-ttu-id="ae079-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ae079-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae079-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae079-113">Requirements</span></span>



| <span data-ttu-id="ae079-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae079-114">Requirement</span></span> | <span data-ttu-id="ae079-115">Value</span><span class="sxs-lookup"><span data-stu-id="ae079-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae079-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae079-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ae079-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae079-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae079-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae079-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae079-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="ae079-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="ae079-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="ae079-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
