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
# <a name="event-log-file-format"></a><span data-ttu-id="8091c-103">Formato de archivo de registro de eventos</span><span class="sxs-lookup"><span data-stu-id="8091c-103">Event Log File Format</span></span>

<span data-ttu-id="8091c-104">Cada registro de eventos contiene un encabezado (representado por la estructura de encabezado del archivo de [**\_ \_ registro Elf**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) ) que tiene un tamaño fijo, seguido de un número variable de registros de eventos (representados por estructuras [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) ) y un registro de fin de archivo (representado por la estructura de [**registro de \_ EOF \_ de Elf**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) ).</span><span class="sxs-lookup"><span data-stu-id="8091c-104">Each event log contains a header (represented by the [**ELF\_LOGFILE\_HEADER**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) structure) that has a fixed size, followed by a variable number of event records (represented by [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) structures), and an end-of-file record (represented by the [**ELF\_EOF\_RECORD**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) structure).</span></span>

<span data-ttu-id="8091c-105">La estructura de encabezado del archivo de **\_ Registro \_ Elf** y la estructura de **\_ \_ registro EOF de Elf** se escriben en el registro de eventos cuando se crea el registro de eventos y se actualizan cada vez que se escribe un evento en el registro.</span><span class="sxs-lookup"><span data-stu-id="8091c-105">The **ELF\_LOGFILE\_HEADER** structure and the **ELF\_EOF\_RECORD** structure are written in the event log when the event log is created and are updated each time an event is written to the log.</span></span>

<span data-ttu-id="8091c-106">Cuando una aplicación llama a la función [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) para escribir una entrada en el registro de eventos, el sistema pasa los parámetros al servicio de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="8091c-106">When an application calls the [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) function to write an entry to the event log, the system passes the parameters to the event-logging service.</span></span> <span data-ttu-id="8091c-107">El servicio de registro de eventos utiliza la información para escribir una estructura **EVENTLOGRECORD** en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="8091c-107">The event-logging service uses the information to write an **EVENTLOGRECORD** structure to the event log.</span></span> <span data-ttu-id="8091c-108">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="8091c-108">The following diagram illustrates this process.</span></span>

![escribir un archivo de registro](images/evreport.png)

<span data-ttu-id="8091c-110">Los registros de eventos se organizan de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="8091c-110">The event records are organized in one of the following ways:</span></span>

-   <span data-ttu-id="8091c-111">Sin ajuste.</span><span class="sxs-lookup"><span data-stu-id="8091c-111">Non-wrapping.</span></span> <span data-ttu-id="8091c-112">El registro más antiguo está inmediatamente después del encabezado del registro de eventos y se agregan nuevos registros después del último registro que se agregó (antes del **\_ \_ registro de EOF de Elf**).</span><span class="sxs-lookup"><span data-stu-id="8091c-112">The oldest record is immediately after the event log header and new records are added after the last record that was added (before the **ELF\_EOF\_RECORD**).</span></span> <span data-ttu-id="8091c-113">En el ejemplo siguiente se muestra el método sin ajuste:</span><span class="sxs-lookup"><span data-stu-id="8091c-113">The following example shows the non-wrapping method:</span></span>

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    <span data-ttu-id="8091c-114">El no ajuste puede producirse cuando se crea el registro de eventos o cuando se borra el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="8091c-114">Non-wrapping can occur when the event log is created or when the event log is cleared.</span></span> <span data-ttu-id="8091c-115">El registro de eventos sigue siendo de no ajuste hasta que se alcanza el límite de tamaño del registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="8091c-115">The event log continues to be non-wrapping until the event log size limit is reached.</span></span> <span data-ttu-id="8091c-116">El tamaño del registro de eventos está limitado por el valor de configuración **MaxSize** o la cantidad de recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="8091c-116">The event log size is limited by either the **MaxSize** configuration value or the amount of system resources.</span></span>

    <span data-ttu-id="8091c-117">Cuando se alcanza el límite de tamaño del registro de eventos, puede comenzar el ajuste.</span><span class="sxs-lookup"><span data-stu-id="8091c-117">When the event log size limit is reached, it might start wrapping.</span></span> <span data-ttu-id="8091c-118">El ajuste se controla mediante el valor de configuración **retención** .</span><span class="sxs-lookup"><span data-stu-id="8091c-118">Wrapping is controlled by the **Retention** configuration value.</span></span> <span data-ttu-id="8091c-119">Para obtener más información sobre los valores de configuración del registro de eventos, vea [EventLog Key](eventlog-key.md).</span><span class="sxs-lookup"><span data-stu-id="8091c-119">For more information about the event log configuration values, see [Eventlog Key](eventlog-key.md).</span></span>

-   <span data-ttu-id="8091c-120">Envoltura.</span><span class="sxs-lookup"><span data-stu-id="8091c-120">Wrapping.</span></span> <span data-ttu-id="8091c-121">Los registros se organizan como un búfer circular.</span><span class="sxs-lookup"><span data-stu-id="8091c-121">The records are organized as a circular buffer.</span></span> <span data-ttu-id="8091c-122">A medida que se agregan nuevos registros, se reemplazan los registros más antiguos.</span><span class="sxs-lookup"><span data-stu-id="8091c-122">As new records are added, the oldest records are replaced.</span></span> <span data-ttu-id="8091c-123">La ubicación de los registros más antiguos y más recientes variará.</span><span class="sxs-lookup"><span data-stu-id="8091c-123">The location of the oldest and newest records will vary.</span></span> <span data-ttu-id="8091c-124">En el siguiente ejemplo se muestra el método de ajuste.</span><span class="sxs-lookup"><span data-stu-id="8091c-124">The following example shows the wrapping method.</span></span>

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

    <span data-ttu-id="8091c-125">En el ejemplo, el registro más antiguo ya no es 1, pero es 102 porque se ha sobrescrito el espacio de los registros 1 a 101.</span><span class="sxs-lookup"><span data-stu-id="8091c-125">In the example the oldest record is no longer 1, but is 102 because the space for records 1 to 101 was overwritten.</span></span>

    <span data-ttu-id="8091c-126">Hay cierto espacio entre el **registro de \_ EOF \_ de Elf** y el registro más antiguo, ya que el sistema borrará un número entero de registros para liberar espacio para el registro más reciente.</span><span class="sxs-lookup"><span data-stu-id="8091c-126">There is some space between the **ELF\_EOF\_RECORD** and the oldest record because the system will erase an integral number of records to free space for the newest record.</span></span> <span data-ttu-id="8091c-127">Por ejemplo, si el registro más reciente tiene 100 bytes de longitud y los dos registros más antiguos tienen una longitud de 75 bytes, el sistema quitará los dos registros más antiguos.</span><span class="sxs-lookup"><span data-stu-id="8091c-127">For example, if the newest record is 100 bytes long and the two oldest records are 75 bytes long, then the system will remove the two oldest records.</span></span> <span data-ttu-id="8091c-128">Los bytes adicionales 50 se utilizarán más adelante cuando se escriban nuevos registros.</span><span class="sxs-lookup"><span data-stu-id="8091c-128">The extra 50 bytes will be used later when new records are written.</span></span>

    <span data-ttu-id="8091c-129">Un archivo de registro de eventos tiene un tamaño fijo y, cuando se ajustan los registros del archivo, el registro situado al final del archivo se dividirá normalmente en dos registros.</span><span class="sxs-lookup"><span data-stu-id="8091c-129">An event log file has a fixed size and when the records in the file wrap, the record at the end of the file will typically be split into two records.</span></span> <span data-ttu-id="8091c-130">Por ejemplo, si la posición de la siguiente escritura es 100 bytes desde el final del archivo y el tamaño del registro es de 300 bytes, los primeros 100 bytes se escribirán al final del archivo y los siguientes 200 bytes se escribirán al principio del archivo inmediatamente después del **\_ \_ encabezado de registro Elf**.</span><span class="sxs-lookup"><span data-stu-id="8091c-130">For example, if the position for the next write is 100 bytes from the end of the file and the size of the record is 300 bytes, the first 100 bytes will be written at the end of the file and the next 200 bytes will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="8091c-131">Si el espacio disponible al final del archivo es menor que la parte fija del **EVENTLOGRECORD** (0x38 bytes), todo el registro nuevo se escribirá al principio del archivo inmediatamente después del encabezado del archivo de registro de **Elf \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="8091c-131">If the available space at the end of the file is less than the fixed portion of the **EVENTLOGRECORD** (0x38 bytes), all of the new record will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="8091c-132">Los bytes no usados al final del archivo se rellenarán con el patrón 0x00000027.</span><span class="sxs-lookup"><span data-stu-id="8091c-132">The unused bytes at the end of the file will be filled with the pattern 0x00000027.</span></span>

<span data-ttu-id="8091c-133">Para obtener más información y un ejemplo de código, vea [informar de un evento](reporting-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="8091c-133">For more information and a code example, see [Reporting an Event](reporting-an-event.md).</span></span>

 

 
