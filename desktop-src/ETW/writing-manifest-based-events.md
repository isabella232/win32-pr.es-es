---
description: Obtenga información sobre cómo escribir eventos basados en manifiestos en una sesión de seguimiento. Comience con el registro del proveedor para que esté listo para escribir eventos en una sesión de seguimiento.
ms.assetid: 76e7202e-74ce-40a3-a04b-9af5117fe20e
title: Escribir eventos basados en manifiestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6963051f65beb652eda04e3d0be6db99925e4eed81032c5687850915a0f1c173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151084"
---
# <a name="writing-manifest-based-events"></a>Escribir eventos basados en manifiestos

Para poder escribir eventos en una sesión de seguimiento, debe registrar el proveedor. El registro de un proveedor indica a ETW que el proveedor está listo para escribir eventos en una sesión de seguimiento. Un proceso puede registrar hasta 1024 GUID de proveedor; sin embargo, debe limitar el número de proveedores que registra el proceso a uno o dos.

**Antes de Windows Vista:** No hay ningún límite en el número de proveedores que un proceso puede registrar.

Para registrar un proveedor basado en manifiestos, llame a la [**función EventRegister.**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) La función registra el GUID del proveedor e identifica una devolución de llamada opcional a la que ETW llama cuando un controlador habilita o deshabilita el proveedor.

Antes de que se cierre el proveedor, llame a [**la función EventUnregister**](/windows/desktop/api/Evntprov/nf-evntprov-eventunregister) para quitar el registro del proveedor de ETW. La [**función EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) devuelve el identificador de registro que se pasa a la **función EventUnregister.**

[Los proveedores basados](about-event-tracing.md) en manifiestos no tienen que implementar una [**función EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback) para recibir notificaciones cuando una sesión habilita o deshabilita el proveedor. La devolución de llamada es opcional y se usa con fines informativos. no es necesario especificar ni implementar la devolución de llamada al registrar el proveedor. Un proveedor basado en manifiestos puede escribir simplemente eventos y ETW decidirá si el evento se registra en una sesión de seguimiento. Si un evento requiere que realice un trabajo exhaustivo para generar los datos del evento, puede llamar primero a las funciones [**EventEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventenabled) o [**EventProviderEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventproviderenabled) para comprobar que el evento se escribirá en una sesión antes de realizar el trabajo.

Normalmente, implementaría la devolución de llamada si el proveedor requiere que el controlador pase los datos de filtro definidos por el proveedor (vea el parámetro *FilterData* de [**EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback)) al proveedor o si el proveedor usa la información de contexto que especificó cuando se registró (vea el parámetro *CallbackContext* de [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister)).

[Los proveedores basados](about-event-tracing.md) en manifiestos llaman a [**la función EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) o [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) para escribir eventos en una sesión. Si los datos del evento son una cadena o si no define un manifiesto para el proveedor y los datos del evento son una sola cadena, llame a la [**función EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) para escribir el evento. Para los datos de eventos que contienen tipos de datos numéricos o complejos, llame a la [**función EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) para registrar el evento.

En el ejemplo siguiente se muestra cómo preparar los datos del evento que se escribirán mediante la [**función EventWrite.**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) En el ejemplo se hace referencia a los eventos definidos en [Publishing Your Event Schema for a Manifest-based Provider](publishing-your-event-schema-for-a-manifest-base-provider.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <evntprov.h>
#include "provider.h"  // Generated from manifest

#define SUNDAY     0X1
#define MONDAY     0X2
#define TUESDAY    0X4
#define WEDNESDAY  0X8
#define THURSDAY   0X10
#define FRIDAY     0X20
#define SATURDAY   0X40

enum TRANSFER_TYPE {
  Download = 1,
  Upload,
  UploadReply
};

#define MAX_NAMEDVALUES          5  // Maximum array size
#define MAX_PAYLOAD_DESCRIPTORS  9 + (2 * MAX_NAMEDVALUES)

typedef struct _namedvalue {
  LPWSTR name;
  USHORT value;
} NAMEDVALUE, *PNAMEDVALUE;

void wmain(void)
{
    DWORD status = ERROR_SUCCESS;
    REGHANDLE RegistrationHandle = NULL; 
    EVENT_DATA_DESCRIPTOR Descriptors[MAX_PAYLOAD_DESCRIPTORS]; 
    DWORD i = 0;

    // Data to load into event descriptors

    USHORT Scores[3] = {45, 63, 21};
    ULONG pImage = (ULONG)&Scores;
    DWORD TransferType = Upload;
    DWORD Day = MONDAY | TUESDAY;
    LPWSTR Path = L"c:\\path\\folder\\file.ext";
    BYTE Cert[11] = {0x2, 0x4, 0x8, 0x10, 0x20, 0x30, 0x40, 0x50, 0x60, 0x0, 0x1};
    PBYTE Guid = (PBYTE) &ProviderGuid;
    USHORT ArraySize = MAX_NAMEDVALUES;
    BOOL IsLocal = TRUE;
    NAMEDVALUE NamedValues[MAX_NAMEDVALUES] = { 
        {L"Bill", 1},
        {L"Bob", 2},
        {L"William", 3},
        {L"Robert", 4},
        {L"", 5}
        };

    status = EventRegister(
        &ProviderGuid,      // GUID that identifies the provider
        NULL,               // Callback not used
        NULL,               // Context noot used
        &RegistrationHandle // Used when calling EventWrite and EventUnregister
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"EventRegister failed with %lu\n", status);
        goto cleanup;
    }
  
    // Load the array of data descriptors for the TransferEvent event. 
    // Add the data to the array in the order of the <data> elements
    // defined in the event's template. 
   
    EventDataDescCreate(&Descriptors[i++], &pImage, sizeof(ULONG));
    EventDataDescCreate(&Descriptors[i++], Scores, sizeof(Scores));
    EventDataDescCreate(&Descriptors[i++], Guid, sizeof(GUID));
    EventDataDescCreate(&Descriptors[i++], Cert, sizeof(Cert));
    EventDataDescCreate(&Descriptors[i++], &IsLocal, sizeof(BOOL));
    EventDataDescCreate(&Descriptors[i++], Path, (ULONG)(wcslen(Path) + 1) * sizeof(WCHAR));
    EventDataDescCreate(&Descriptors[i++], &ArraySize, sizeof(USHORT));

    // If your event contains a structure, you should write each member
    // of the structure separately. If the structure contained integral data types
    // such as DWORDs and the data types were aligned on an 8-byte boundary, you 
    // could use the following call to write the structure, however, you are 
    // encouraged to write the members separately.
    //
    // EventDataDescCreate(&EvtData, struct, sizeof(struct));
    //
    // Because the array of structures in this example contains both strings 
    // and numbers, you must write each member of the structure separately.

    for (int j = 0; j < MAX_NAMEDVALUES; j++)
    {
        EventDataDescCreate(&Descriptors[i++], NamedValues[j].name, (ULONG)(wcslen(NamedValues[j].name)+1) * sizeof(WCHAR) );
        EventDataDescCreate(&Descriptors[i++], &(NamedValues[j].value), sizeof(USHORT) );
    }

    EventDataDescCreate(&Descriptors[i++], &Day, sizeof(DWORD));
    EventDataDescCreate(&Descriptors[i++], &TransferType, sizeof(DWORD));

    // Write the event. You do not have to verify if your provider is enabled before
    // writing the event. ETW will write the event to any session that enabled
    // the provider. If no session enabled the provider, the event is not 
    // written. If you need to perform extra work to write an event that you
    // would not otherwise do, you may want to call the EventEnabled function
    // before performing the extra work. The EventEnabled function tells you if a
    // session has enabled your provider, so you know if you need to perform the 
    // extra work or not.

    status = EventWrite(
        RegistrationHandle,              // From EventRegister
        &TransferEvent,                  // EVENT_DESCRIPTOR generated from the manifest
        (ULONG)MAX_PAYLOAD_DESCRIPTORS,  // Size of the array of EVENT_DATA_DESCRIPTORs
        &Descriptors[0]                  // Array of descriptors that contain the event data
        );

    if (status != ERROR_SUCCESS) 
    {
        wprintf(L"EventWrite failed with 0x%x", status);
    }

cleanup:

    EventUnregister(RegistrationHandle);
}
```



Cuando se compila el manifiesto (vea [Compilar](../wes/compiling-an-instrumentation-manifest.md)un manifiesto de instrumentación) que se usa en el ejemplo anterior, se crea el siguiente archivo de encabezado (al que se hace referencia en el ejemplo anterior).


```C++
//**********************************************************************`
//* This is an include file generated by Message Compiler.             *`
//*                                                                    *`
//* Copyright (c) Microsoft Corporation. All Rights Reserved.          *`
//**********************************************************************`
#pragma once
//+
// Provider Microsoft-Windows-ETWProvider Event Count 1
//+
EXTERN_C __declspec(selectany) const GUID ProviderGuid = {0xd8909c24, 0x5be9, 0x4502, {0x98, 0xca, 0xab, 0x7b, 0xdc, 0x24, 0x89, 0x9d}};
//
// Keyword
//
#define READ_KEYWORD 0x1
#define WRITE_KEYWORD 0x2
#define LOCAL_KEYWORD 0x4
#define REMOTE_KEYWORD 0x8

//
// Event Descriptors
//
EXTERN_C __declspec(selectany) const EVENT_DESCRIPTOR TransferEvent = {0x1, 0x0, 0x0, 0x4, 0x0, 0x0, 0x5};
#define TransferEvent_value 0x1
#define MSG_Provider_Name                    0x90000001L
#define MSG_Event_WhenToTransfer             0xB0000001L
#define MSG_Map_Download                     0xD0000001L
#define MSG_Map_Upload                       0xD0000002L
#define MSG_Map_UploadReply                  0xD0000003L
#define MSG_Map_Sunday                       0xF0000001L
#define MSG_Map_Monday                       0xF0000002L
#define MSG_Map_Tuesday                      0xF0000003L
#define MSG_Map_Wednesday                    0xF0000004L
#define MSG_Map_Thursday                     0xF0000005L
#define MSG_Map_Friday                       0xF0000006L
#define MSG_Map_Saturday                     0xF0000007L
```



 

 
