---
title: Propiedad HelpContextID (objeto de colección Commands)
description: Obtenga información sobre la propiedad HelpContextID del objeto Commands Collection. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ed6ccf40545e15b3603ce5abe80ef94ff4272a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068241"
---
# <a name="helpcontextid-property-commands-collection-object"></a>Propiedad HelpContextID (objeto de colección Commands)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece un número de contexto asociado para el [**objeto Commands.**](/windows/desktop/lwef/the-commands-collection-object) Se usa para proporcionar ayuda contextual para el **objeto Commands.**

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Caracteres("**_CharacterID_*_"). Commands("_*_name_*_"). HelpContextID_ *  \[  =  *Number*\]



| Parte     | Descripción                                   |
|----------|-----------------------------------------------|
| *Number* | Entero que especifica un número de contexto válido. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si ha creado un archivo de Ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, el Agente llama automáticamente a help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **True** y el usuario selecciona el objeto [**Commands.**](/windows/desktop/lwef/the-commands-collection-object) Si establece un número de contexto en **HelpContextID,** el Agente llama a la Ayuda y busca el tema identificado por ese número de contexto.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> La compilación de un archivo de Ayuda requiere el compilador de Ayuda de Microsoft Windows.

 

## <a name="see-also"></a>Consulte también

[**HelpFile, propiedad**](helpfile-property.md)


 

 
