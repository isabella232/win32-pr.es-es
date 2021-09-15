---
title: Propiedad De confianza
description: Propiedad De confianza
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567565"
---
# <a name="confidence-property"></a>Propiedad De confianza

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece si la confianza **del** cliente aparece en la sugerencia de escucha.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands("_*_name_*_")_*.**Confidence* *  \[  =  *Number*\]



| Parte     | Descripción                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| *Number* | Expresión numérica que se evalúa como un entero Long que identifica el valor de confianza para [**el comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si el valor de confianza devuelto de la mejor coincidencia (UserInput.Confidence) no supera el valor establecido para la **propiedad Confidence,** el texto proporcionado en [**ConfidenceText**](confidencetext-property.md) se muestra en la sugerencia de escucha.

 

 