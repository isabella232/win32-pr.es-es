---
title: IAgentCharacter SetIdleOn
description: IAgentCharacter SetIdleOn
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde86da6dda12744aedcd780b93d92c45fe2906dd16073bf0e3555848718e747
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665685"
---
# <a name="iagentcharactersetidleon"></a>IAgentCharacter::SetIdleOn

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

Establece el procesamiento de inactividad automático para un carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Bon*
</dt> <dd>

Marca de procesamiento inactiva. Si este parámetro es **True**, Microsoft Agent reproduce automáticamente animaciones de estado de **Idling.**

</dd> </dl>

El servidor establece automáticamente un tiempo de espera después de la última animación que se reproduce para un carácter. Cuando se completa el intervalo de este temporizador, el servidor comienza los estados de **idling** de un carácter, reproduciendo sus animaciones **de idling** asociadas a intervalos regulares. Si desea administrar las animaciones de estado **idling** usted mismo, establezca la propiedad en **False**. Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md)


 

 




