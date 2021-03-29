---
description: Estos valores se usan con las funciones ImmGetConversionStatus y ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valores del modo de oración IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2fb9d25b2c3b1828e8c36aca554468f6447af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277043"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="069eb-103">Valores del modo de oración IME</span><span class="sxs-lookup"><span data-stu-id="069eb-103">IME Sentence Mode Values</span></span>

<span data-ttu-id="069eb-104">Estos valores se usan con las funciones [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) y [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="069eb-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="069eb-105">Constante</span><span class="sxs-lookup"><span data-stu-id="069eb-105">Constant</span></span>                  | <span data-ttu-id="069eb-106">Definición</span><span class="sxs-lookup"><span data-stu-id="069eb-106">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="069eb-107">SMODE de IME \_ \_ automática</span><span class="sxs-lookup"><span data-stu-id="069eb-107">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="069eb-108">El IME realiza el procesamiento de la conversión en modo automático.</span><span class="sxs-lookup"><span data-stu-id="069eb-108">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="069eb-109">IME \_ SMODE \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="069eb-109">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="069eb-110">No hay información para la frase.</span><span class="sxs-lookup"><span data-stu-id="069eb-110">No information for sentence.</span></span>                                               |
| <span data-ttu-id="069eb-111">IME \_ SMODE \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="069eb-111">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="069eb-112">El IME usa la información de frases para predecir el siguiente carácter.</span><span class="sxs-lookup"><span data-stu-id="069eb-112">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="069eb-113">IME \_ SMODE \_ PLURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="069eb-113">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="069eb-114">El IME usa la información de la cláusula plural para llevar a cabo el procesamiento de la conversión.</span><span class="sxs-lookup"><span data-stu-id="069eb-114">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="069eb-115">IME \_ SMODE \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="069eb-115">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="069eb-116">El IME realiza el procesamiento de la conversión en el modo de un solo carácter.</span><span class="sxs-lookup"><span data-stu-id="069eb-116">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="069eb-117">\_conversación SMODE de IME \_</span><span class="sxs-lookup"><span data-stu-id="069eb-117">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="069eb-118">El IME usa el modo de conversación.</span><span class="sxs-lookup"><span data-stu-id="069eb-118">The IME uses conversation mode.</span></span> <span data-ttu-id="069eb-119">Esto resulta útil para las aplicaciones de chat.</span><span class="sxs-lookup"><span data-stu-id="069eb-119">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="069eb-120">Los bits 16 a 31 están reservados para el uso de IME.</span><span class="sxs-lookup"><span data-stu-id="069eb-120">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



