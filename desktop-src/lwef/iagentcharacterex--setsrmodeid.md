---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252591"
---
# <a name="iagentcharacterexsetsrmodeid"></a>IAgentCharacterEx::SetSRModeID

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

Establece el identificador de modo del motor de reconocimiento de voz establecido para el carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

bszModeID

La configuración del identificador de modo del motor de reconocimiento de voz para el carácter.

Esta configuración establece el motor para la entrada de voz de un carácter. El identificador de modo de un motor de reconocimiento de voz es el GUID definido por el proveedor de voz que identifica de forma única el modo del motor (con formato de llaves y guiones). Para más información, consulte la documentación [del SDK de Voz de Microsoft](https://msdn.microsoft.com/library/ee705648.aspx).

Si especifica un identificador de modo que no coincide con la configuración de idioma del carácter, si el usuario ha deshabilitado el reconocimiento de voz (en la hoja de propiedades de Microsoft Agent) o el motor no está instalado, se producirá un error en esta llamada. Si no establece un identificador de modo del motor de reconocimiento de voz para el carácter, el servidor establece uno que coincida con la configuración de idioma del carácter (mediante interfaces de Microsoft Speech API).

Cuando la entrada de voz está habilitada en la hoja de propiedades del Agente (Opciones avanzadas de caracteres), al establecer esta propiedad se cargará el motor asociado (si aún no está cargado) e iniciará los servicios de voz. Es decir, la clave de escucha está disponible y se puede mostrar la sugerencia de escucha. (La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en Opciones avanzadas de caracteres). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia los servicios de voz.

Esta propiedad solo se aplica al cliente del carácter; el valor no refleja la configuración para otros clientes del carácter u otros caracteres del cliente.

Los requisitos del motor de voz de Microsoft Agent se basan en los requisitos de Microsoft Speech API. Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el Agente .

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md)


 

 




