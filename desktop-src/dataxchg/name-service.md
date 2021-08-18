---
title: Servicio de nombres
description: En este tema se describe cómo datos dinámicos Exchange Management Library permite que una aplicación de servidor registre los nombres de servicio que admite.
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- Windows Interfaz de usuario,datos dinámicos Exchange (DDE)
- datos dinámicos Exchange (DDE), servicio de nombres
- DDE (datos dinámicos Exchange),name service
- intercambio de datos, datos dinámicos Exchange (DDE)
- Windows Interfaz de usuario,datos dinámicos Exchange Management Library (DDEML)
- datos dinámicos Exchange Management Library (DDEML),name service
- DDEML (datos dinámicos Exchange management library),name service
- data exchange,datos dinámicos Exchange Management Library (DDEML)
- datos dinámicos Exchange (DDE),registro de nombres de servicio
- DDE (datos dinámicos Exchange), registro de nombres de servicio
- datos dinámicos Exchange Management Library (DDEML), registro de nombres de servicio
- DDEML (datos dinámicos Exchange management library),registro de nombres de servicio
- datos dinámicos Exchange (DDE),filtro de nombre de servicio
- DDE (datos dinámicos Exchange), filtro de nombre de servicio
- datos dinámicos Exchange Management Library (DDEML), filtro de nombre de servicio
- DDEML (datos dinámicos Exchange Management Library),filtro de nombre de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7346bd98979e9bd5a4aa0e43493e975d802875cf8fd0fc79d7bd002bcd0c5494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811652"
---
# <a name="name-service"></a>Servicio de nombres

La biblioteca de administración de datos dinámicos Exchange (DDEML) permite a una aplicación de servidor registrar los nombres de servicio que admite y evitar que DDEML envíe transacciones [**XTYP \_ CONNECT**](xtyp-connect.md) para nombres de servicio no admitidos a la función de devolución de llamada datos dinámicos Exchange (DDE) del servidor.

En los temas siguientes se describe el servicio de nombres.

-   [Registro de nombres de servicio](#service-name-registration)
-   [Filtro de nombre de servicio](#service-name-filter)

## <a name="service-name-registration"></a>Registro de nombres de servicio

Al registrar sus nombres de servicio con DDEML, un servidor informa a otras aplicaciones DDE en el sistema de que hay disponible un nuevo servidor. Un servidor registra un nombre de servicio llamando a la función [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) y especificando un identificador de cadena que identifica el nombre. En respuesta, DDEML envía una transacción [**XTYP \_ REGISTER**](xtyp-register.md) a la función de devolución de llamada de cada aplicación DDEML del sistema (excepto las que especificaron la marca de filtro CBF SKIP REGISTRATIONS en la función \_ \_ [**DdeInitialize).**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) La transacción **XTYP \_ REGISTER** pasa dos identificadores de cadena a una función de devolución de llamada: el primero identifica la cadena que especifica el nombre del servicio base y el segundo identifica la cadena que especifica el servicio específico de la instancia. Normalmente, un cliente usa el nombre del servicio base en una lista de servidores disponibles, por lo que el usuario puede seleccionar un servidor de la lista. El cliente usa el nombre de servicio específico de la instancia para establecer una conversación con una instancia específica de una aplicación de servidor, si se ejecuta más de una instancia.

Un servidor puede usar [**DdeNameService para**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) anular el registro de un nombre de servicio. Esta función hace que DDEML envíe transacciones [**\_ UNREGISTER de XTYP**](xtyp-unregister.md) a las otras aplicaciones DDE del sistema, informándolos de que ya no pueden usar el nombre para establecer conversaciones.

Un servidor debe llamar a [**DdeNameService para**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) registrar sus nombres de servicio poco después de llamar a [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Un servidor debe anular el registro de sus nombres de servicio mediante **DdeNameService** justo antes de llamar a la [**función DdeUninitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)

## <a name="service-name-filter"></a>Filtro de nombre de servicio

Además de registrar nombres de servicio, [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) permite que un servidor active o desactive su filtro de nombre de servicio. Cuando un servidor desactiva su filtro de nombre de servicio, DDEML envía la transacción [**XTYP \_ CONNECT**](xtyp-connect.md) a la función de devolución de llamada DDE del servidor cada vez que un cliente llama a la función [**DdeConnect,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) independientemente del nombre de servicio especificado en la función. Cuando un servidor activa su filtro de nombre de servicio, DDEML envía la transacción **XTYP \_ CONNECT** al servidor solo cuando **DdeConnect** especifica un nombre de servicio que el servidor ha especificado en una llamada a **DdeNameService**.

De forma predeterminada, el filtro de nombre de servicio está en cuando una aplicación llama a [**DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Este valor predeterminado impide que DDEML envíe la transacción [**XTYP \_ CONNECT**](xtyp-connect.md) a un servidor antes de que el servidor haya creado los identificadores de cadena que necesita. Un servidor puede desactivar su filtro de nombre de servicio especificando la marca FILTEROFF de DNS en \_ una llamada a [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice). La marca FILTERON de DNS \_ activa el filtro.

 

 




