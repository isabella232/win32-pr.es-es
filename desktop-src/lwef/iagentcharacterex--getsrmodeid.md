---
title: IAgentCharacterEx GetSRModeID
description: IAgentCharacterEx GetSRModeID
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d43e09722aef8f39f802c6a4be037a2002cab564be535554b2450668faed90d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114765"
---
# <a name="iagentcharacterexgetsrmodeid"></a>IAgentCharacterEx::GetSRModeID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

Recupera el identificador de modo del motor de reconocimiento de voz establecido para el carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Dirección de un BSTR que recibe la configuración del identificador de modo del motor de reconocimiento de voz para el carácter.

</dd> </dl>

Esta configuración devuelve el motor establecido para la entrada de voz de un carácter. El identificador de modo de un motor de reconocimiento de voz es una representación de cadena del GUID (con formato de llaves y guiones) por parte del proveedor de voz que identifica de forma única el motor. Para más información, consulte la documentación [del SDK de Voz de Microsoft](https://msdn.microsoft.com/library/ee705648.aspx).

Si no establece un identificador de modo de motor de reconocimiento de voz para el carácter, el servidor devuelve un motor que coincide con la configuración de idioma del carácter (mediante interfaces de Microsoft Speech API). Si no hay ningún motor de reconocimiento de voz correspondiente disponible para el carácter, el servidor devuelve una cadena null (vacía).

Cuando la entrada de voz está habilitada (en la ventana Opciones avanzadas de caracteres), al consultar o establecer esta propiedad se cargará el motor asociado (si aún no está cargado) e iniciará los servicios de voz. Es decir, la clave de escucha está disponible y se puede mostrar la sugerencia de escucha. (La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en Opciones avanzadas de caracteres). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia los servicios de voz y devuelve una cadena nula (cadena vacía).

Esta función devuelve solo la configuración para el uso del carácter por parte de la aplicación cliente; la configuración no refleja otros clientes del carácter u otros caracteres de la aplicación cliente.

Esta función no da error si [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md) devuelve **False**.

Los requisitos del motor de voz de Microsoft Agent se basan en microsoft Speech API. Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el Agente .

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::SetSRModeID**](iagentcharacterex--setsrmodeid.md)


 

 




