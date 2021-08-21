---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f9f888fcea9069ff31ccef6b2c1ef5a0148fbb34ba21d03ee881c52056f10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105543"
---
# <a name="iagentcharacterexgetsrstatus"></a>IAgentCharacterEx::GetSRStatus

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

Recupera el estado de la condición necesaria para admitir la entrada de voz.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Dirección de una variable que recibe uno de los siguientes valores para la configuración de estado:



| Valor                                                                               | Descripción                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const unsigned long** **LISTEN STATUS \_ \_ CANLISTEN = 0;**<br/>               | Las condiciones admiten la entrada de voz.                                                                                                                                                                                                          |
| **const unsigned long** **LISTEN STATUS \_ \_ NOAUDIO = 1;**<br/>                 | No hay ningún dispositivo de entrada de audio disponible en este sistema. (Tenga en cuenta que esto no detecta si un micrófono está instalado; solo puede detectar si el usuario tiene una tarjeta de sonido habilitada para entrada correctamente instalada con un controlador de trabajo). |
| **const unsigned long** **LISTEN STATUS \_ \_ NOTTOPMOST = 2;**<br/>              | Otro cliente es el cliente activo de este carácter o el carácter actual no está en la parte superior.                                                                                                                                           |
| **const unsigned long** **LISTEN STATUS \_ \_ ¡y¡3;**<br/>           | El canal de entrada o salida de audio está ocupado actualmente, otra aplicación usa audio.                                                                                                                                               |
| **const unsigned long** **LISTEN STATUS \_ \_ COULDNZONETIALIZESPEECH = 4;**<br/> | Se produjo un error no especificado en el proceso de inicialización del subsistema de reconocimiento de voz. Esto incluye la posibilidad de que no haya ningún motor de voz disponible que coincida con la configuración de idioma del carácter.                          |
| **const unsigned long** **LISTEN STATUS \_ \_ SPEECHDISABLED = 5;**<br/>          | El usuario ha deshabilitado la entrada de voz en la ventana Opciones avanzadas de caracteres.                                                                                                                                                              |
| **const unsigned long** **LISTEN STATUS ERROR = \_ \_ 6;**<br/>                   | Se produjo un error al comprobar el estado del audio, pero el sistema no devolvió la causa del error.                                                                                                                                |



 

</dd> </dl>

Esta función permite consultar si las condiciones actuales admiten la entrada de reconocimiento de voz, incluido el estado del dispositivo de audio. Si la aplicación usa [**el método IAgentCharacterEx::Listen,**](iagentcharacterex--listen.md) puede usar esta función para asegurarse de que la llamada se realizará correctamente. Al llamar a este método también se carga el motor de voz si aún no está cargado. Sin embargo, no activa el modo de escucha.

Cuando la entrada de voz está habilitada en la hoja de propiedades del Agente (Opciones avanzadas de caracteres), al consultar el estado se cargará el motor asociado (si aún no está cargado) y se iniciarán los servicios de voz. Es decir, la clave de escucha está disponible y se puede mostrar la sugerencia de escucha. (La clave de escucha y la sugerencia de escucha solo se habilitan si también están habilitadas en Opciones avanzadas de caracteres). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia los servicios de voz.

Esta función devuelve solo la configuración para el uso del carácter por parte de la aplicación cliente; la configuración no refleja otros clientes del carácter u otros caracteres de la aplicación cliente.

 

 





