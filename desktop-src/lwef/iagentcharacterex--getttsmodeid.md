---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104077393"
---
# <a name="iagentcharacterexgetttsmodeid"></a>IAgentCharacterEx::GetTTSModeID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

Recupera el identificador de modo del conjunto de motores TTS para el carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Dirección de un BSTR que recibe la configuración de ID. de modo del motor TTS para el carácter.

</dd> </dl>

Esta configuración devuelve el identificador del modo de motor de TTS (texto a voz) de la salida hablada de un carácter. El identificador de modo de un motor TTS es una representación de cadena del GUID (con formato con llaves y guiones) definida por el proveedor de voz que identifica de forma única al motor. Para obtener más información, consulte la [documentación del SDK de Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx). Si se consulta esta propiedad, se cargará el motor asociado si aún no está cargado.

Si no establece un identificador de modo de motor TTS para el carácter, el servidor intenta devolver un motor que coincide con (mediante interfaces de Microsoft Speech API) la configuración de TTS compilada del carácter y la configuración de idioma actual del carácter. Si son diferentes, la configuración de idioma del carácter invalida la configuración de modo creado. Si no ha establecido la configuración de idioma del carácter, el idioma del carácter es el ID. de idioma predeterminado del usuario y el servidor intenta la coincidencia en función de ese identificador de idioma.

Esta función no genera un error si [**IAgentAudioObjectProperties:: GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) devuelve **false**.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los requisitos del motor de voz de Microsoft Agent se basan en Microsoft Speech API. Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el agente.

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::SetTTSModeID**](iagentcharacterex--setttsmodeid.md)


 

 




