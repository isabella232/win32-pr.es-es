---
title: Propiedad HelpFile
description: Propiedad HelpFile
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0167034b064e8a6e7540dd22ff0b8185a8f96e82decf504aae4f4994b70d6694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478619"
---
# <a name="helpfile-property"></a>Propiedad HelpFile

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece la ruta de acceso y el nombre de archivo de un archivo Windows de Ayuda contextual proporcionado por la aplicación cliente.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Nombre de archivo del archivo de_ *  \[  =  *ayuda*\]



| Parte       | Descripción                                                                    |
|------------|--------------------------------------------------------------------------------|
| *Nombre de archivo* | Expresión de cadena que especifica la ruta de acceso y el nombre de archivo del Windows ayuda. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si ha creado un archivo de Ayuda de Windows para la aplicación y ha establecido la propiedad **HelpFile** del carácter, el Agente llama automáticamente a la Ayuda cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **True** y el usuario hace clic en el carácter o selecciona un comando en su menú emergente. Si especificó un número de contexto en la propiedad [**HelpContextID**](helpcontextid-property.md) del comando seleccionado, la Ayuda muestra un tema correspondiente al contexto de ayuda actual; de lo contrario, muestra "Sin tema de Ayuda asociado a este elemento".

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**Propiedad HelpModeOn**](helpmodeon-property.md), [ **propiedad HelpContextID**](helpcontextid-property.md)


 

 




