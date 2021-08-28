---
title: Desconectando
description: Cuando una aplicación cliente RAS inicia una operación de conexión, la llamada RasDial recibe un identificador de conexión HRASCONN para identificar la conexión.
ms.assetid: a0fddc69-44bb-4bb0-ae57-ebecbe85cbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fde205dfeb838639447c9f9359ee5b1258b2426eb55dbdd592291aea002fad6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101865"
---
# <a name="disconnecting"></a>Desconectando

Cuando una aplicación cliente RAS inicia una operación de conexión, la llamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) recibe un identificador de conexión **HRASCONN** para identificar la conexión. Si el identificador devuelto no es **NULL,** el cliente debe llamar finalmente a la [**función RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) para finalizar la conexión. Si se produce un error durante la operación de conexión, el cliente debe llamar a **RasHangUp** aunque nunca se haya establecido la conexión.

La aplicación que llama [**a RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) no debe salir inmediatamente porque el administrador de acceso Connection Manager necesita tiempo para finalizar correctamente la conexión. En su lugar, la aplicación debe esperar hasta que la [**función RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) devuelva ERROR INVALID HANDLE, lo que indica \_ que se ha eliminado la \_ conexión.

Es posible que una aplicación cliente RAS tenga que finalizar una conexión aunque no tenga el identificador devuelto por [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala). Por ejemplo, la aplicación que llamó **a RasDial** podría haber salido después de establecer correctamente la conexión. En este caso, la aplicación de desconexión puede usar la [**función RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) para obtener todas las conexiones actuales. Para cada conexión, **RasEnumConnections** devuelve una estructura [**RASCONN**](/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)) que contiene el identificador de conexión **HRASCONN** y el nombre de la entrada de la libreta de teléfono o el número de teléfono especificados cuando se inició la operación de conexión. Esta información se puede usar para mostrar una lista de conexiones desde las que el usuario puede seleccionar la conexión para finalizar.

 

 