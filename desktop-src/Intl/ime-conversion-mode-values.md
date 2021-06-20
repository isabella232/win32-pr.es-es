---
description: Revise la lista de valores de modo de conversión del editor de métodos de entrada (IME). Estos valores se usan con las funciones ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valores del modo de conversión de IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c52bc2f8f6f9fc87df48a15c66ce24b33e51742
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406758"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="4aac6-104">Valores del modo de conversión de IME</span><span class="sxs-lookup"><span data-stu-id="4aac6-104">IME Conversion Mode Values</span></span>

<span data-ttu-id="4aac6-105">Estos valores se usan con las funciones [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) [**e ImmSetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)</span><span class="sxs-lookup"><span data-stu-id="4aac6-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="4aac6-106">bit</span><span class="sxs-lookup"><span data-stu-id="4aac6-106">Bit</span></span>                      | <span data-ttu-id="4aac6-107">Significado</span><span class="sxs-lookup"><span data-stu-id="4aac6-107">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aac6-108">IME \_ CMODE \_ ALPHANUMERIC</span><span class="sxs-lookup"><span data-stu-id="4aac6-108">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="4aac6-109">Modo de entrada alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="4aac6-109">Alphanumeric input mode.</span></span> <span data-ttu-id="4aac6-110">Este es el valor predeterminado, definido como 0x0000.</span><span class="sxs-lookup"><span data-stu-id="4aac6-110">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="4aac6-111">IME \_ CMODE \_ CHARCODE</span><span class="sxs-lookup"><span data-stu-id="4aac6-111">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="4aac6-112">Se establece en 1 si el modo de entrada de código de caracteres; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="4aac6-112">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="4aac6-113">EUDC \_ de CMODE \_ de IME</span><span class="sxs-lookup"><span data-stu-id="4aac6-113">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="4aac6-114">Se establece en 1 si el modo de conversión eudc; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="4aac6-114">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="4aac6-115">IME \_ CMODE \_ FIXED</span><span class="sxs-lookup"><span data-stu-id="4aac6-115">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="4aac6-116">**Windows Me/98, Windows 2000, Windows XP:** Se establece en 1 si el modo de conversión es fijo; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="4aac6-116">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="4aac6-117">FULLSHAPE \_ de CMODE de IME \_</span><span class="sxs-lookup"><span data-stu-id="4aac6-117">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="4aac6-118">Se establece en 1 si el modo de forma completa; 0 si el modo de forma media.</span><span class="sxs-lookup"><span data-stu-id="4aac6-118">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="4aac6-119">IME \_ CMODE \_ HANJACONVERT</span><span class="sxs-lookup"><span data-stu-id="4aac6-119">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="4aac6-120">Se establece en 1 si el modo de conversión HANJA; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="4aac6-120">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="4aac6-121">IME \_ CMODE \_ KATAKANA</span><span class="sxs-lookup"><span data-stu-id="4aac6-121">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="4aac6-122">Se establece en 1 si el modo KATAKANA; 0 si el modo HIRAGANA.</span><span class="sxs-lookup"><span data-stu-id="4aac6-122">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="4aac6-123">IME \_ CMODE \_ NATIVE</span><span class="sxs-lookup"><span data-stu-id="4aac6-123">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="4aac6-124">Se establece en 1 si el modo NATIVE; 0 si el modo ALFANUMERIC.</span><span class="sxs-lookup"><span data-stu-id="4aac6-124">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="4aac6-125">IME \_ CMODE \_ NOCONVERSION</span><span class="sxs-lookup"><span data-stu-id="4aac6-125">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="4aac6-126">Establezca en 1 para evitar el procesamiento de conversiones por IME; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="4aac6-126">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="4aac6-127">IME \_ CMODE \_ ROMAN</span><span class="sxs-lookup"><span data-stu-id="4aac6-127">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="4aac6-128">Se establece en 1 si el modo de entrada ROMAN; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="4aac6-128">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="4aac6-129">\_SOFTKBD de CMODE de IME \_</span><span class="sxs-lookup"><span data-stu-id="4aac6-129">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="4aac6-130">Se establece en 1 si el modo de teclado flexible; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="4aac6-130">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="4aac6-131">SÍMBOLO \_ CMODE de IME \_</span><span class="sxs-lookup"><span data-stu-id="4aac6-131">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="4aac6-132">Se establece en 1 si el modo de conversión SYMBOL; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="4aac6-132">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="4aac6-133">Todos los demás bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="4aac6-133">All other bits are reserved.</span></span>

 

 



