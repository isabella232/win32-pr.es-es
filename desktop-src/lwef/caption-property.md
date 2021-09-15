---
title: Propiedad Caption (objeto Command)
description: Obtenga información sobre la propiedad Caption del objeto Command. Microsoft Agent está en desuso a partir Windows 7.
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0eb41def3b183fe4185b9c66a9ca5cd172372fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567597"
---
# <a name="caption-property-command-object"></a>Propiedad Caption (objeto Command)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Determina el texto que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en el menú emergente del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands("_*_name_*_"). Cadena de_ *  \[  =  *título*\]



| Parte     | Descripción                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| *string* | Expresión de cadena que se evalúa como el texto mostrado como título del **comando**. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para especificar una clave de acceso (mnemotécnica sin línea) para el título **,** incluya un carácter de yerba (&) antes de ese carácter.

Si no define **voiceCaption para** el comando, se usará la configuración de título. 

 

 
