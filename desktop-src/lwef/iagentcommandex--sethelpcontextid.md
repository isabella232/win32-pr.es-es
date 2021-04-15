---
title: IAgentCommandEx SetHelpContextID
description: IAgentCommandEx SetHelpContextID
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7539cef8e986db40ef94a8fd3d47073fbe489d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105695602"
---
# <a name="iagentcommandexsethelpcontextid"></a>IAgentCommandEx::SetHelpContextID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

Establece [**HelpContextID**](helpcontextid-property-com.md) para un objeto [**Command**](/windows/desktop/lwef/the-command-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*
</dt> <dd>

El número de contexto del tema de ayuda asociado al objeto de [**comando**](/windows/desktop/lwef/the-command-object) ; se utiliza para proporcionar ayuda contextual para el comando.

</dd> </dl>

Si ha creado un archivo de ayuda de Windows para la aplicación y lo ha establecido en la propiedad [**HelpFile**](helpfile-property.md) del carácter. El agente de Microsoft llama automáticamente a la ayuda cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario selecciona el comando. Si hay un número de contexto en el [**HelpContextID**](helpcontextid-property-com.md), el agente llama a help y busca el tema identificado por el número de contexto actual. El número de contexto actual es el valor de **HelpContextID** para el comando.

> [!Note]  
> La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.

 

## <a name="see-also"></a>Consulte también

[**IAgentCommandEx:: GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 