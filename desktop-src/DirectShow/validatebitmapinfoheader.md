---
description: La función ValidateBitmapInfoHeader comprueba una estructura BITMAPINFOHEADER para detectar algunos errores comunes que pueden producir desbordamientos de búfer o desbordamientos de enteros.
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: Función ValidateBitmapInfoHeader (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681168"
---
# <a name="validatebitmapinfoheader-function"></a><span data-ttu-id="f770d-103">ValidateBitmapInfoHeader función)</span><span class="sxs-lookup"><span data-stu-id="f770d-103">ValidateBitmapInfoHeader function</span></span>

<span data-ttu-id="f770d-104">La `ValidateBitmapInfoHeader` función comprueba una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) para detectar algunos errores comunes que pueden producir desbordamientos de búfer o desbordamientos de enteros.</span><span class="sxs-lookup"><span data-stu-id="f770d-104">The `ValidateBitmapInfoHeader` function checks a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="f770d-105">Esta función no garantiza que la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) sea válida o que el código que usa la estructura sea seguro.</span><span class="sxs-lookup"><span data-stu-id="f770d-105">This function does not guarantee that the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f770d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f770d-106">Syntax</span></span>


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="f770d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f770d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f770d-108">*pbmi*</span><span class="sxs-lookup"><span data-stu-id="f770d-108">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="f770d-109">Puntero a la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="f770d-109">Pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure to validate.</span></span>

</dd> <dt>

<span data-ttu-id="f770d-110">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="f770d-110">*cbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f770d-111">Tamaño del bloque de memoria que contiene la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="f770d-111">Size of the memory block that holds the structure, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f770d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f770d-112">Return value</span></span>

<span data-ttu-id="f770d-113">Devuelve un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="f770d-113">Returns a Boolean value.</span></span> <span data-ttu-id="f770d-114">Si el valor es **false**, la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no es válida.</span><span class="sxs-lookup"><span data-stu-id="f770d-114">If the value is **FALSE**, the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="f770d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f770d-115">Remarks</span></span>

<span data-ttu-id="f770d-116">Esta función protege contra los siguientes errores:</span><span class="sxs-lookup"><span data-stu-id="f770d-116">This function guards against the following errors:</span></span>

-   <span data-ttu-id="f770d-117">Desbordamiento aritmético en el tamaño de la estructura o un tamaño de estructura no válido.</span><span class="sxs-lookup"><span data-stu-id="f770d-117">Arithmetic overflow in the structure size or an invalid structure size.</span></span>
-   <span data-ttu-id="f770d-118">Valor no válido para el miembro **biClrUsed** .</span><span class="sxs-lookup"><span data-stu-id="f770d-118">Invalid value for the **biClrUsed** member.</span></span>
-   <span data-ttu-id="f770d-119">Desbordamiento aritmético en el tamaño de la imagen (**biSizeImage**).</span><span class="sxs-lookup"><span data-stu-id="f770d-119">Arithmetic overflow in the image size (**biSizeImage**).</span></span>
-   <span data-ttu-id="f770d-120">Valores no válidos para el tamaño de la imagen (**biSizeImage**) para los formatos RGB.</span><span class="sxs-lookup"><span data-stu-id="f770d-120">Invalid values for the image size (**biSizeImage**) for RGB formats.</span></span>

<span data-ttu-id="f770d-121">La función no comprueba si la estructura describe un formato de vídeo válido.</span><span class="sxs-lookup"><span data-stu-id="f770d-121">The function does not check whether the structure describes a valid video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="f770d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f770d-122">Requirements</span></span>



| <span data-ttu-id="f770d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f770d-123">Requirement</span></span> | <span data-ttu-id="f770d-124">Value</span><span class="sxs-lookup"><span data-stu-id="f770d-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f770d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f770d-125">Header</span></span><br/> | <dl> <span data-ttu-id="f770d-126"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f770d-126"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f770d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f770d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f770d-128">Funciones de vídeo e imagen</span><span class="sxs-lookup"><span data-stu-id="f770d-128">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




