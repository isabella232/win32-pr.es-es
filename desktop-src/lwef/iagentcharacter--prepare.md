---
title: Preparación de IAgentCharacter
description: Preparación de IAgentCharacter
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b383bf10330934379990693b75fe2908a432f8d5
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119880"
---
# <a name="iagentcharacterprepare"></a>IAgentCharacter::P repare

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

Recupera los datos de animación de un carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente. Cuando la función devuelve un resultado, *pdwReqID* contiene el identificador de la solicitud.

<dl> <dt>

<span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*
</dt> <dd>

Valor que indica el tipo de datos de animación que se va a cargar y que debe ser uno de los siguientes:



| Valor                                                           | Descripción                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| **const unsigned short** **PREPARE ANIMATION = \_ 0;**<br/> | Datos de animación de un carácter.                              |
| **const unsigned short** **PREPARE STATE = \_ 1;**<br/>     | Datos de estado de un carácter.                                  |
| **const unsigned short** **PREPARE WAVE = \_ 2**<br/>       | Archivo de sonido de un carácter (. WAV o . LWV) para la salida hablada. |



 

</dd> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

Nombre de la animación o el estado.

El nombre de animación se basa en el definido para el carácter cuando se guardó mediante el Editor de caracteres de Microsoft Agent.

Para los estados, el valor puede ser uno de los siguientes:



|                      | Descripción                                     |
|----------------------|-------------------------------------------------|
| **"Gesturing"**      | Para recuperar todas las **animaciones de estado Gesturing.** |
| **"GesturingDown"**  | Para recuperar **animaciones GesturingDown.**       |
| **"GesturingLeft"**  | Para recuperar **animaciones GesturingLeft.**       |
| **"GesturingRight"** | Para recuperar **animaciones GesturingRight.**      |
| **"GesturingUp"**    | Para recuperar **animaciones GesturingUp.**         |
| **"Ocultar"**         | Para recuperar las **animaciones de** estado Ocultar.    |
| **"Audiencia"**        | Para recuperar las **animaciones de** estado de la audiencia.   |
| **"Idling"**         | Para recuperar todas las animaciones de estado de **idling.**    |
| **"IdlingLevel1"**   | Para recuperar todas **las animaciones IdlingLevel1.**    |
| **"IdlingLevel2"**   | Para recuperar todas **las animaciones IdlingLevel2.**    |
| **"IdlingLevel3"**   | Para recuperar todas **las animaciones IdlingLevel3.**    |
| **"Escuchando"**      | Para recuperar las **animaciones de** estado De escucha. |
| **"Mover"**         | Para recuperar todas las **animaciones de** estado de movimiento.    |
| **"MovingDown"**     | Para recuperar todas **las animaciones de** movimiento.          |
| **"MovingLeft"**     | Para recuperar todas **las animaciones MovingLeft.**      |
| **"MovingRight"**    | Para recuperar todas **las animaciones MovingRight.**     |
| **"MovingUp"**       | Para recuperar todas **las animaciones MovingUp.**        |
| **"Mostrando"**        | Para recuperar las **animaciones de** estado Mostrando.   |
| **"Habla"**       | Para recuperar las **animaciones de** estado de habla.  |



 

Para. Archivos WAV, establezca *bszName en* la dirección URL o la especificación de archivo para . Archivo WAV. Si la especificación no está completa, se interpreta como relativa a la especificación usada en el [**método Load.**](https://www.bing.com/search?q=**Load**)

</dd> <dt>

<span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*
</dt> <dd>

Valor booleano que especifica si el servidor pone en cola la [**solicitud Prepare.**](/windows/desktop/lwef/iagentcharacter--prepare) **True** pone en cola la solicitud y hace que cualquier solicitud de animación que le sigue espere hasta que se carguen los datos de animación que especifica. **False** recupera los datos de animación de forma asincrónica.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador [**de solicitud**](/windows/desktop/lwef/iagentcharacter--prepare) de preparación.

</dd> </dl>

Si carga un carácter mediante el protocolo HTTP (un . Archivo ACF), debe usar el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para recuperar datos de animación antes de poder reproducir la animación. No puede usar este método si cargó el carácter mediante el protocolo UNC (un . ARCHIVO DE ACS). Tampoco puede recuperar datos HTTP para un carácter mediante **Prepare** si cargó ese carácter mediante el protocolo UNC (. Archivo de caracteres de ACS).

Los datos de animación o sonido recuperados con [**el método Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) se almacenan en la memoria caché del explorador. Las llamadas posteriores comprobarán la memoria caché y, si los datos de animación ya están allí, el control carga los datos directamente desde la memoria caché. Una vez cargados, los datos de animación o sonido se pueden reproducir con los [**métodos Play**](/windows/desktop/lwef/iagentcharacter--play) [**o Speak.**](/windows/desktop/lwef/iagentcharacter--speak)

Puede especificar varias animaciones y estados si los separa con comas. Sin embargo, no puede mezclar tipos en la misma [**instrucción Prepare.**](/windows/desktop/lwef/iagentcharacter--prepare)

 

