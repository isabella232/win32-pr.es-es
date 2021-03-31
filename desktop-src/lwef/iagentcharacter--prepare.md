---
title: Preparación de IAgentCharacter
description: Preparación de IAgentCharacter
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebee8d2ea99c8782e9506e0e4a812cfb277487
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077718"
---
# <a name="iagentcharacterprepare"></a>IAgentCharacter::P redondear

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

Recupera los datos de animación de un carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente. Cuando la función devuelve, *pdwReqID* contiene el identificador de la solicitud.

<dl> <dt>

<span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*
</dt> <dd>

Valor que indica el tipo de datos de animación que se va a cargar y que debe ser uno de los siguientes:



| Value                                                           | Descripción                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| **const sin signo Short** **Prepárese \_ Animation = 0;**<br/> | Datos de animación de un carácter.                              |
| **const unsigned short** ( **Estado de preparación) \_ = 1;**<br/>     | Datos de estado de un carácter.                                  |
| **const unsigned short** ( **preparación) \_ Wave = 2**<br/>       | Archivo de sonido de un carácter (. WAV o. LWV) para la salida de voz. |



 

</dd> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

El nombre de la animación o el estado.

El nombre de la animación se basa en el definido para el carácter cuando se guardó con el editor de caracteres del agente de Microsoft.

En el caso de los Estados, el valor puede ser uno de los siguientes:



|                      |                                                 |
|----------------------|-------------------------------------------------|
| **"Gesturing"**      | Para recuperar todas las animaciones de estado de **gesturing** . |
| **"GesturingDown"**  | Para recuperar animaciones **GesturingDown** .       |
| **"GesturingLeft"**  | Para recuperar animaciones **GesturingLeft** .       |
| **"GesturingRight"** | Para recuperar animaciones **GesturingRight** .      |
| **"GesturingUp"**    | Para recuperar animaciones **GesturingUp** .         |
| **Conde**         | Para recuperar las animaciones de estado **ocultas** .    |
| **Oye**        | Para recuperar las animaciones del estado de la **audición** .   |
| **Inactivo**         | Para recuperar todas las animaciones de estado de **ralentí** .    |
| **"IdlingLevel1"**   | Para recuperar todas las animaciones **IdlingLevel1** .    |
| **"IdlingLevel2"**   | Para recuperar todas las animaciones **IdlingLevel2** .    |
| **"IdlingLevel3"**   | Para recuperar todas las animaciones **IdlingLevel3** .    |
| **Escucha**      | Para recuperar las animaciones de estado de **escucha** . |
| **Moverlo**         | Para recuperar todas las animaciones de estado en **movimiento** .    |
| **"MovingDown"**     | Para recuperar todas las animaciones en **movimiento** .          |
| **"MovingLeft"**     | Para recuperar todas las animaciones **MovingLeft** .      |
| **"MovingRight"**    | Para recuperar todas las animaciones **MovingRight** .     |
| **"MovingUp"**       | Para recuperar todas las animaciones **MovingUp** .        |
| **Mostrar**        | Para recuperar las animaciones de estado **que se muestran** .   |
| **Habla**       | Para recuperar las animaciones de estado de **habla** .  |



 

Para. Archivos WAV, establezca *bszName* en la dirección URL o especificación de archivo para. Archivo WAV. Si la especificación no está completa, se interpreta como relativa a la especificación utilizada en el método [**Load**](https://www.bing.com/search?q=**Load**) .

</dd> <dt>

<span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*
</dt> <dd>

Un valor booleano que especifica si el servidor pone en cola la solicitud de [**preparación**](/windows/desktop/lwef/iagentcharacter--prepare) . **True** pone en cola la solicitud y hace que cualquier solicitud de animación que le siga espere hasta que se carguen los datos de animación que especifica. **False** recupera los datos de animación de forma asincrónica.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de solicitud de [**preparación**](/windows/desktop/lwef/iagentcharacter--prepare) .

</dd> </dl>

Si carga un carácter mediante el protocolo HTTP (. ACF), debe usar el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para recuperar los datos de animación antes de poder reproducir la animación. No puede usar este método si cargó el carácter mediante el protocolo UNC (. Archivo de ACS). Tampoco puede recuperar datos HTTP para un carácter mediante **Prepárese** Si cargó ese carácter mediante el protocolo UNC (. Archivo de caracteres de ACS).

Los datos de animación o de sonido recuperados con el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) se almacenan en la memoria caché del explorador. Las llamadas subsiguientes comprobarán la memoria caché y, si los datos de la animación ya están allí, el control cargará los datos directamente desde la memoria caché. Una vez cargados, los datos de animación o sonido se pueden reproducir con los métodos [**Play**](/windows/desktop/lwef/iagentcharacter--play) o [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) .

Puede especificar varias animaciones y Estados separándolos con comas. Sin embargo, no se pueden mezclar tipos en la misma instrucción [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) .

 

