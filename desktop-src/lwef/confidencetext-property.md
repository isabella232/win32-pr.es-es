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
# <a name="confidencetext-property"></a>Propiedad ConfidenceText

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el **ConfidenceText** del cliente que aparece en la sugerencia de escucha.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

* agente ***. Caracteres ("*** CharacterID ***"). Comandos ("*** name ***")**.  \[ ConfidenceText  =  *cadena*\]



| Parte     | Descripción                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| *string* | Expresión de cadena que se evalúa como el texto de **ConfidenceText** para el [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando el valor de confianza devuelto de la mejor coincidencia (UserInput. Confidence) no supera la configuración de [**confianza**](confidence-property.md) , el servidor muestra el texto proporcionado en **ConfidenceText** en la sugerencia de escucha.

 

 