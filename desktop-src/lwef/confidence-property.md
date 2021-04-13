---
title: Propiedad Confidence
description: Propiedad Confidence
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420575"
---
# <a name="confidence-property"></a><span data-ttu-id="7b831-103">Propiedad Confidence</span><span class="sxs-lookup"><span data-stu-id="7b831-103">Confidence Property</span></span>

<span data-ttu-id="7b831-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7b831-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7b831-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="7b831-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7b831-106">Devuelve o establece si la **confianza** del cliente aparece en la sugerencia de escucha.</span><span class="sxs-lookup"><span data-stu-id="7b831-106">Returns or sets whether the client's **Confidence** appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="7b831-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="7b831-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7b831-108">\*agente ***. Caracteres ("*** CharacterID ***"). Comandos ("*** name \***")**. \* \*\* \*  \[  =  *número* de confianza\]</span><span class="sxs-lookup"><span data-stu-id="7b831-108">*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.\*\*Confidence*\* \[ = *Number*\]</span></span>



| <span data-ttu-id="7b831-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7b831-109">Part</span></span>     | <span data-ttu-id="7b831-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b831-110">Description</span></span>                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b831-111">*Number*</span><span class="sxs-lookup"><span data-stu-id="7b831-111">*Number*</span></span> | <span data-ttu-id="7b831-112">Expresión numérica que se evalúa como un entero largo que identifica el valor de confianza para el [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="7b831-112">A numeric expression that evaluates to a Long integer that identifies confidence value for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b831-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b831-113">Remarks</span></span>

<span data-ttu-id="7b831-114">Si el valor de confianza devuelto de la mejor coincidencia (UserInput. Confidence) no supera el valor establecido para la propiedad **Confidence** , se muestra el texto proporcionado en [**ConfidenceText**](confidencetext-property.md) en la sugerencia de escucha.</span><span class="sxs-lookup"><span data-stu-id="7b831-114">If the returned confidence value of the best match (UserInput.Confidence) does not exceed value you set for the **Confidence** property, the text supplied in [**ConfidenceText**](confidencetext-property.md) is displayed in the Listening Tip.</span></span>

 

 