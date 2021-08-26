---
title: IAgentSpeechInputProperties GetListeningTip
description: IAgentSpeechInputProperties GetListeningTip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0199e75ad56cee2c299ce53be3aa94376104af5ead40004e8dbbd8fd4dcfec9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014185"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a>IAgentSpeechInputProperties::GetListeningTip

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

Recupera un valor que indica si la sugerencia de escucha está habilitada para mostrarse.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*
</dt> <dd>

Dirección de una variable que recibe **True si** la sugerencia de escucha está habilitada para mostrarse, o **False** si la sugerencia de escucha está deshabilitada.

</dd> </dl>

Si [**GetEnabled**](iagentspeechinputproperties--getenabled.md) devuelve **False**, al consultar cualquier otra propiedad de entrada de voz se devuelve un error.

## <a name="see-also"></a>Consulte también

[**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




