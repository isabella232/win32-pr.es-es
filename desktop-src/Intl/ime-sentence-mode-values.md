---
description: Revise la lista de valores de modo de oración del editor de métodos de entrada (IME). Estos valores se usan con las funciones ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valores del modo de oración IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 285636ab097bd536e5bd0e4e1869f12c648c3cbb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406768"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="195cc-104">Valores del modo de oración IME</span><span class="sxs-lookup"><span data-stu-id="195cc-104">IME Sentence Mode Values</span></span>

<span data-ttu-id="195cc-105">Estos valores se usan con las [**funciones ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) [**e ImmSetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)</span><span class="sxs-lookup"><span data-stu-id="195cc-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="195cc-106">Constante</span><span class="sxs-lookup"><span data-stu-id="195cc-106">Constant</span></span>                  | <span data-ttu-id="195cc-107">Definición</span><span class="sxs-lookup"><span data-stu-id="195cc-107">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="195cc-108">IME \_ SMODE \_ AUTOMATIC</span><span class="sxs-lookup"><span data-stu-id="195cc-108">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="195cc-109">El IME lleva a cabo el procesamiento de conversión en modo automático.</span><span class="sxs-lookup"><span data-stu-id="195cc-109">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="195cc-110">IME \_ SMODE \_ NONE</span><span class="sxs-lookup"><span data-stu-id="195cc-110">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="195cc-111">No hay información para la oración.</span><span class="sxs-lookup"><span data-stu-id="195cc-111">No information for sentence.</span></span>                                               |
| <span data-ttu-id="195cc-112">IME \_ SMODE \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="195cc-112">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="195cc-113">El IME usa información de frases para predecir el carácter siguiente.</span><span class="sxs-lookup"><span data-stu-id="195cc-113">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="195cc-114">IME \_ SMODE \_ PLURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="195cc-114">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="195cc-115">El IME usa información de la cláusula plural para llevar a cabo el procesamiento de conversión.</span><span class="sxs-lookup"><span data-stu-id="195cc-115">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="195cc-116">IME \_ SMODE \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="195cc-116">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="195cc-117">El IME lleva a cabo el procesamiento de conversión en modo de carácter único.</span><span class="sxs-lookup"><span data-stu-id="195cc-117">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="195cc-118">IME \_ SMODE \_ CONVERSATION</span><span class="sxs-lookup"><span data-stu-id="195cc-118">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="195cc-119">El IME usa el modo de conversación.</span><span class="sxs-lookup"><span data-stu-id="195cc-119">The IME uses conversation mode.</span></span> <span data-ttu-id="195cc-120">Esto es útil para aplicaciones de chat.</span><span class="sxs-lookup"><span data-stu-id="195cc-120">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="195cc-121">Los bits del 16 al 31 están reservados para el uso de IME.</span><span class="sxs-lookup"><span data-stu-id="195cc-121">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



