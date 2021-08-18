---
title: Propiedad HelpContextID (objeto Characters)
description: Obtenga información sobre la propiedad HelpContextID del objeto Characters. Microsoft Agent está en desuso a partir Windows 7.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c790f4e3b0e69f4c8dc5e032b0021067e908f4af6200432dae668d08b47e1f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478722"
---
# <a name="helpcontextid-property-characters-object"></a>Propiedad HelpContextID (objeto Characters)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece un número de contexto asociado para el carácter. Se usa para proporcionar ayuda contextual para el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). HelpContextID_ *  \[  =  *Number*\]



| Parte     | Descripción                                   |
|----------|-----------------------------------------------|
| *Number* | Entero que especifica un número de contexto válido. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para admitir la Ayuda contextual para el carácter, asigne el número de contexto al carácter que usa para el tema de Ayuda asociado al compilar el archivo de Ayuda. Esta propiedad solo se aplica al cliente del carácter; la configuración no afecta a otros clientes del carácter ni a otros caracteres del cliente.

Si ha creado un archivo de Ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, el Agente llama automáticamente a la Ayuda cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **True** y el usuario hace clic en el carácter. Si hay un número de contexto en [**HelpContextID,**](helpcontextid-property.md)el Agente llama a la Ayuda y busca el tema identificado por el número de contexto actual. El número de contexto actual es el valor **de HelpContextID** para el carácter.

> [!Note]  
> La compilación de un archivo de Ayuda requiere el compilador Windows Ayuda de Microsoft.

 

## <a name="see-also"></a>Consulte también

[**Propiedad HelpFile**](helpfile-property.md)


 

 




