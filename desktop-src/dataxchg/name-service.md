---
title: Servicio de nombres
description: En este tema se describe cómo la biblioteca de administración de Intercambio dinámico de datos permite a una aplicación de servidor registrar los nombres de servicio que admite.
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- Interfaz de usuario de Windows, Intercambio dinámico de datos (DDE)
- Intercambio dinámico de datos (DDE), servicio de nombres
- DDE (Intercambio dinámico de datos), servicio de nombres
- intercambio de datos, Intercambio dinámico de datos (DDE)
- Interfaz de usuario de Windows, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), servicio de nombres
- DDEML (biblioteca de administración de Intercambio dinámico de datos), servicio de nombres
- intercambio de datos, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Intercambio dinámico de datos (DDE), registro de nombre de servicio
- DDE (Intercambio dinámico de datos), registro de nombre de servicio
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), registro de nombre de servicio
- DDEML (biblioteca de administración de Intercambio dinámico de datos), registro de nombre de servicio
- Intercambio dinámico de datos (DDE), filtro de nombre de servicio
- DDE (Intercambio dinámico de datos), filtro de nombre de servicio
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), filtro de nombre de servicio
- DDEML (biblioteca de administración de Intercambio dinámico de datos), filtro de nombre de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f958ab73164e70177cb5deeb5f400f44695015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357760"
---
# <a name="name-service"></a>Servicio de nombres

La biblioteca de administración de Intercambio dinámico de datos (DDEML) permite a una aplicación de servidor registrar los nombres de servicio que admite y evitar que DDEML envíe transacciones de [**\_ conexión de XTYP**](xtyp-connect.md) para los nombres de servicio no admitidos a la función de devolución de llamada del intercambio dinámico de datos (DDE) del servidor.

En los temas siguientes se describe el servicio de nombres.

-   [Registro de nombre de servicio](#service-name-registration)
-   [Filtro de nombre de servicio](#service-name-filter)

## <a name="service-name-registration"></a>Registro de nombre de servicio

Al registrar sus nombres de servicio con el DDEML, un servidor informa a otras aplicaciones DDE del sistema de que hay un nuevo servidor disponible. Un servidor registra un nombre de servicio llamando a la función [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) y especificando un identificador de cadena que identifica el nombre. En respuesta, el DDEML envía una transacción de [**\_ registro XTYP**](xtyp-register.md) a la función de devolución de llamada de cada aplicación ddeml en el sistema (excepto las que especificaron la \_ \_ marca de filtro CBF SKIP registros en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ). La transacción de **\_ registro XTYP** pasa dos identificadores de cadena a una función de devolución de llamada: el primero identifica la cadena que especifica el nombre del servicio base y la segunda identifica la cadena que especifica el servicio específico de la instancia. Un cliente normalmente usa el nombre del servicio base en una lista de servidores disponibles, por lo que el usuario puede seleccionar un servidor de la lista. El cliente utiliza el nombre del servicio específico de la instancia para establecer una conversación con una instancia específica de una aplicación de servidor, si se está ejecutando más de una instancia.

Un servidor puede usar [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para anular el registro de un nombre de servicio. Esta función hace que DDEML envíe transacciones de [**XTYP \_ unregister**](xtyp-unregister.md) a las demás aplicaciones DDE del sistema, lo que les informa de que ya no pueden usar el nombre para establecer conversaciones.

Un servidor debe llamar a [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar sus nombres de servicio pronto después de llamar a [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Un servidor debe anular el registro de sus nombres de servicio mediante **DdeNameService** justo antes de llamar a la función [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .

## <a name="service-name-filter"></a>Filtro de nombre de servicio

Además de registrar los nombres de servicio, [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) permite a un servidor activar o desactivar el filtro de nombre de servicio. Cuando un servidor desactiva su filtro de nombre de servicio, el DDEML envía la transacción [**XTYP \_ Connect**](xtyp-connect.md) a la función de devolución de llamada DDE del servidor cada vez que un cliente llama a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , independientemente del nombre del servicio especificado en la función. Cuando un servidor activa su filtro de nombre de servicio, el DDEML envía la transacción **XTYP \_ Connect** al servidor solo cuando **DdeConnect** especifica un nombre de servicio que el servidor ha especificado en una llamada a **DdeNameService**.

De forma predeterminada, el filtro de nombre de servicio está activado cuando una aplicación llama a [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Este valor predeterminado evita que DDEML envíe la transacción [**XTYP \_ Connect**](xtyp-connect.md) a un servidor antes de que el servidor haya creado la cadena que necesita. Un servidor puede desactivar su filtro de nombre de servicio especificando la \_ marca FILTEROFF de DNS en una llamada a [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice). La marca de filtro de DNS \_ activa el filtro.

 

 




