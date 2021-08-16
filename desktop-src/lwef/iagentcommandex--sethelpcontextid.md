---
title: IAgentCommandEx SetHelpContextID
description: IAgentCommandEx SetHelpContextID
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b876276d42ff07081b60194e90beff3ad9ef19fec383c50d70a551e1c9a5e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750219"
---
# <a name="iagentcommandexsethelpcontextid"></a>IAgentCommandEx::SetHelpContextID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

Establece [**helpContextID para**](helpcontextid-property-com.md) un [**objeto Command.**](/windows/desktop/lwef/the-command-object)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*
</dt> <dd>

Número de contexto del tema de ayuda asociado al [**objeto Command;**](/windows/desktop/lwef/the-command-object) se usa para proporcionar ayuda contextual para el comando.

</dd> </dl>

Si ha creado un archivo Windows ayuda para la aplicación y lo ha establecido en la propiedad [**HelpFile del**](helpfile-property.md) carácter. Microsoft Agent llama automáticamente a la Ayuda cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **True** y el usuario selecciona el comando. Si hay un número de contexto en [**HelpContextID,**](helpcontextid-property-com.md)el Agente llama a la Ayuda y busca el tema identificado por el número de contexto actual. El número de contexto actual es el valor de **HelpContextID** para el comando.

> [!Note]  
> La compilación de un archivo de Ayuda requiere microsoft Windows compilador de Ayuda.

 

## <a name="see-also"></a>Consulte también

[**IAgentCommandEx::GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 