---
description: La tabla DisplayToID relaciona la cadena fácil de usar mostrada por el Monitor de sistema con el GUID almacenado en las otras tablas.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485eab24a2c758b36e190e035a9442a032ebd683f3f5ea052bd37992ad14c85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033915"
---
# <a name="displaytoid"></a>DisplayToID

La **tabla DisplayToID** relaciona la cadena fácil de usar mostrada por el Monitor de sistema con el GUID almacenado en las otras tablas.

La **tabla DisplayToID** define los campos siguientes:

-   **GUID:** Identificador único generado para un registro. Este campo es la clave principal de esta tabla.
-   **RunID:** Reservado para uso interno.
-   **DisplayString:** Nombre del archivo de registro tal como se muestra en el Monitor de sistema.
-   **LogStartTime:** Hora en que se inició el proceso de registro en formato yyyy-mm-dd hh:mm:ss:nnn.
-   **LogStopTime:** Hora en que el proceso de registro se detuvo en formato yyyy-mm-dd hh:mm:ss:nnn. Se pueden diferenciar varios archivos de registro con el mismo valor **displayString** mediante el uso del valor de y los **campos LogStartTime.** Los valores de los **campos LogStartTime** y **LogStopTime** también permiten acceder rápidamente al tiempo total de recopilación.
-   **NumberOfRecords:** Número de ejemplos almacenados en la tabla para cada colección de registros.
-   **MinutesToUTC:** Valor utilizado para convertir los datos de fila almacenados en hora UTC a la hora local.
-   **TimeZoneName:** Nombre de la zona horaria donde se recopilaron los datos. Si va a recopilar o a volver a etiquetar datos de un archivo recopilado en sistemas de su propia zona horaria, este campo mostrará la ubicación.

**Nota**  Antes de Windows Vista, los conjuntos de recopiladores de datos se almacenaban en el registro en

**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Services \\ SysmonLog \\ Log Queries**

. Los campos enumerados anteriormente no corresponden a los valores del Registro. Por Windows Vista, los conjuntos de recopiladores de datos no se almacenan en el Registro.

 

 



