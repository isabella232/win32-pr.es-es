---
title: HelpFile (propiedad)
description: HelpFile (propiedad)
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776458"
---
# <a name="helpfile-property"></a>HelpFile (propiedad)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece la ruta de acceso y el nombre de archivo de un archivo de ayuda contextual de Microsoft Windows proporcionado por la aplicación cliente.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente. ***Caracteres ("*** CharacterID * *").* *  \[  =  *Nombre de archivo* de HelpFile\]



| Parte       | Descripción                                                                    |
|------------|--------------------------------------------------------------------------------|
| *Nombre de archivo* | Expresión de cadena que especifica la ruta de acceso y el nombre del archivo de ayuda de Windows. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si ha creado un archivo de ayuda de Windows para la aplicación y ha establecido la propiedad **HelpFile** del carácter, el agente llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario hace clic en el carácter o selecciona un comando en el menú emergente. Si especificó un número de contexto en la propiedad [**IDDelContextoDeAyuda**](helpcontextid-property.md) del comando seleccionado, la ayuda de muestra un tema correspondiente al contexto de ayuda actual. en caso contrario, se muestra "no hay ningún tema de ayuda asociado a este elemento".

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**Propiedad HelpModeOn**](helpmodeon-property.md), [ **propiedad HelpContextID**](helpcontextid-property.md)


 

 




