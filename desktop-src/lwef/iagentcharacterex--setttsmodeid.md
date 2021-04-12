---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34392e65fcb8f3a46db6251f01f59ad76aba278d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420371"
---
# <a name="iagentcharacterexsetttsmodeid"></a>IAgentCharacterEx::SetTTSModeID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

Establece el identificador de modo del conjunto de motores TTS para el carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*
</dt> <dd>

La configuración del identificador de modo del motor TTS para el carácter.

> [!Note]  
> **IAgentCharacterEx: SetTTSModeID** puede producir un error si Speech.dll no está instalado y el motor especificado no coincide con la configuración de modo TTS compilado del carácter.

 

</dd> </dl>

Esta configuración determina el modo de motor preferido para la salida de voz oral de un carácter. El identificador de modo de un motor de conversión de texto a voz es el GUID definido por el proveedor de voz que identifica de forma única el modo del motor (con formato de llaves y guiones). Para obtener más información, consulte la [documentación del SDK de Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).

Si establece un identificador de modo TTS, invalida el intento del servidor de hacer coincidir un motor de voz basado en el identificador del modo TTS compilado del carácter, el ID. de idioma actual del sistema y el ID. de idioma actual del carácter. Sin embargo, si intenta establecer un identificador de modo cuando el usuario ha deshabilitado la salida de voz en la hoja de propiedades del agente de Microsoft o cuando el motor asociado no está instalado, se producirá un error en esta llamada.

Si no establece un identificador de modo de motor TTS para el carácter, el servidor establece un motor que coincide con la configuración de idioma del carácter (mediante interfaces de Microsoft Speech API). Al establecer esta propiedad, se cargará el motor asociado si aún no está cargado.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los requisitos del motor de voz de Microsoft Agent se basan en Microsoft Speech API. Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el agente.

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx:GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




