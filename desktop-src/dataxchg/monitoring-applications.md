---
title: Supervisión de aplicaciones
description: En este tema se describe cómo se pueden usar los elementos de la biblioteca de administración de Intercambio dinámico de datos para crear una aplicación que supervise la actividad de intercambio dinámico de datos en el sistema.
ms.assetid: 6705dc8e-d1e9-4057-9fa2-42cd5cf818af
keywords:
- Interfaz de usuario de Windows, Intercambio dinámico de datos (DDE)
- Intercambio dinámico de datos (DDE), supervisar aplicaciones
- DDE (Intercambio dinámico de datos), supervisar aplicaciones
- intercambio de datos, Intercambio dinámico de datos (DDE)
- Interfaz de usuario de Windows, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), supervisar aplicaciones
- DDEML (biblioteca de administración de Intercambio dinámico de datos), supervisar aplicaciones
- intercambio de datos, biblioteca de administración de Intercambio dinámico de datos (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f75685d4caa15e519485b2d8b37983faa35366
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075465"
---
# <a name="monitoring-applications"></a><span data-ttu-id="8b3d6-111">Supervisión de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8b3d6-111">Monitoring Applications</span></span>

<span data-ttu-id="8b3d6-112">Los elementos de la API de la biblioteca de administración de Intercambio dinámico de datos (DDEML) se pueden usar para crear una aplicación que supervise la actividad de Intercambio dinámico de datos (DDE) en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-112">The API elements of the Dynamic Data Exchange Management Library (DDEML) can be used to create an application that monitors Dynamic Data Exchange (DDE) activity in the system.</span></span> <span data-ttu-id="8b3d6-113">Al igual que cualquier aplicación DDEML, una aplicación de supervisión DDE contiene una función de devolución de llamada DDE.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-113">Like any DDEML application, a DDE monitoring application contains a DDE callback function.</span></span> <span data-ttu-id="8b3d6-114">DDEML notifica a la función de devolución de llamada DDE de una aplicación de supervisión cada vez que se produce un evento DDE, pasando información sobre el evento a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-114">The DDEML notifies a monitoring application's DDE callback function whenever a DDE event occurs, passing information about the event to the callback function.</span></span> <span data-ttu-id="8b3d6-115">Normalmente, la aplicación muestra la información en una ventana o la escribe en un archivo.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-115">The application typically displays the information in a window or writes it to a file.</span></span>

<span data-ttu-id="8b3d6-116">Para recibir notificaciones de DDEML, una aplicación se debe haber registrado como monitor DDE especificando la \_ marca de monitor APPCLASS en una llamada a la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="8b3d6-116">To receive notifications from the DDEML, an application must have registered as a DDE monitor by specifying the APPCLASS\_MONITOR flag in a call to the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="8b3d6-117">En esta misma llamada, la aplicación puede especificar una o más marcas de monitor para indicar los tipos de eventos para los que el método DDEML debe notificar a la función de devolución de llamada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-117">In this same call, the application can specify one or more monitor flags to indicate the types of events for which the DDEML is to notify the application's callback function.</span></span> <span data-ttu-id="8b3d6-118">Una aplicación puede especificar las marcas de supervisión siguientes:</span><span class="sxs-lookup"><span data-stu-id="8b3d6-118">The following monitor flags can be specified by an application:</span></span>



| <span data-ttu-id="8b3d6-119">Marca</span><span class="sxs-lookup"><span data-stu-id="8b3d6-119">Flag</span></span>          | <span data-ttu-id="8b3d6-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b3d6-120">Description</span></span>                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3d6-121">\_devoluciones de llamada MF</span><span class="sxs-lookup"><span data-stu-id="8b3d6-121">MF\_CALLBACKS</span></span> | <span data-ttu-id="8b3d6-122">Notifica a la función de devolución de llamada cada vez que se envía una transacción a cualquier función de devolución de llamada DDE del sistema.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-122">Notifies the callback function whenever a transaction is sent to any DDE callback function in the system.</span></span>                                                                                                                                           |
| <span data-ttu-id="8b3d6-123">MF \_ conv</span><span class="sxs-lookup"><span data-stu-id="8b3d6-123">MF\_CONV</span></span>      | <span data-ttu-id="8b3d6-124">Notifica a la función de devolución de llamada cada vez que se establece o finaliza una conversación.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-124">Notifies the callback function whenever a conversation is established or terminated.</span></span>                                                                                                                                                                |
| <span data-ttu-id="8b3d6-125">errores de MF \_</span><span class="sxs-lookup"><span data-stu-id="8b3d6-125">MF\_ERRORS</span></span>    | <span data-ttu-id="8b3d6-126">Notifica a la función de devolución de llamada cada vez que se produce un error DDEML.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-126">Notifies the callback function whenever a DDEML error occurs.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="8b3d6-127">\_información de HSZ MF \_</span><span class="sxs-lookup"><span data-stu-id="8b3d6-127">MF\_HSZ\_INFO</span></span> | <span data-ttu-id="8b3d6-128">Notifica a la función de devolución de llamada cada vez que una aplicación DDEML crea, libera o incrementa el recuento de uso de un identificador de cadena o cada vez que se libera un identificador de cadena como resultado de una llamada a la función [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="8b3d6-128">Notifies the callback function whenever a DDEML application creates, frees, or increments the usage count of a string handle or whenever a string handle is freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> |
| <span data-ttu-id="8b3d6-129">\_vínculos MF</span><span class="sxs-lookup"><span data-stu-id="8b3d6-129">MF\_LINKS</span></span>     | <span data-ttu-id="8b3d6-130">Notifica a la función de devolución de llamada cada vez que se inicia o finaliza un bucle de notificación.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-130">Notifies the callback function whenever an advise loop is started or ended.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="8b3d6-131">MF \_ POSTMSGS</span><span class="sxs-lookup"><span data-stu-id="8b3d6-131">MF\_POSTMSGS</span></span>  | <span data-ttu-id="8b3d6-132">Notifica a la función de devolución de llamada cada vez que el sistema o una aplicación envía un mensaje DDE.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-132">Notifies the callback function whenever the system or an application posts a DDE message.</span></span>                                                                                                                                                           |
| <span data-ttu-id="8b3d6-133">MF \_ SENDMSGS</span><span class="sxs-lookup"><span data-stu-id="8b3d6-133">MF\_SENDMSGS</span></span>  | <span data-ttu-id="8b3d6-134">Notifica a la función de devolución de llamada cada vez que el sistema o una aplicación envía un mensaje DDE.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-134">Notifies the callback function whenever the system or an application sends a DDE message.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="8b3d6-135">En el ejemplo siguiente se muestra cómo registrar una aplicación de supervisión DDE para que su función de devolución de llamada DDE reciba notificaciones de todos los eventos DDE.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-135">The following example shows how to register a DDE monitoring application so that its DDE callback function receives notifications of all DDE events.</span></span>


```
DWORD idInst; 
PFNCALLBACK lpDdeProc; 
hInst = hInstance; 
 
if (DdeInitialize( 
        (LPDWORD) &idInst,  // instance identifier 
        DDECallback,        // pointer to callback function 
        APPCLASS_MONITOR |  // this is a monitoring application 
        MF_CALLBACKS     |  // monitor callback functions 
        MF_CONV          |  // monitor conversation data 
        MF_ERRORS        |  // monitor DDEML errors 
        MF_HSZ_INFO      |  // monitor data handle activity 
        MF_LINKS         |  // monitor advise loops 
        MF_POSTMSGS      |  // monitor posted DDE messages 
        MF_SENDMSGS,        // monitor sent DDE messages 
        0))                 // reserved 
{
    return FALSE; 
}
```



<span data-ttu-id="8b3d6-136">El DDEML informa a una aplicación de supervisión de un evento DDE mediante el envío de una transacción del [**\_ monitor XTYP**](xtyp-monitor.md) a la función de devolución de llamada DDE de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-136">The DDEML informs a monitoring application of a DDE event by sending an [**XTYP\_MONITOR**](xtyp-monitor.md) transaction to the application's DDE callback function.</span></span> <span data-ttu-id="8b3d6-137">Durante esta transacción, DDEML pasa una marca de monitor que especifica el tipo de evento DDE que se ha producido y un identificador a un objeto DDE que contiene información detallada sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-137">During this transaction, the DDEML passes a monitor flag that specifies the type of DDE event that has occurred and a handle to a DDE object that contains detailed information about the event.</span></span> <span data-ttu-id="8b3d6-138">DDEML proporciona un conjunto de estructuras que la aplicación puede usar para extraer la información del objeto DDE.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-138">The DDEML provides a set of structures that the application can use to extract the information from the DDE object.</span></span> <span data-ttu-id="8b3d6-139">Existe una estructura correspondiente para cada tipo de evento DDE.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-139">There is a corresponding structure for each type of DDE event.</span></span>



| <span data-ttu-id="8b3d6-140">Estructura</span><span class="sxs-lookup"><span data-stu-id="8b3d6-140">Structure</span></span>                                  | <span data-ttu-id="8b3d6-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b3d6-141">Description</span></span>                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="8b3d6-142">**MONCBSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="8b3d6-142">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | <span data-ttu-id="8b3d6-143">Contiene información sobre una transacción.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-143">Contains information about a transaction.</span></span>                         |
| [<span data-ttu-id="8b3d6-144">**MONCONVSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="8b3d6-144">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | <span data-ttu-id="8b3d6-145">Contiene información acerca de una conversación.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-145">Contains information about a conversation.</span></span>                        |
| [<span data-ttu-id="8b3d6-146">**MONERRSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="8b3d6-146">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | <span data-ttu-id="8b3d6-147">Contiene información acerca del error de DDE más reciente.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-147">Contains information about the latest DDE error.</span></span>                  |
| [<span data-ttu-id="8b3d6-148">**MONLINKSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="8b3d6-148">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | <span data-ttu-id="8b3d6-149">Contiene información sobre un bucle de notificación.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-149">Contains information about an advise loop.</span></span>                        |
| [<span data-ttu-id="8b3d6-150">**MONHSZSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="8b3d6-150">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | <span data-ttu-id="8b3d6-151">Contiene información sobre un identificador de cadena.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-151">Contains information about a string handle.</span></span>                       |
| [<span data-ttu-id="8b3d6-152">**MONMSGSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="8b3d6-152">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | <span data-ttu-id="8b3d6-153">Contiene información acerca de un mensaje DDE enviado o expuesto.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-153">Contains information about a DDE message that was sent or posted.</span></span> |



 

<span data-ttu-id="8b3d6-154">En el ejemplo siguiente se muestra la función de devolución de llamada DDE de una aplicación de supervisión DDE que da formato a la información sobre cada evento de identificador de cadena y, a continuación, muestra la información en una ventana.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-154">The following example shows the DDE callback function of a DDE monitoring application that formats information about each string handle event and then displays the information in a window.</span></span> <span data-ttu-id="8b3d6-155">La función utiliza la estructura [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) para extraer la información del objeto DDE.</span><span class="sxs-lookup"><span data-stu-id="8b3d6-155">The function uses the [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure to extract the information from the DDE object.</span></span>


```
HDDEDATA CALLBACK DDECallback(uType, uFmt, hconv, hsz1, hsz2, 
    hdata, dwData1, dwData2) 
UINT uType; 
UINT uFmt; 
HCONV hconv; 
HSZ hsz1; 
HSZ hsz2; 
HDDEDATA hdata; 
DWORD dwData1; 
DWORD dwData2; 
{ 
    LPVOID lpData; 
    CHAR *szAction; 
    CHAR szBuf[256]; 
    DWORD cb;
    HRESULT hResult; 
 
    switch (uType) 
    { 
        case XTYP_MONITOR: 
            // Obtain a pointer to the global memory object. 
 
            if (lpData = DdeAccessData(hdata, &cb)) 
            { 
                // Examine the monitor flag. 
 
                switch (dwData2) 
                { 
                    case MF_HSZ_INFO: 
 
#define PHSZS ((MONHSZSTRUCT *)lpData) 
 
                        // The global memory object contains 
                        // string handle data. Use the MONHSZSTRUCT 
                        // structure to access the data. 
 
                        switch (PHSZS->fsAction) 
                        { 
                            // Examine the action flags to determine
                            // the action performed on the handle.
 
                            case MH_CREATE: 
                                szAction = "Created"; 
                                break; 
 
                            case MH_KEEP: 
                                szAction = "Incremented"; 
                                break; 
 
                            case MH_DELETE: 
                                szAction = "Deleted"; 
                                break; 
 
                            case MH_CLEANUP: 
                                szAction = "Cleaned up"; 
                                break; 
 
                            default: 
                                DdeUnaccessData(hdata); 
                                return (HDDEDATA) 0; 
                        } 
 
                        // Write formatted output to a buffer. 
                        hResult = StringCchPrintf(szBuf, 256/sizeof(TCHAR),
                            "Handle %s, Task: %x, Hsz: %lx(%s)", 
                            (LPSTR) szAction, PHSZS->hTask, 
                            PHSZS->hsz, (LPSTR) PHSZS->str);
                        if (FAILED(hResult))
                        {
                        // TO DO: Write error handler.
                            return;
                        } 
                        // Display text or write to a file. 
 
                        break; 
 
#undef PHSZS 
 
                    // Process other MF_* flags. 
 
                    default: 
                        break; 
                } 
            } 
 
            // Free the global memory object. 
 
            DdeUnaccessData(hdata); 
            break; 
 
        default: 
            break; 
    } 
    return (HDDEDATA) 0; 
} 
```



 

 




