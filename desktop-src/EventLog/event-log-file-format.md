---
description: Cada registro de eventos contiene un encabezado (representado por la estructura LOGFILE HEADER de ELF) que tiene un tamaño fijo, seguido de un número variable de registros de eventos (representados por estructuras EVENTLOGRECORD) y un registro de fin de archivo (representado por la estructura EOF RECORD de \_ \_ \_ ELF). \_
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: Formato de archivo de registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ed6df35ac1fcd641a9a895b2c32eb34d6a4c1cb472ab03f16417f55900c767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814302"
---
# <a name="event-log-file-format"></a>Formato de archivo de registro de eventos

Cada registro de eventos contiene un encabezado (representado por la estructura [**\_ LOGFILE \_ HEADER de ELF)**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) que tiene un tamaño fijo, seguido de un número variable de registros de eventos (representados por estructuras [**EVENTLOGRECORD)**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) y un registro de fin de archivo (representado por la estructura [**\_ EOF \_ RECORD de ELF).**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85))

La **estructura ELF \_ LOGFILE \_ HEADER** y la estructura **ELF \_ EOF \_ RECORD** se escriben en el registro de eventos cuando se crea el registro de eventos y se actualizan cada vez que se escribe un evento en el registro.

Cuando una aplicación llama a la [**función ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) para escribir una entrada en el registro de eventos, el sistema pasa los parámetros al servicio de registro de eventos. El servicio de registro de eventos usa la información para escribir una **estructura EVENTLOGRECORD** en el registro de eventos. En el siguiente diagrama se muestra este proceso.

![escribir un archivo de registro](images/evreport.png)

Los registros de eventos se organizan de una de las maneras siguientes:

-   No encapsulado. El registro más antiguo se encuentra inmediatamente después del encabezado del registro de eventos y se agregan nuevos registros después del último registro que se agregó (antes de **\_ EOF \_ RECORD de ELF).** En el ejemplo siguiente se muestra el método de no ajuste:

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    El no ajuste puede producirse cuando se crea el registro de eventos o cuando se borra el registro de eventos. El registro de eventos sigue sin ajustarse hasta que se alcanza el límite de tamaño del registro de eventos. El tamaño del registro de eventos está limitado por el valor **de configuración MaxSize** o la cantidad de recursos del sistema.

    Cuando se alcanza el límite de tamaño del registro de eventos, podría empezar a ajustarse. El ajuste se controla mediante el **valor de configuración Retención.** Para obtener más información sobre los valores de configuración del registro de eventos, vea [Eventlog Key](eventlog-key.md).

-   Envoltura. Los registros se organizan como búfer circular. A medida que se agregan nuevos registros, se reemplazan los registros más antiguos. La ubicación de los registros más antiguos y más nuevos variará. En el ejemplo siguiente se muestra el método de ajuste.

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    EVENT RECORD 301         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 400         (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    Wasted space
    EVENT RECORD 102         (EVENTLOGRECORD)
    EVENT RECORD 103         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 299         (EVENTLOGRECORD)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    ```

    En el ejemplo, el registro más antiguo ya no es 1, pero es 102 porque se sobrescribía el espacio para los registros 1 a 101.

    Hay cierto espacio entre **el registro \_ EOF \_** de ELF y el registro más antiguo porque el sistema borrará un número entero de registros para liberar espacio para el registro más reciente. Por ejemplo, si el registro más reciente tiene 100 bytes de longitud y los dos registros más antiguos tienen 75 bytes, el sistema quitará los dos registros más antiguos. Los 50 bytes adicionales se usarán más adelante cuando se escriban nuevos registros.

    Un archivo de registro de eventos tiene un tamaño fijo y, cuando los registros del archivo se encapsulan, el registro al final del archivo normalmente se dividirá en dos registros. Por ejemplo, si la posición de la siguiente escritura es de 100 bytes desde el final del archivo y el tamaño del registro es de 300 bytes, los primeros 100 bytes se escribirán al final del archivo y los 200 bytes siguientes se escribirán al principio del archivo inmediatamente después de **ELF \_ LOGFILE \_ HEADER**. Si el espacio disponible al final del archivo es menor que la parte fija de **EVENTLOGRECORD** (0x38 bytes), todo el nuevo registro se escribirá al principio del archivo inmediatamente después de **ELF \_ LOGFILE \_ HEADER**. Los bytes no usados al final del archivo se rellenarán con el patrón 0x00000027.

Para obtener más información y un ejemplo de código, vea [Notificar un evento](reporting-an-event.md).

 

 
