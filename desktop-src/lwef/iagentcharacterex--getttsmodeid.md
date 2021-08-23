---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e6bc029a6fce1da3d6f920a25ccc86c49619751a6bd43f865154bd7a235696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105493"
---
# <a name="iagentcharacterexgetttsmodeid"></a>IAgentCharacterEx::GetTTSModeID

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

Recupera el identificador de modo del motor de TTS establecido para el carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Dirección de un BSTR que recibe la configuración del identificador de modo del motor de TTS para el carácter.

</dd> </dl>

Esta configuración devuelve el identificador de modo del motor TTS (texto a voz) para la salida hablada de un carácter. El identificador de modo de un motor de TTS es una representación de cadena del GUID (con formato de llaves y guiones) definido por el proveedor de voz que identifica de forma única el motor. Para más información, consulte la documentación [del SDK de Voz de Microsoft](https://msdn.microsoft.com/library/ee705648.aspx). Al consultar esta propiedad, se cargará el motor asociado si aún no está cargado.

Si no establece un identificador de modo de motor TTS para el carácter, el servidor intenta devolver un motor que coincida (mediante interfaces de Microsoft Speech API) la configuración TTS compilada del carácter y la configuración de idioma actual del carácter. Si son diferentes, la configuración de idioma del carácter invalida su configuración de modo de creación. Si no ha establecido la configuración de idioma del carácter, el idioma del carácter es el identificador de idioma predeterminado del usuario y el servidor intenta la coincidencia en función de ese identificador de idioma.

Esta función no da error si [**IAgentAudioObjectProperties::GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) devuelve **False**.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los requisitos del motor de voz de Microsoft Agent se basan en microsoft Speech API. Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el Agente .

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::SetTTSModeID**](iagentcharacterex--setttsmodeid.md)


 

 




