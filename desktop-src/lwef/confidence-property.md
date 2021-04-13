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
# <a name="confidence-property"></a>Propiedad Confidence

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece si la **confianza** del cliente aparece en la sugerencia de escucha.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID ***"). Comandos ("*** name ***")**. * ** *  \[  =  *número* de confianza\]



| Parte     | Descripción                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| *Number* | Expresión numérica que se evalúa como un entero largo que identifica el valor de confianza para el [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si el valor de confianza devuelto de la mejor coincidencia (UserInput. Confidence) no supera el valor establecido para la propiedad **Confidence** , se muestra el texto proporcionado en [**ConfidenceText**](confidencetext-property.md) en la sugerencia de escucha.

 

 