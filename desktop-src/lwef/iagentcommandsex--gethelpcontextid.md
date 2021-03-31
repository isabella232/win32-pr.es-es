---
title: IAgentCommandsEx GetHelpContextID
description: IAgentCommandsEx GetHelpContextID
ms.assetid: db5f93e9-8cd3-4147-94b4-50cfe12033c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a49a633a66622626973e450b9566033b1ad96e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077670"
---
# <a name="iagentcommandsexgethelpcontextid"></a>IAgentCommandsEx::GetHelpContextID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of Commands object help topic ID
);
```

Recupera [**HelpContextID**](helpcontextid-property.md) para un objeto [**Command**](/windows/desktop/lwef/the-command-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*
</dt> <dd>

Dirección de una variable que recibe el número de contexto del tema de ayuda para el objeto de [**comando**](/windows/desktop/lwef/the-command-object) .

</dd> </dl>

Si ha creado un archivo de ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, Microsoft Agent llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario selecciona el objeto de [**comando**](/windows/desktop/lwef/the-command-object) . Si hay un número de contexto en el [**HelpContextID**](helpcontextid-property.md), el agente llama a help y busca el tema identificado por el número de contexto actual. El número de contexto actual es el valor de **HelpContextID** para el objeto de **comando** .

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.

 

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 