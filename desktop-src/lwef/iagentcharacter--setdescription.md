---
title: IAgentCharacter SetDescription
description: IAgentCharacter SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d96765d3faddafef00a28826ec5a9fdd92acb6884ac3aa659ad88ba2c091a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609825"
---
# <a name="iagentcharactersetdescription"></a>IAgentCharacter::SetDescription

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

Establece la descripción del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*
</dt> <dd>

BSTR que establece la descripción del carácter. La descripción predeterminada de un carácter se define cuando se compila con el Editor de caracteres de Microsoft Agent. La configuración de descripción es opcional y no se puede proporcionar para todos los caracteres. Puede cambiar la descripción del carácter **mediante IAgentCharacter::setDescription**; sin embargo, este valor no es persistente (se almacena permanentemente). La descripción del carácter vuelve a su configuración predeterminada cada vez que un cliente carga por primera vez el carácter.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::GetDescription**](iagentcharacter--getdescription.md)


 

 




