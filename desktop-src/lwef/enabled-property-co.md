---
title: Propiedad Enabled (objeto Command)
description: Obtenga información sobre la propiedad de objeto Enabled Command. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc0c65d5cfa0438fe9d61eac0c59e916731e057
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407338"
---
# <a name="enabled-property-command-object"></a>Propiedad Enabled (objeto Command)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

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
| *boolean* | Expresión booleana que especifica si el **comando** está habilitado.<br/> <dl> <dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Verdad**</dt> <dd> El **comando** está habilitado.<br/> </dd> <dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Falso**</dt> <dd> El **comando** está deshabilitado.<br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si la [**propiedad Enabled**](enabled-property.md) está establecida en **True**, el título de los objetos [**Command**](/windows/desktop/lwef/the-command-object) aparece como texto normal en el menú emergente del carácter cuando la aplicación cliente está activa en la entrada. Si la **propiedad Enabled** es **False**, el título aparece como texto no disponible (deshabilitado). Tampoco se **puede acceder a** un comando deshabilitado para la entrada de voz.

 

