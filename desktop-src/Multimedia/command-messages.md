---
title: Mensajes de comando
description: Mensajes de comando
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- Mensajes de comandos de MCI, acerca de
- Mensajes de comandos MCI, sintaxis
- mciSendCommand función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533100"
---
# <a name="command-messages"></a>Mensajes de comando

La interfaz de mensajes de comandos está diseñada para que la utilicen las aplicaciones que requieren una interfaz de lenguaje C para controlar los dispositivos multimedia. Utiliza un paradigma de paso de mensajes para comunicarse con dispositivos MCI. Puede enviar un comando mediante la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .

La función **mciSendCommand** devuelve cero si es correcto. Si se produce un error en la función, la palabra de orden inferior del valor devuelto contiene un código de error. Este código de error se puede pasar a la función [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obtener una descripción de texto del error.

## <a name="syntax-of-command-messages"></a>Sintaxis de los mensajes de comandos

Los mensajes de comandos MCI constan de los siguientes elementos:

-   Un valor de mensaje constante
-   Estructura que contiene los parámetros del comando.
-   Un conjunto de marcadores que especifican las opciones del comando y validan los campos en el bloque de parámetros.

En el ejemplo siguiente se usa la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar el comando [**MCI \_ Play**](mci-play.md) al dispositivo identificado mediante un identificador de dispositivo.


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



El identificador de dispositivo proporcionado en el primer parámetro se recupera cuando el dispositivo se abre con el comando [**MCI \_ Open**](mci-open.md) . El último parámetro es la dirección de una estructura de [**\_ \_ parms de reproducción de MCI**](mci-play-parms.md) , que podría contener información sobre dónde empezar y finalizar la reproducción. Muchos mensajes de comando de MCI usan una estructura para contener parámetros de este tipo. El primer miembro de cada una de estas estructuras identifica la ventana que recibe un mensaje [**mm \_ MCINOTIFY**](mm-mcinotify.md) cuando finaliza la operación.

 

 