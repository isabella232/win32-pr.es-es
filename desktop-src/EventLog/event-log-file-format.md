---
description: Cada registro de eventos contiene un encabezado (representado por la estructura de encabezado del archivo de \_ registro Elf \_ ) que tiene un tamaño fijo, seguido de un número variable de registros de eventos (representados por estructuras EVENTLOGRECORD) y un registro de fin de archivo (representado por la estructura de registro de EOF de Elf \_ \_ ).
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: Formato de archivo de registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4ba5c8bc0114e319107272e706801544e3effa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545027"
---
# <a name="event-log-file-format"></a>Formato de archivo de registro de eventos

Cada registro de eventos contiene un encabezado (representado por la estructura de encabezado del archivo de [**\_ \_ registro Elf**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) ) que tiene un tamaño fijo, seguido de un número variable de registros de eventos (representados por estructuras [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) ) y un registro de fin de archivo (representado por la estructura de [**registro de \_ EOF \_ de Elf**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) ).

La estructura de encabezado del archivo de **\_ Registro \_ Elf** y la estructura de **\_ \_ registro EOF de Elf** se escriben en el registro de eventos cuando se crea el registro de eventos y se actualizan cada vez que se escribe un evento en el registro.

Cuando una aplicación llama a la función [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) para escribir una entrada en el registro de eventos, el sistema pasa los parámetros al servicio de registro de eventos. El servicio de registro de eventos utiliza la información para escribir una estructura **EVENTLOGRECORD** en el registro de eventos. En el siguiente diagrama se muestra este proceso.

![escribir un archivo de registro](images/evreport.png)

Los registros de eventos se organizan de una de las siguientes maneras:

-   Sin ajuste. El registro más antiguo está inmediatamente después del encabezado del registro de eventos y se agregan nuevos registros después del último registro que se agregó (antes del **\_ \_ registro de EOF de Elf**). En el ejemplo siguiente se muestra el método sin ajuste:

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    El no ajuste puede producirse cuando se crea el registro de eventos o cuando se borra el registro de eventos. El registro de eventos sigue siendo de no ajuste hasta que se alcanza el límite de tamaño del registro de eventos. El tamaño del registro de eventos está limitado por el valor de configuración **MaxSize** o la cantidad de recursos del sistema.

    Cuando se alcanza el límite de tamaño del registro de eventos, puede comenzar el ajuste. El ajuste se controla mediante el valor de configuración **retención** . Para obtener más información sobre los valores de configuración del registro de eventos, vea [EventLog Key](eventlog-key.md).

-   Envoltura. Los registros se organizan como un búfer circular. A medida que se agregan nuevos registros, se reemplazan los registros más antiguos. La ubicación de los registros más antiguos y más recientes variará. En el siguiente ejemplo se muestra el método de ajuste.

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

    En el ejemplo, el registro más antiguo ya no es 1, pero es 102 porque se ha sobrescrito el espacio de los registros 1 a 101.

    Hay cierto espacio entre el **registro de \_ EOF \_ de Elf** y el registro más antiguo, ya que el sistema borrará un número entero de registros para liberar espacio para el registro más reciente. Por ejemplo, si el registro más reciente tiene 100 bytes de longitud y los dos registros más antiguos tienen una longitud de 75 bytes, el sistema quitará los dos registros más antiguos. Los bytes adicionales 50 se utilizarán más adelante cuando se escriban nuevos registros.

    Un archivo de registro de eventos tiene un tamaño fijo y, cuando se ajustan los registros del archivo, el registro situado al final del archivo se dividirá normalmente en dos registros. Por ejemplo, si la posición de la siguiente escritura es 100 bytes desde el final del archivo y el tamaño del registro es de 300 bytes, los primeros 100 bytes se escribirán al final del archivo y los siguientes 200 bytes se escribirán al principio del archivo inmediatamente después del **\_ \_ encabezado de registro Elf**. Si el espacio disponible al final del archivo es menor que la parte fija del **EVENTLOGRECORD** (0x38 bytes), todo el registro nuevo se escribirá al principio del archivo inmediatamente después del encabezado del archivo de registro de **Elf \_ \_**. Los bytes no usados al final del archivo se rellenarán con el patrón 0x00000027.

Para obtener más información y un ejemplo de código, vea [informar de un evento](reporting-an-event.md).

 

 
