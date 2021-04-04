---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4396e325f5afba161046f2a001cebb29033d709b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075536"
---
# <a name="iagentcharacterexgetsrstatus"></a>IAgentCharacterEx::GetSRStatus

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

Recupera el estado de la condición necesaria para admitir la entrada de voz.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Dirección de una variable que recibe uno de los siguientes valores para la configuración de estado:



| Value                                                                               | Descripción                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const unsigned Long** **Listen \_ status \_ CANLISTEN = 0;**<br/>               | Las condiciones admiten la entrada de voz.                                                                                                                                                                                                          |
| **const unsigned Long** **Listen \_ status \_ = 1;**<br/>                 | No hay ningún dispositivo de entrada de audio disponible en este sistema. (Tenga en cuenta que esto no detecta si hay un micrófono instalado; solo puede detectar si el usuario tiene una tarjeta de sonido habilitada para la entrada instalada correctamente con un controlador de trabajo). |
| **const unsigned Long** **Listen \_ status \_ NOTTOPMOST = 2;**<br/>              | Otro cliente es el cliente activo de este carácter o el carácter actual no es el nivel superior.                                                                                                                                           |
| **const unsigned Long** **Listen \_ status \_ CANTOPENAUDIO = 3;**<br/>           | El canal de entrada o salida de audio está ocupado actualmente, otra aplicación está usando audio.                                                                                                                                               |
| **const unsigned Long** **Listen \_ status \_ COULDNTINITIALIZESPEECH = 4;**<br/> | Se produjo un error no especificado en el proceso de inicialización del subsistema de reconocimiento de voz. Esto incluye la posibilidad de que no haya ningún motor de voz disponible que coincida con la configuración de idioma del carácter.                          |
| **const unsigned Long** **Listen \_ status \_ SPEECHDISABLED = 5;**<br/>          | El usuario ha deshabilitado la entrada de voz en la ventana Opciones de carácter avanzadas.                                                                                                                                                              |
| **const unsigned Long** **Listen \_ error status \_ = 6;**<br/>                   | Error al comprobar el estado de audio, pero el sistema no ha devuelto la causa del error.                                                                                                                                |



 

</dd> </dl>

Esta función permite consultar si las condiciones actuales admiten la entrada del reconocimiento de voz, incluido el estado del dispositivo de audio. Si su aplicación usa el método [**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md) , puede usar esta función para asegurarse de que la llamada se realizará correctamente. La llamada a este método también carga el motor de voz si aún no está cargado. Sin embargo, no activa el modo de escucha.

Cuando se habilita la entrada de voz en la hoja de propiedades del agente (opciones de caracteres avanzadas), al consultar el estado se cargará el motor asociado (si aún no está cargado) e iniciará servicios de voz. Es decir, la clave de escucha está disponible y la sugerencia de escucha es visible. (La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en opciones de caracteres avanzadas). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia Speech Services.

Esta función solo devuelve el valor del uso de la aplicación cliente del carácter; la configuración no refleja otros clientes del carácter u otros caracteres de la aplicación cliente.

 

 





