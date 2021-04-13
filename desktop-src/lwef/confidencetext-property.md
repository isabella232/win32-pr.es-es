---
title: Propiedad ConfidenceText
description: Propiedad ConfidenceText
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb30b5ac481b6011d3575ab99dbc389f426b085d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420638"
---
# <a name="confidencetext-property"></a><span data-ttu-id="31e30-103">Propiedad ConfidenceText</span><span class="sxs-lookup"><span data-stu-id="31e30-103">ConfidenceText Property</span></span>

<span data-ttu-id="31e30-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="31e30-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="31e30-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="31e30-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="31e30-106">Devuelve o establece el **ConfidenceText** del cliente que aparece en la sugerencia de escucha.</span><span class="sxs-lookup"><span data-stu-id="31e30-106">Returns or sets the client's **ConfidenceText** that appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="31e30-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="31e30-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="31e30-108">\* agente ***. Caracteres ("*** CharacterID ***"). Comandos ("*** name \***")**.  \[ ConfidenceText  =  *cadena*\]</span><span class="sxs-lookup"><span data-stu-id="31e30-108">\*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.**ConfidenceText**\[ = *string*\]</span></span>



| <span data-ttu-id="31e30-109">Parte</span><span class="sxs-lookup"><span data-stu-id="31e30-109">Part</span></span>     | <span data-ttu-id="31e30-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="31e30-110">Description</span></span>                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31e30-111">*string*</span><span class="sxs-lookup"><span data-stu-id="31e30-111">*string*</span></span> | <span data-ttu-id="31e30-112">Expresión de cadena que se evalúa como el texto de **ConfidenceText** para el [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="31e30-112">A string expression that evaluates to the text for the **ConfidenceText** for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31e30-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31e30-113">Remarks</span></span>

<span data-ttu-id="31e30-114">Cuando el valor de confianza devuelto de la mejor coincidencia (UserInput. Confidence) no supera la configuración de [**confianza**](confidence-property.md) , el servidor muestra el texto proporcionado en **ConfidenceText** en la sugerencia de escucha.</span><span class="sxs-lookup"><span data-stu-id="31e30-114">When the returned confidence value of the best match (UserInput.Confidence) does not exceed the [**Confidence**](confidence-property.md) setting, the server displays the text supplied in **ConfidenceText** in the Listening Tip.</span></span>

 

 