---
title: IAgentSpeechInputProperties GetHotKey
description: IAgentSpeechInputProperties GetHotKey
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e672b26f97cfbe92bc71d0ceab165e100c3ecf92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104074987"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a>IAgentSpeechInputProperties::GetHotKey

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

Recupera la asignación de teclado actual para la clave de escucha de entrada de voz.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*
</dt> <dd>

Dirección de un BSTR que recibe la configuración de Hotkey actual usada para abrir el canal de audio para la entrada de voz.

</dd> </dl>

Si [**GetEnabled**](iagentspeechinputproperties--getenabled.md) devuelve **false**, al consultar esta configuración se produce un error.

## <a name="see-also"></a>Consulte también

[**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




