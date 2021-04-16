---
description: Especifica si el color especificado es un color de texto especial.
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: FSpecialTextIMEColorStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialTextIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: cfaf83aeb2fcb03ab61c1280ec821174117026fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649663"
---
# <a name="fspecialtextimecolorstyle-function"></a><span data-ttu-id="4780f-103">FSpecialTextIMEColorStyle función)</span><span class="sxs-lookup"><span data-stu-id="4780f-103">FSpecialTextIMEColorStyle function</span></span>

<span data-ttu-id="4780f-104">Especifica si el color especificado es un color de texto especial.</span><span class="sxs-lookup"><span data-stu-id="4780f-104">Specifies whether the specified color is a special text color.</span></span>

## <a name="syntax"></a><span data-ttu-id="4780f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4780f-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="4780f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4780f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4780f-107">*pcolorstyle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4780f-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4780f-108">Una estructura **IMECOLORSTY** devuelta por una función [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="4780f-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4780f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4780f-109">Return value</span></span>

<span data-ttu-id="4780f-110">Devuelve **verdadero** cuando el color es un color de texto especial.</span><span class="sxs-lookup"><span data-stu-id="4780f-110">Returns **TRUE** when the color is a special text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="4780f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4780f-111">Remarks</span></span>

<span data-ttu-id="4780f-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4780f-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4780f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4780f-113">Requirements</span></span>



| <span data-ttu-id="4780f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4780f-114">Requirement</span></span> | <span data-ttu-id="4780f-115">Value</span><span class="sxs-lookup"><span data-stu-id="4780f-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4780f-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4780f-116">DLL</span></span><br/> | <dl> <span data-ttu-id="4780f-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4780f-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4780f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4780f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4780f-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="4780f-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="4780f-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="4780f-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
