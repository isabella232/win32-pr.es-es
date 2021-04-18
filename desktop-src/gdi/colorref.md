---
Description: El valor COLORREF se usa para especificar un color RGB.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (WINDEF. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104998881"
---
# <a name="colorref"></a><span data-ttu-id="f2e0d-103">COLORREF</span><span class="sxs-lookup"><span data-stu-id="f2e0d-103">COLORREF</span></span>

<span data-ttu-id="f2e0d-104">El valor COLORREF se usa para especificar un color [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="f2e0d-104">The COLORREF value is used to specify an [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color.</span></span>


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a><span data-ttu-id="f2e0d-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2e0d-105">Remarks</span></span>

<span data-ttu-id="f2e0d-106">Al especificar un color [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) explícito, el valor de **COLORREF** tiene el formato hexadecimal siguiente:</span><span class="sxs-lookup"><span data-stu-id="f2e0d-106">When specifying an explicit [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color, the **COLORREF** value has the following hexadecimal form:</span></span>

`0x00bbggrr`

<span data-ttu-id="f2e0d-107">El byte de orden inferior contiene un valor para la intensidad relativa de rojo; el segundo byte contiene un valor para Green; y el tercer byte contiene un valor para Blue.</span><span class="sxs-lookup"><span data-stu-id="f2e0d-107">The low-order byte contains a value for the relative intensity of red; the second byte contains a value for green; and the third byte contains a value for blue.</span></span> <span data-ttu-id="f2e0d-108">El byte de orden superior debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f2e0d-108">The high-order byte must be zero.</span></span> <span data-ttu-id="f2e0d-109">El valor máximo de un solo byte es 0xFF.</span><span class="sxs-lookup"><span data-stu-id="f2e0d-109">The maximum value for a single byte is 0xFF.</span></span>

<span data-ttu-id="f2e0d-110">Para crear un valor de color **COLORREF** , use la macro [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="f2e0d-110">To create a **COLORREF** color value, use the [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="f2e0d-111">Para extraer los valores individuales de los componentes rojo, verde y azul de un valor de color, use las macros [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)y [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f2e0d-111">To extract the individual values for the red, green, and blue components of a color value, use the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span>

## <a name="example"></a><span data-ttu-id="f2e0d-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2e0d-112">Example</span></span>

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

<span data-ttu-id="f2e0d-113">Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples) en github.</span><span class="sxs-lookup"><span data-stu-id="f2e0d-113">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e0d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2e0d-114">Requirements</span></span>



| <span data-ttu-id="f2e0d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2e0d-115">Requirement</span></span> | <span data-ttu-id="f2e0d-116">Value</span><span class="sxs-lookup"><span data-stu-id="f2e0d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e0d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2e0d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e0d-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f2e0d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f2e0d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2e0d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e0d-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2e0d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2e0d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2e0d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2e0d-122"><dt>WINDEF. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2e0d-122"><dt>Windef.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e0d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2e0d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e0d-124">Información general sobre colores</span><span class="sxs-lookup"><span data-stu-id="f2e0d-124">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="f2e0d-125">Estructuras de color</span><span class="sxs-lookup"><span data-stu-id="f2e0d-125">Color Structures</span></span>](color-structures.md)
</dt> <dt>

[<span data-ttu-id="f2e0d-126">GetBValue</span><span class="sxs-lookup"><span data-stu-id="f2e0d-126">GetBValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[<span data-ttu-id="f2e0d-127">GetGValue</span><span class="sxs-lookup"><span data-stu-id="f2e0d-127">GetGValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[<span data-ttu-id="f2e0d-128">**GetRValue**</span><span class="sxs-lookup"><span data-stu-id="f2e0d-128">**GetRValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[<span data-ttu-id="f2e0d-129">RGB</span><span class="sxs-lookup"><span data-stu-id="f2e0d-129">RGB</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




