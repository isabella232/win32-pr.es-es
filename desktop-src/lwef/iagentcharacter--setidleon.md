---
title: IAgentCharacter SetIdleOn
description: IAgentCharacter SetIdleOn
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98db30c9c440ed0564b98977d33e15e390cf57d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419198"
---
# <a name="iagentcharactersetidleon"></a>IAgentCharacter::SetIdleOn

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

Establece el procesamiento de inactividad automático para un carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Despedida*
</dt> <dd>

Marca de procesamiento inactivo. Si este parámetro es **true**, el agente de Microsoft reproduce automáticamente las animaciones de estado de **ralentí** .

</dd> </dl>

El servidor establece automáticamente un tiempo de espera después de la última animación reproducida para un carácter. Una vez completado el intervalo de este temporizador, el servidor inicia los Estados de **ralentí** para un carácter, reproduciendo sus animaciones de inactiva **asociadas a intervalos** regulares. Si desea administrar las animaciones de estado de **ralentí** , establezca la propiedad en **false**. Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md)


 

 




