---
title: Propiedad Caption (objeto Command)
description: Propiedad Caption
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714513"
---
# <a name="caption-property-command-object"></a>Propiedad Caption (objeto Command)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Determina el texto que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en el menú emergente del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_"). Comandos ("_*_Name_*_")._ *  \[  =  *Cadena* de leyenda\]



| Parte     | Descripción                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| *string* | Expresión de cadena que se evalúa como el texto que se muestra como título del **comando**. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para especificar una tecla de acceso (tecla de acceso no alineada) para el **título**, incluya un carácter de y comercial (&) antes de ese carácter.

Si no define un **VoiceCaption** para el comando, se usará la configuración del **título** .

 

 
