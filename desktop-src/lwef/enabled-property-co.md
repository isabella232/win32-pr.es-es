---
title: Propiedad Enabled (objeto Command)
description: Obtenga información sobre la propiedad de objeto Enabled Command. Microsoft Agent está en desuso a partir Windows 7.
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3d8b77833da20c4a0b4254d4ce3432ff20d2f9b18a1da877adc9664bbff6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726065"
---
# <a name="enabled-property-command-object"></a>Propiedad Enabled (objeto Command)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece si el **comando** está habilitado en el menú emergente del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands("_*_name_*_"). Booleano_ *  \[  =  *habilitado*\]



| Parte      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que especifica si el **comando** está habilitado.<br/> <dl> <dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Verdadero**</dt> <dd> El **comando** está habilitado.<br/> </dd> <dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Falso**</dt> <dd> El **comando** está deshabilitado.<br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si la [**propiedad Enabled**](enabled-property.md) está establecida en **True**, el título de los objetos [**Command**](/windows/desktop/lwef/the-command-object) aparece como texto normal en el menú emergente del carácter cuando la aplicación cliente está activa en la entrada. Si la **propiedad Enabled** es **False,** el título aparece como texto no disponible (deshabilitado). Tampoco se **puede acceder a** un comando deshabilitado para la entrada de voz.

 

