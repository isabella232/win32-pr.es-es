---
title: IAgentCharacter SetDescription
description: IAgentCharacter SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419199"
---
# <a name="iagentcharactersetdescription"></a>IAgentCharacter:: SetDescription

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

Establece la descripción del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*
</dt> <dd>

BSTR que establece la descripción del carácter. La descripción predeterminada de un carácter se define cuando se compila con el editor de caracteres del agente de Microsoft. La configuración de la descripción es opcional y es posible que no se proporcione para todos los caracteres. Puede cambiar la descripción del carácter mediante **IAgentCharacter:: setDescription**; sin embargo, este valor no es persistente (se almacena de forma permanente). La descripción del carácter vuelve a su configuración predeterminada siempre que un cliente carga el carácter por primera vez.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: GetDescription**](iagentcharacter--getdescription.md)


 

 




