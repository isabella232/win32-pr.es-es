---
title: IAgentSpeechInputProperties GetListeningTip
description: IAgentSpeechInputProperties GetListeningTip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91218fb7935edb68458d540a8f35fe5402b317ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704563"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a>IAgentSpeechInputProperties::GetListeningTip

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

Recupera un valor que indica si la sugerencia de escucha está habilitada para la presentación.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*
</dt> <dd>

Dirección de una variable que recibe **true** si la sugerencia de escucha está habilitada para la presentación o **false** si la sugerencia de escucha está deshabilitada.

</dd> </dl>

Si [**GetEnabled**](iagentspeechinputproperties--getenabled.md) devuelve **false**, la consulta de otras propiedades de entrada de voz devuelve un error.

## <a name="see-also"></a>Consulte también

[**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




