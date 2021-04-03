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
# <a name="monitoring-applications"></a>Supervisión de aplicaciones

Los elementos de la API de la biblioteca de administración de Intercambio dinámico de datos (DDEML) se pueden usar para crear una aplicación que supervise la actividad de Intercambio dinámico de datos (DDE) en el sistema. Al igual que cualquier aplicación DDEML, una aplicación de supervisión DDE contiene una función de devolución de llamada DDE. DDEML notifica a la función de devolución de llamada DDE de una aplicación de supervisión cada vez que se produce un evento DDE, pasando información sobre el evento a la función de devolución de llamada. Normalmente, la aplicación muestra la información en una ventana o la escribe en un archivo.

Para recibir notificaciones de DDEML, una aplicación se debe haber registrado como monitor DDE especificando la \_ marca de monitor APPCLASS en una llamada a la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . En esta misma llamada, la aplicación puede especificar una o más marcas de monitor para indicar los tipos de eventos para los que el método DDEML debe notificar a la función de devolución de llamada de la aplicación. Una aplicación puede especificar las marcas de supervisión siguientes:



| Marca          | Descripción                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_devoluciones de llamada MF | Notifica a la función de devolución de llamada cada vez que se envía una transacción a cualquier función de devolución de llamada DDE del sistema.                                                                                                                                           |
| MF \_ conv      | Notifica a la función de devolución de llamada cada vez que se establece o finaliza una conversación.                                                                                                                                                                |
| errores de MF \_    | Notifica a la función de devolución de llamada cada vez que se produce un error DDEML.                                                                                                                                                                                       |
| \_información de HSZ MF \_ | Notifica a la función de devolución de llamada cada vez que una aplicación DDEML crea, libera o incrementa el recuento de uso de un identificador de cadena o cada vez que se libera un identificador de cadena como resultado de una llamada a la función [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) . |
| \_vínculos MF     | Notifica a la función de devolución de llamada cada vez que se inicia o finaliza un bucle de notificación.                                                                                                                                                                         |
| MF \_ POSTMSGS  | Notifica a la función de devolución de llamada cada vez que el sistema o una aplicación envía un mensaje DDE.                                                                                                                                                           |
| MF \_ SENDMSGS  | Notifica a la función de devolución de llamada cada vez que el sistema o una aplicación envía un mensaje DDE.                                                                                                                                                           |



 

En el ejemplo siguiente se muestra cómo registrar una aplicación de supervisión DDE para que su función de devolución de llamada DDE reciba notificaciones de todos los eventos DDE.


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



El DDEML informa a una aplicación de supervisión de un evento DDE mediante el envío de una transacción del [**\_ monitor XTYP**](xtyp-monitor.md) a la función de devolución de llamada DDE de la aplicación. Durante esta transacción, DDEML pasa una marca de monitor que especifica el tipo de evento DDE que se ha producido y un identificador a un objeto DDE que contiene información detallada sobre el evento. DDEML proporciona un conjunto de estructuras que la aplicación puede usar para extraer la información del objeto DDE. Existe una estructura correspondiente para cada tipo de evento DDE.



| Estructura                                  | Descripción                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | Contiene información sobre una transacción.                         |
| [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | Contiene información acerca de una conversación.                        |
| [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | Contiene información acerca del error de DDE más reciente.                  |
| [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | Contiene información sobre un bucle de notificación.                        |
| [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | Contiene información sobre un identificador de cadena.                       |
| [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | Contiene información acerca de un mensaje DDE enviado o expuesto. |



 

En el ejemplo siguiente se muestra la función de devolución de llamada DDE de una aplicación de supervisión DDE que da formato a la información sobre cada evento de identificador de cadena y, a continuación, muestra la información en una ventana. La función utiliza la estructura [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) para extraer la información del objeto DDE.


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



 

 




