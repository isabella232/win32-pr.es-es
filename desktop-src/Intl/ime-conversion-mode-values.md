---
description: Estos valores se usan con las funciones ImmGetConversionStatus y ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valores del modo de conversión IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59b9f1a8d5015e78a5249d3499fc55e1a94d941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154585"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="a9c3b-103">Valores del modo de conversión IME</span><span class="sxs-lookup"><span data-stu-id="a9c3b-103">IME Conversion Mode Values</span></span>

<span data-ttu-id="a9c3b-104">Estos valores se usan con las funciones [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) y [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="a9c3b-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="a9c3b-105">bit</span><span class="sxs-lookup"><span data-stu-id="a9c3b-105">Bit</span></span>                      | <span data-ttu-id="a9c3b-106">Significado</span><span class="sxs-lookup"><span data-stu-id="a9c3b-106">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c3b-107">CMODE de IME \_ \_ alfanumérica</span><span class="sxs-lookup"><span data-stu-id="a9c3b-107">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="a9c3b-108">Modo de entrada alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-108">Alphanumeric input mode.</span></span> <span data-ttu-id="a9c3b-109">Este es el valor predeterminado, definido como 0x0000.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-109">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="a9c3b-110">CMODE de IME \_ \_</span><span class="sxs-lookup"><span data-stu-id="a9c3b-110">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="a9c3b-111">Se establece en 1 si el modo de entrada del código de carácter; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-111">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="a9c3b-112">CMODE de IME \_ \_</span><span class="sxs-lookup"><span data-stu-id="a9c3b-112">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="a9c3b-113">Se establece en 1 si el modo de conversión de EUDC; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-113">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="a9c3b-114">IME \_ CMODE \_ corregido</span><span class="sxs-lookup"><span data-stu-id="a9c3b-114">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="a9c3b-115">**Windows Me/98, windows 2000 y Windows XP:** Se establece en 1 si el modo de conversión es fijo; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-115">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="a9c3b-116">IME \_ CMODE \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="a9c3b-116">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="a9c3b-117">Se establece en 1 si el modo de forma completa; 0 si el modo de mitad de la forma.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-117">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="a9c3b-118">IME \_ CMODE \_ HANJACONVERT</span><span class="sxs-lookup"><span data-stu-id="a9c3b-118">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="a9c3b-119">Se establece en 1 si el modo de conversión HANJA; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-119">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="a9c3b-120">\_CMODE \_ katakana de IME</span><span class="sxs-lookup"><span data-stu-id="a9c3b-120">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="a9c3b-121">Se establece en 1 si el modo KATAKANA; 0 si el modo es HIRAGANA.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-121">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="a9c3b-122">IME \_ CMODE \_ nativo</span><span class="sxs-lookup"><span data-stu-id="a9c3b-122">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="a9c3b-123">Se establece en 1 si el modo nativo; 0 si el modo es alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-123">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="a9c3b-124">CMODE de IME \_ \_</span><span class="sxs-lookup"><span data-stu-id="a9c3b-124">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="a9c3b-125">Se establece en 1 para evitar el procesamiento de conversiones por parte de IME; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="a9c3b-126">IME \_ CMODE \_ Roman</span><span class="sxs-lookup"><span data-stu-id="a9c3b-126">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="a9c3b-127">Se establece en 1 si el modo de entrada ROMAN; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-127">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="a9c3b-128">IME \_ CMODE \_ SOFTKBD</span><span class="sxs-lookup"><span data-stu-id="a9c3b-128">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="a9c3b-129">Se establece en 1 si el modo de teclado en pantalla; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-129">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="a9c3b-130">\_símbolo CMODE de IME \_</span><span class="sxs-lookup"><span data-stu-id="a9c3b-130">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="a9c3b-131">Se establece en 1 si el modo de conversión de símbolos; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-131">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="a9c3b-132">Todos los demás bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="a9c3b-132">All other bits are reserved.</span></span>

 

 



