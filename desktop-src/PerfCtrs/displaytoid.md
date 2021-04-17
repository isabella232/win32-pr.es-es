---
description: La tabla DisplayToID relaciona la cadena descriptiva que muestra el monitor de sistema con el GUID almacenado en las otras tablas.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b71ae8c4ebaafc80d98580a13a83e3cc7cff815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667332"
---
# <a name="displaytoid"></a>DisplayToID

La tabla **DisplayToID** relaciona la cadena descriptiva que muestra el monitor de sistema con el GUID almacenado en las otras tablas.

La tabla **DisplayToID** define los campos siguientes:

-   **GUID:** Identificador único generado para un registro. Este campo es la clave principal de esta tabla.
-   **RunID:** Reservado para uso interno.
-   **DisplayString:** Nombre del archivo de registro que se muestra en el monitor de sistema.
-   **LogStartTime:** Hora en que se inició el proceso de registro en formato AAAA-MM-DD HH: mm: SS: nnn.
-   **LogStopTime:** Hora en que el proceso de registro se detuvo en el formato AAAA-MM-DD HH: mm: SS: nnn. Se pueden diferenciar varios archivos de registro con el mismo valor **DisplayString** usando el valor de los campos y **LogStartTime** . Los valores de los campos **LogStartTime** y **LogStopTime** también permiten acceder rápidamente al tiempo total de recopilación.
-   **NumberOfRecords:** Número de muestras almacenadas en la tabla para cada colección de registros.
-   **MinutesToUTC:** Valor que se usa para convertir los datos de fila almacenados en hora UTC en hora local.
-   **TimeZoneName:** Nombre de la zona horaria en la que se recopilaron los datos. Si va a recopilar datos de un archivo recopilado en sistemas que se encuentran en su propia zona horaria, este campo indicará la ubicación.

**Nota:**  Antes de Windows Vista, los conjuntos de recopiladores de datos se almacenaban en el registro en

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ SysmonLog \\ log queries**

. Los campos enumerados anteriormente no corresponden a los valores del registro. En Windows Vista, los conjuntos de recopiladores de datos no se almacenan en el registro.

 

 



