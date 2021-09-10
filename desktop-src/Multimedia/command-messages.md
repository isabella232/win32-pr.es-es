---
title: Mensajes de comando
description: Mensajes de comando
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- Mensajes de comando de MCI, acerca de
- mensajes de comando de MCI, sintaxis
- Función mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371599"
---
# <a name="command-messages"></a>Mensajes de comando

La interfaz de mensaje de comando está diseñada para que la usen las aplicaciones que requieren una interfaz en lenguaje C para controlar los dispositivos multimedia. Usa un paradigma de paso de mensajes para comunicarse con dispositivos MCI. Puede enviar un comando mediante la [**función mciSendCommand.**](/previous-versions//dd757160(v=vs.85))

La **función mciSendCommand** devuelve cero si se realiza correctamente. Si se produce un error en la función, la palabra de orden bajo del valor devuelto contiene un código de error. Puede pasar este código de error a la [**función mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obtener una descripción de texto del error.

## <a name="syntax-of-command-messages"></a>Sintaxis de mensajes de comando

Los mensajes de comando MCI constan de los siguientes elementos:

-   Valor de mensaje constante
-   Estructura que contiene parámetros para el comando
-   Conjunto de marcas que especifican opciones para el comando y validan los campos del bloque de parámetros

En el ejemplo siguiente se usa [**la función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar el comando [**MCI \_ PLAY**](mci-play.md) al dispositivo identificado por un identificador de dispositivo.


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



El identificador de dispositivo especificado en el primer parámetro se recupera cuando el dispositivo se abre mediante el [**comando MCI \_ OPEN.**](mci-open.md) El último parámetro es la dirección de una estructura [**\_ MCI PLAY \_ PARMS,**](mci-play-parms.md) que puede contener información sobre dónde comenzar y finalizar la reproducción. Muchos mensajes de comando MCI usan una estructura para contener parámetros de este tipo. El primer miembro de cada una de estas estructuras identifica la ventana que recibe un mensaje [**\_ MM MTIFTIFY**](mm-mcinotify.md) cuando finaliza la operación.

 

 