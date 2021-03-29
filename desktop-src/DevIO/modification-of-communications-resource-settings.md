---
description: Cuando la función CreateFile abre un identificador de un recurso de comunicaciones serie, el sistema inicializa y configura el recurso de acuerdo con los valores configurados la última vez que se abrió el recurso.
ms.assetid: a39881d8-32af-4846-a2d3-508f1945b666
title: Modificación de la configuración de los recursos de comunicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8658029470fae9ee2d70ffb1459312c3c4d80ecf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080194"
---
# <a name="modification-of-communications-resource-settings"></a>Modificación de la configuración de los recursos de comunicaciones

Cuando la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) abre un identificador de un recurso de comunicaciones serie, el sistema inicializa y configura el recurso de acuerdo con los valores configurados la última vez que se abrió el recurso. Conservar la configuración anterior permite al usuario conservar la configuración especificada a través de un comando de **modo** cuando se vuelve a abrir el dispositivo. Los valores heredados de la operación de apertura anterior incluyen los valores de configuración del bloque de control del dispositivo (una estructura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) ) y los valores de tiempo de espera utilizados en las operaciones de e/s. Si el dispositivo no se ha abierto nunca, se configura con los valores predeterminados del sistema.

Para determinar la configuración inicial de un recurso de comunicaciones serie, un proceso llama a la función [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) , que rellena una estructura de [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) de puerto serie con las opciones de configuración actuales. Para modificar esta configuración, un proceso especifica una estructura **DCB** en una llamada a la función [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) .

Los miembros de la estructura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) especifican las opciones de configuración, como la velocidad en baudios, el número de bits de datos por byte y el número de bits de parada por byte. Otros miembros de **DCB** especifican caracteres especiales y habilitan la comprobación de paridad y el control de flujo. Cuando un proceso necesita modificar solo algunas de estas opciones de configuración, primero debe llamar a [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) para rellenar una estructura **DCB** con la configuración actual. Después, el proceso puede ajustar los valores importantes de la estructura **DCB** y volver a configurar el dispositivo llamando a [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) y especificando la estructura **DCB** modificada. Este procedimiento garantiza que los miembros no modificados de la estructura **DCB** contengan los valores adecuados. Por ejemplo, un error común es configurar un dispositivo con una estructura **DCB** en la que el miembro **XonChar** de la estructura sea igual que el miembro **XoffChar** .

La función [**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba) proporciona otra manera de modificar una estructura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) . **BuildCommDCB** usa una cadena con el mismo formato que los argumentos de la línea de comandos del comando de **modo** para especificar la velocidad en baudios, el esquema de paridad, el número de bits de parada y el número de bits de datos. El resto de los miembros de [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) no se modifican mediante esta función, salvo que los miembros adecuados se establecen para deshabilitar XON/XOFF y el control de flujo de hardware. **BuildCommDCB** solo modifica una estructura **DCB** ; no vuelve a configurar el dispositivo.

Un proceso puede volver a configurar un recurso de comunicaciones mediante la función [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) para obtener información de un controlador de dispositivo sobre las opciones de configuración que admite. El proceso puede utilizar esta información para evitar especificar una configuración que no se admite.

La función [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) vuelve a configurar el recurso de comunicaciones, pero no afecta a los búferes de entrada y salida internos del controlador especificado. Los búferes no se vacían y las operaciones de lectura y escritura pendientes no se terminan prematuramente.

Un proceso reinicializa un recurso de comunicaciones mediante la función [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm) , que realiza las tareas siguientes:

-   Finaliza las operaciones de lectura y escritura pendientes, incluso si no se han completado.
-   Descarta los caracteres no leídos y libera los búferes de entrada y salida internos del controlador asociado con el recurso especificado.
-   Reasigna los búferes de entrada y salida internos.

No es necesario un proceso para llamar a [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm). Si no es así, el controlador del recurso inicializa el dispositivo con la configuración predeterminada la primera vez que se usa el identificador de recursos de comunicaciones.

 

 
