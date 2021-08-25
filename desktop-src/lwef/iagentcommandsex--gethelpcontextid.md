---
title: IAgentCommandsEx GetHelpContextID
description: IAgentCommandsEx GetHelpContextID
ms.assetid: db5f93e9-8cd3-4147-94b4-50cfe12033c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e15088eae1025daf7c98695dcf7fd610a04c30089028af0887107228de84b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961835"
---
# <a name="iagentcommandsexgethelpcontextid"></a>IAgentCommandsEx::GetHelpContextID

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of Commands object help topic ID
);
```

Recupera [**helpContextID para**](helpcontextid-property.md) un [**objeto Command.**](/windows/desktop/lwef/the-command-object)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*
</dt> <dd>

Dirección de una variable que recibe el número de contexto del tema de ayuda para el [**objeto Command.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Si ha creado un archivo de Ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, Microsoft Agent llama automáticamente a la Ayuda cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **True** y el usuario selecciona el objeto [**Command.**](/windows/desktop/lwef/the-command-object) Si hay un número de contexto en [**HelpContextID,**](helpcontextid-property.md)el Agente llama a la Ayuda y busca el tema identificado por el número de contexto actual. El número de contexto actual es el valor de **HelpContextID** para el **objeto Command.**

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> La compilación de un archivo de Ayuda requiere el compilador Windows Ayuda de Microsoft.

 

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 