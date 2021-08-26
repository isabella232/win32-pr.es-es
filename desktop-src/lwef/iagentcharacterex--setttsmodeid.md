---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a24195fd177abbde3c6423f966df67ba0faeaf315038d7f8cb0b4ca136f16c3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114725"
---
# <a name="iagentcharacterexsetttsmodeid"></a>IAgentCharacterEx::SetTTSModeID

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

Establece el identificador de modo del motor de TTS establecido para el carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*
</dt> <dd>

La configuración del identificador de modo del motor de TTS para el carácter.

> [!Note]  
> **IAgentCharacterEx:SetTTSModeID** puede producir un error si Speech.dll no está instalado y el motor que especifique no coincide con la configuración del modo TTS compilado del carácter.

 

</dd> </dl>

Esta configuración determina el modo de motor preferido para la salida TTS hablada de un carácter. El identificador de modo de un motor de TTS (texto a voz) es el GUID definido por el proveedor de voz que identifica de forma única el modo del motor (con formato de llaves y guiones). Para obtener más información, consulte la [documentación del SDK de Voz de Microsoft](https://msdn.microsoft.com/library/ee705648.aspx).

Si establece un identificador de modo TTS, invalida el intento del servidor de hacer coincidir un motor de voz en función del identificador de modo TTS compilado del carácter, el identificador de idioma del sistema actual y el identificador de idioma actual del carácter. Sin embargo, si intenta establecer un identificador de modo cuando el usuario ha deshabilitado la salida de voz en la hoja de propiedades de Microsoft Agent o cuando el motor asociado no está instalado, se producirá un error en esta llamada.

Si no establece un identificador de modo de motor TTS para el carácter, el servidor establece un motor que coincide con la configuración de idioma del carácter (mediante las interfaces de Speech API Microsoft). Si establece esta propiedad, se cargará el motor asociado si aún no está cargado.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los requisitos del motor de voz de Microsoft Agent se basan en microsoft Speech API. Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el Agente .

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx:GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




