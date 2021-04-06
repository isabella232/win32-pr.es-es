---
title: IAgentCharacter Mostrar
description: IAgentCharacter Mostrar
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997a9879d564644085bd92e4515460c3dde33208
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077755"
---
# <a name="iagentcharactershow"></a>IAgentCharacter:: show

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

Muestra un carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente. Cuando la función devuelve, *pdwReqID* contiene el identificador de la solicitud.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*
</dt> <dd>

Marca de animación de estado que se muestra. Si este parámetro es **true**, la animación de estado **que** se reproduce después de que el carácter esté visible; Si **es false**, la animación no se reproduce.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de solicitud de [**presentación**](/windows/desktop/lwef/iagentcharacter--show) .

</dd> </dl>

Evite establecer el parámetro *bFast* en **true** sin reproducir una animación de antemano; de lo contrario, se puede mostrar el marco de caracteres, pero no tiene ninguna imagen para mostrar. En concreto, tenga en cuenta que si llama a [**moveTo**](iagentcharacter--moveto.md) cuando el carácter no está visible, no se reproduce ninguna animación. Por lo tanto, si llama al método **Show** con *BFAST* establecido en **true**, no se mostrará ninguna imagen. Del mismo modo, si llama a [**Hide**](/windows/desktop/lwef/iagentcharacter--hide), **Show** with *bFast* establecido en **true**, no habrá ninguna imagen visible.

Al usar el protocolo HTTP para tener acceso a los datos de animación y de caracteres, utilice el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantizar la disponibilidad de la animación de estado **que se muestra** antes de llamar a este método.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: Hide**](iagentcharacter--hide.md)


 

 