---
title: Comunicación con dispositivos MCI
description: Comunicación con dispositivos MCI
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- MCIWndSendString (macro)
- mciSendString función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7f5458cff0ef4c5c5f84e565fae06ade8796c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651346"
---
# <a name="communicating-with-mci-devices"></a>Comunicación con dispositivos MCI

El controlador de cada dispositivo MCI mantiene una lista de la configuración y las capacidades actuales, de modo que puede emitir una respuesta precisa cuando se consulta información.

Si desea comunicarse con un dispositivo MCI, puede usar las macros y funciones de MCIWnd. Muchos de los comandos y consultas de MCI más comunes se definen como macros. Sin embargo, si la tarea que desea realizar no está disponible como una función o macro, puede enviar comandos MCI directamente al controlador de dispositivo mediante la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) o mediante el formulario de mensaje o la forma de cadena de los comandos MCI. El uso de la macro **MCIWndSendString** es equivalente a utilizar la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) de la siguiente manera:


```C++
mciSendString(sz, Null, 0, Null) 
```



Los parámetros de [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) solo incluyen el identificador de ventana y la forma de cadena del comando. Para recuperar la información devuelta por un comando de cadena, use la macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .

Para obtener más información acerca de MCI, consulte [MCI](mci.md).

> [!Note]  
> Debe excluir el alias del dispositivo del comando MCI al usar **MCIWndSendString**. La biblioteca MCIWnd agrega este alias cuando envía el comando al dispositivo MCI.

 

 

 