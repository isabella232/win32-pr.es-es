---
title: Comunicación con dispositivos MCI
description: Comunicación con dispositivos MCI
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- Macro MCIWndSendString
- Función mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3def53cda9374ba50dfea8252918f073d961410092a977c8779f3a29d6b36204
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807845"
---
# <a name="communicating-with-mci-devices"></a>Comunicación con dispositivos MCI

El controlador de cada dispositivo MCI mantiene una lista de su configuración y funcionalidades actuales, por lo que puede emitir una respuesta precisa cuando se le consulta para obtener información.

Si desea comunicarse con un dispositivo MCI, puede usar macros y funciones de MCIWnd. Muchos de los comandos y consultas de MCI más comunes se definen como macros. Sin embargo, si la tarea que desea realizar no está disponible como función o macro, puede enviar comandos MCI directamente al controlador de dispositivo mediante la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) o mediante el formulario de mensaje o la forma de cadena de los comandos MCI. El uso de la macro **MCIWndSendString** equivale a usar la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) como se muestra a continuación:


```C++
mciSendString(sz, Null, 0, Null) 
```



Los parámetros de [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) incluyen solo el identificador de ventana y la forma de cadena del comando. Para recuperar la información devuelta por un comando de cadena, use la macro [**MCIWndReturnString.**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)

Para obtener más información sobre MCI, vea [MCI](mci.md).

> [!Note]  
> Debe excluir el alias de dispositivo del comando MCI cuando use **MCIWndSendString**. La biblioteca MCIWnd agrega este alias cuando envía el comando al dispositivo MCI.

 

 

 