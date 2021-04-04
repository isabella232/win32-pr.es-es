---
title: Desconectando
description: Cuando una aplicación cliente RAS inicia una operación de conexión, la llamada RasDial recibe un identificador de conexión HRASCONN para identificar la conexión.
ms.assetid: a0fddc69-44bb-4bb0-ae57-ebecbe85cbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859a3751bcbaf7d95927cdf6d14de859ddcc731e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078289"
---
# <a name="disconnecting"></a>Desconectando

Cuando una aplicación cliente RAS inicia una operación de conexión, la llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) recibe un identificador de conexión **HRASCONN** para identificar la conexión. Si el identificador devuelto no es **null**, el cliente debe llamar finalmente a la función [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) para finalizar la conexión. Si se produce un error durante la operación de conexión, el cliente debe llamar a **RasHangUp** aunque no se haya establecido nunca la conexión.

La aplicación que llama a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) no debe salir inmediatamente porque el administrador de conexiones de acceso remoto necesita tiempo para finalizar correctamente la conexión. En su lugar, la aplicación debe esperar hasta que la función [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) devuelva un error de \_ identificador no válido \_ , lo que indica que se ha eliminado la conexión.

Es posible que una aplicación cliente RAS tenga que finalizar una conexión aunque no tenga el identificador devuelto por [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala). Por ejemplo, la aplicación que llamó a **rasdial** podría haber salido una vez establecida correctamente la conexión. En este caso, la aplicación de desconexión puede utilizar la función [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) para obtener todas las conexiones actuales. Para cada conexión, **RasEnumConnections** devuelve una estructura [**RASCONN**](/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)) que contiene el identificador de conexión **HRASCONN** y el nombre de entrada o número de teléfono del libro de teléfono especificado cuando se inició la operación de conexión. Esta información se puede usar para mostrar una lista de conexiones desde las que el usuario puede seleccionar la conexión que desea finalizar.

 

 