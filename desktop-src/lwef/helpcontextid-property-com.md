---
title: Propiedad HelpContextID (objeto Command)
description: Obtenga información sobre la propiedad HelpContextID del objeto Command. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c3c0ff5a6722dd6740c7df7e89bf2b9520053
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068521"
---
# <a name="helpcontextid-property-command-object"></a>Propiedad HelpContextID (objeto Command)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece un número de contexto asociado para el [**objeto Command.**](/windows/desktop/lwef/the-command-object) Se usa para proporcionar ayuda contextual para el **objeto Command.**

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Caracteres("**_CharacterID_*_"). Commands(""). HelpContextID_ *  \[  =  *Number*\]



| Parte     | Descripción                                   |
|----------|-----------------------------------------------|
| *Number* | Entero que especifica un número de contexto válido. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si ha creado un archivo de Ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter en el archivo, el Agente llama automáticamente a help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **True** y el usuario selecciona el comando. Si establece un número de contexto en [**HelpContextID,**](helpcontextid-property.md)el Agente llama a la Ayuda y busca el tema identificado por el número de contexto actual. El número de contexto actual es el valor de **HelpContextID** para el comando.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> La compilación de un archivo de Ayuda requiere el compilador de Ayuda de Microsoft Windows.

 

## <a name="see-also"></a>Consulte también

[**HelpFile, propiedad**](helpfile-property.md)


 

 
