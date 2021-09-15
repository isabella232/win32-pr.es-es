---
title: Propiedad ConfidenceText
description: Propiedad ConfidenceText
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb30b5ac481b6011d3575ab99dbc389f426b085d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567564"
---
# <a name="confidencetext-property"></a>Propiedad ConfidenceText

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el valor **de ConfidenceText del** cliente que aparece en la sugerencia de escucha.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands("_*_name_*_")_*. **ConfidenceText** \[  =  *string*\]



| Parte     | Descripción                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| *string* | Expresión de cadena que se evalúa como el texto de **ConfidenceText** para el [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando el valor de confianza devuelto de la mejor coincidencia [](confidence-property.md) (UserInput.Confidence) no supera la configuración confianza, el servidor muestra el texto proporcionado en **ConfidenceText** en la sugerencia de escucha.

 

 