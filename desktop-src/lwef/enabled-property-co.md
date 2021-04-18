---
title: Propiedad Enabled (objeto Command)
description: Propiedad Enabled
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5999e396f61fbcc820bc1cec7deb0c603eb948e4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695825"
---
# <a name="enabled-property-command-object"></a>Propiedad Enabled (objeto Command)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece si el **comando** está habilitado en el menú emergente del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_"). Comandos ("_*_Name_*_"). Booleano habilitado_ *  \[  =  \]



| Parte      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Una expresión booleana que especifica si el **comando** está habilitado.<br/> <dl> <dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt> <dd> El **comando** está habilitado.<br/> </dd> <dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt> <dd> El **comando** está deshabilitado.<br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si la propiedad [**Enabled**](enabled-property.md) está establecida en **true**, el título de los objetos de [**comando**](/windows/desktop/lwef/the-command-object) aparece como texto normal en el menú emergente del carácter cuando la aplicación cliente es de entrada-activa. Si la propiedad **Enabled** es **false**, el título aparece como texto no disponible (deshabilitado). Tampoco se puede obtener acceso a un **comando** deshabilitado para la entrada de voz.

 

