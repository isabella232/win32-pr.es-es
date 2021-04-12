---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104487291"
---
# <a name="iagentcharacterexsetsrmodeid"></a>IAgentCharacterEx::SetSRModeID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

Establece el identificador de modo del conjunto de motores de reconocimiento de voz para el carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

bszModeID

La configuración del identificador de modo del motor de reconocimiento de voz para el carácter.

Esta configuración establece el motor para la entrada de voz de un carácter. El identificador de modo de un motor de reconocimiento de voz es el GUID definido por el proveedor de voz que identifica de forma única el modo del motor (con formato de llaves y guiones). Para obtener más información, consulte la [documentación del SDK de Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).

Si especifica un identificador de modo que no coincide con la configuración de idioma del carácter, si el usuario ha deshabilitado el reconocimiento de voz (en la hoja de propiedades del agente de Microsoft) o si el motor no está instalado, se producirá un error en esta llamada. Si no establece un identificador de modo de motor de reconocimiento de voz para el carácter, el servidor establece uno que coincida con la configuración de idioma del carácter (mediante interfaces de Microsoft Speech API).

Cuando la entrada de voz está habilitada en la hoja de propiedades del agente (opciones avanzadas de caracteres), al establecer esta propiedad se cargará el motor asociado (si aún no está cargado) e iniciará servicios de voz. Es decir, la clave de escucha está disponible y la sugerencia de escucha es visible. (La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en opciones de caracteres avanzadas). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia Speech Services.

Esta propiedad solo se aplica al cliente del carácter; la configuración no refleja la configuración de otros clientes del carácter u otros caracteres del cliente.

Los requisitos del motor de voz de Microsoft Agent se basan en Microsoft Speech API. Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el agente.

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md)


 

 




