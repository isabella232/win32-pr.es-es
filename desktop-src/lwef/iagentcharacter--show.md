---
title: IAgentCharacter Show
description: IAgentCharacter Show
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcefb523bd2e9f477991bf6fa8352382f75b6bc76d93aab2e7f5c9e8cc1358dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693007"
---
# <a name="iagentcharactershow"></a>IAgentCharacter::Show

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

Muestra un carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente. Cuando la función vuelve, *pdwReqID* contiene el identificador de la solicitud.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*
</dt> <dd>

Muestra la marca de animación de estado. Si este parámetro es **True**, la **animación de** estado Mostrando se reproduce después de hacer visible el carácter; si **es False**, la animación no se reproduce.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de solicitud [**Show.**](/windows/desktop/lwef/iagentcharacter--show)

</dd> </dl>

Evite establecer *el parámetro bFast* en **True** sin reproducir una animación de antemano; de lo contrario, se puede mostrar el marco de caracteres, pero no tener ninguna imagen para mostrar. En concreto, tenga en cuenta que si llama a [**MoveTo**](iagentcharacter--moveto.md) cuando el carácter no está visible, no reproducirá ninguna animación. Por lo tanto, si llama al **método Show** con *bFast* establecido en **True,** no se mostrará ninguna imagen. De forma similar, si llama a [**Ocultar**](/windows/desktop/lwef/iagentcharacter--hide), a continuación, **Mostrar** con *bFast* establecido en **True**, no habrá ninguna imagen visible.

Cuando use el protocolo HTTP para acceder a los datos de caracteres y animaciones, use el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantizar la disponibilidad de la animación de estado **Showing** antes de llamar a este método.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::Hide**](iagentcharacter--hide.md)


 

 