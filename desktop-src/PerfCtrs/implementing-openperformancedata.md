---
description: La función OpenPerformanceData ofrece al proveedor la oportunidad de inicializar sus estructuras de datos de rendimiento.
ms.assetid: 0849d9cb-90d1-4b79-810d-b43f69cc9055
title: Implementación de OpenPerformanceData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f5e4f9860983066f6ce106638962415dcf71b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062895"
---
# <a name="implementing-openperformancedata"></a>Implementación de OpenPerformanceData

La [**función OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) ofrece al proveedor la oportunidad de inicializar sus estructuras de datos de rendimiento. El sistema llama a la función open la primera vez que un consumidor llama a [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)o si el consumidor usa la [**función RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) o [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) para abrir **HKEY \_ PERFORMANCE \_ DATA**.

En el ejemplo siguiente se muestra una implementación de la [**función OpenPerformanceData.**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) El archivo de encabezado que contiene la definición de los contadores usados en esta función sigue este ejemplo. Si usa C++ para implementar esta función, asegúrese de usar extern "C" al declarar la función. Las constantes de desplazamiento de contador usadas en este ejemplo se definen en el archivo CounterOffsets.h que se muestra en [Adding Counter Names and Description to the Registry](adding-counter-names-and-descriptions-to-the-registry.md).


```C++
#include "provider.h"


// Callback that the performance service calls once for each consumer that wants 
// to consume one or more of your counters. You can use this notification to 
// prepare the counter data structures and setup communications with the 
// application that is providing the actual performance data.
extern "C" DWORD APIENTRY OpenPerfData(LPWSTR pContext)
{
    DWORD FirstCounterIndex = 0;
    DWORD FirstHelpIndex = 0;
    DWORD DataSize = sizeof(DWORD);  // Used in the RegQueryValueEx call
    HKEY hkey;
    LONG rc = ERROR_SUCCESS;

    // Use g_OpenCount to prevent initializing the data more than once.
    
    if (g_OpenCount > 1)
    {
        goto cleanup;
    }

    // Retrieve the application specific context data
    // if you define an Export value under the 
    // HKLM\SYSTEM\CurrentControlSet\Services\MyProvider\Linkage key.
    // The context string is a REG_MULTI_SZ string.

    if (pContext)
    {
        for (; *pContext; pContext += (wcslen(pContext)+1))
        {
            // Do something with the string.
        }
    }

    // Retrieve the starting index values for your counters and help strings. You add 
    // your offset values (see Adding Counter Names and Descriptions to the Registry)
    // to these index values to determine your actual object and counter index values.

    rc = RegOpenKeyEx(HKEY_LOCAL_MACHINE, PERFORMANCE_REGISTRY_PATH, 0, KEY_READ, &hkey);
    if (ERROR_SUCCESS == rc)
    {
        rc = RegQueryValueEx(hkey, L"First Counter", NULL, NULL, (LPBYTE)&FirstCounterIndex, &DataSize);
        if (ERROR_SUCCESS == rc)
        {
            rc = RegQueryValueEx(hkey, L"First Help", NULL, NULL, (LPBYTE)&FirstHelpIndex, &DataSize);        
        }

        RegCloseKey(hkey);
    }

    // If you could not open the key or retrieve the value, exit.

    if (ERROR_SUCCESS != rc)
    {
        // If you return a non-success code, the service adds a Disable Performance 
        // Counters value to your Performance key to disable your provider.
        // Consider logging an event and returning success instead of failing.

        rc = ERROR_SUCCESS;
        goto cleanup;
    }

    // Initialize the Transfer object. This is a single instance object, so you can
    // initialize each member of the object and its counters.

    ZeroMemory(&g_Transfer, TransferSize);
    g_Transfer.Object.TotalByteLength = TransferSize;
    g_Transfer.Object.DefinitionLength = sizeof(PERF_OBJECT_TYPE) + 
        sizeof(PERF_COUNTER_DEFINITION) * NumberOfTransferCounters;
    g_Transfer.Object.HeaderLength = sizeof(PERF_OBJECT_TYPE);
    g_TransferIndex = FirstCounterIndex;
    g_Transfer.Object.ObjectNameTitleIndex = g_TransferIndex;
    g_Transfer.Object.ObjectHelpTitleIndex = FirstHelpIndex;
    g_Transfer.Object.DetailLevel = PERF_DETAIL_ADVANCED;
    g_Transfer.Object.NumCounters = NumberOfTransferCounters;
    g_Transfer.Object.DefaultCounter = -1;  // No default counter
    g_Transfer.Object.NumInstances = PERF_NO_INSTANCES;

    // Initialize the bytes sent counter.

    g_Transfer.BytesSentCounter.ByteLength = sizeof(PERF_COUNTER_DEFINITION);
    g_Transfer.BytesSentCounter.CounterNameTitleIndex = FirstCounterIndex + BYTES_SENT;
    g_Transfer.BytesSentCounter.CounterHelpTitleIndex = FirstHelpIndex + BYTES_SENT;
    g_Transfer.BytesSentCounter.DetailLevel = PERF_DETAIL_ADVANCED;
    g_Transfer.BytesSentCounter.CounterType = PERF_COUNTER_RAWCOUNT;
    g_Transfer.BytesSentCounter.CounterSize = sizeof(DWORD);
    g_Transfer.BytesSentCounter.CounterOffset = BytesSentOffset;

    // Initialize the available bandwidth counter.

    g_Transfer.AvailableBandwidthCounter.ByteLength = sizeof(PERF_COUNTER_DEFINITION);
    g_Transfer.AvailableBandwidthCounter.CounterNameTitleIndex = FirstCounterIndex + AVAILABLE_BANDWIDTH;
    g_Transfer.AvailableBandwidthCounter.CounterHelpTitleIndex = FirstHelpIndex + AVAILABLE_BANDWIDTH;
    g_Transfer.AvailableBandwidthCounter.DetailLevel = PERF_DETAIL_ADVANCED;
    g_Transfer.AvailableBandwidthCounter.CounterType = PERF_RAW_FRACTION;
    g_Transfer.AvailableBandwidthCounter.CounterSize = sizeof(DWORD);
    g_Transfer.AvailableBandwidthCounter.CounterOffset = AvailableBandwidthOffset;

    // Initialize the total bandwidth counter. This is a base counter for the
    // available bandwidth counter. You do not specify index values for base counters.

    g_Transfer.TotalBandwidthBaseCounter.ByteLength = sizeof(PERF_COUNTER_DEFINITION);
    g_Transfer.TotalBandwidthBaseCounter.CounterType = PERF_RAW_BASE;
    g_Transfer.TotalBandwidthBaseCounter.CounterSize = sizeof(DWORD);
    g_Transfer.TotalBandwidthBaseCounter.CounterOffset = TotalBandwidthBaseOffset;

    // Specify the size of the counter block which contains the raw counter values. 

    g_Transfer.CounterBlock.ByteLength = EndOfTransferData;

    // Initialize the Peer object. This is a multiple instance object. You cannot 
    // initialize all members of the Peer object because you do not know how 
    // many instances there will be until the object data is queried. You set 
    // the TotalByteLength and NumInstances members in the CollectPerfData function.

    ZeroMemory(&g_Peer, sizeof(PEER));
    g_Peer.Object.DefinitionLength = sizeof(PERF_OBJECT_TYPE) + 
        sizeof(PERF_COUNTER_DEFINITION) * NumberOfPeerCounters;
    g_Peer.Object.HeaderLength = sizeof(PERF_OBJECT_TYPE);
    g_PeerIndex = FirstCounterIndex + PEER_OBJECT;
    g_Peer.Object.ObjectNameTitleIndex = g_PeerIndex;
    g_Peer.Object.ObjectHelpTitleIndex = FirstHelpIndex + PEER_OBJECT;
    g_Peer.Object.DetailLevel = PERF_DETAIL_ADVANCED;
    g_Peer.Object.NumCounters = NumberOfPeerCounters;
    g_Peer.Object.DefaultCounter = -1;  // No default counter

    // Initialize the bytes served counter.

    g_Peer.BytesServedCounter.ByteLength = sizeof(PERF_COUNTER_DEFINITION);
    g_Peer.BytesServedCounter.CounterNameTitleIndex = FirstCounterIndex + BYTES_SERVED;
    g_Peer.BytesServedCounter.CounterHelpTitleIndex = FirstHelpIndex + BYTES_SERVED;
    g_Peer.BytesServedCounter.DetailLevel = PERF_DETAIL_ADVANCED;
    g_Peer.BytesServedCounter.CounterType = PERF_COUNTER_RAWCOUNT;
    g_Peer.BytesServedCounter.CounterSize = sizeof(DWORD);
    g_Peer.BytesServedCounter.CounterOffset = BytesServedOffset;

    InterlockedIncrement(&g_OpenCount);  // Decremented in ClosePerfData

cleanup:
    
    return rc;
}
```



A continuación se muestra el archivo de encabezado usado en este ejemplo.


```C++
#ifndef _PROVIDER_H
#define _PROVIDER_H

#include <windows.h>
#include <strsafe.h>
#include "CounterOffsets.h"

extern "C" DWORD APIENTRY OpenPerfData(LPWSTR pContext);
extern "C" DWORD APIENTRY CollectPerfData(LPWSTR pQuery, PVOID* ppData, LPDWORD pcbData, LPDWORD pObjectsReturned);
extern "C" DWORD APIENTRY ClosePerfData();
BOOL IsQuerySupported(LPWSTR pQuery, DWORD* pQueriedObjects);
DWORD GetQuerySize(DWORD QueriedObjects);

// Define the Transfer counter object. This object is a single 
// instance counter object, so you can define it completely.
typedef struct _transfer 
{
    PERF_OBJECT_TYPE Object;
    PERF_COUNTER_DEFINITION BytesSentCounter;
    PERF_COUNTER_DEFINITION AvailableBandwidthCounter;
    PERF_COUNTER_DEFINITION TotalBandwidthBaseCounter;
    PERF_COUNTER_BLOCK CounterBlock;
    DWORD BytesSentData;
    DWORD AvailableBandwidthData;
    DWORD TotalBandwidthData;
} TRANSFER, *PTRANSFER;

// Define offsets to counter data
#define BytesSentOffset sizeof(PERF_COUNTER_BLOCK)
#define AvailableBandwidthOffset BytesSentOffset + sizeof(DWORD)
#define TotalBandwidthBaseOffset AvailableBandwidthOffset + sizeof(DWORD)
#define EndOfTransferData TotalBandwidthBaseOffset + sizeof(DWORD)
#define TransferSize sizeof(TRANSFER)

#define NumberOfTransferCounters 3

#define MAX_INSTANCE_NAME_LEN 15 

// Define the Peer counter object. This object is a multiple
// instance object, so you must define the object and instances
// separately.
typedef struct _peer {
  PERF_OBJECT_TYPE Object;
  PERF_COUNTER_DEFINITION BytesServedCounter;
} PEER, *PPEER;

typedef struct _peerinstance {
  PERF_INSTANCE_DEFINITION Instance;
  WCHAR InstanceName[MAX_INSTANCE_NAME_LEN+1];
  PERF_COUNTER_BLOCK CounterBlock;
  DWORD BytesServedData;
} PEER_INSTANCE, *PPEER_INSTANCE;

#define BytesServedOffset sizeof(PERF_COUNTER_BLOCK)
#define EndOfPeerData BytesServedOffset + sizeof(DWORD)
#define NumberOfPeerCounters 1

// For this example, the instances are static, so predefine the names.
#define INSTANCE_NAME_1 L"Peer 1"
#define INSTANCE_NAME_2 L"Peer 2"
#define PERFORMANCE_REGISTRY_PATH L"SYSTEM\\CurrentControlSet\\Services\\MyApplication\\Performance"

typedef enum _queriedflags { 
  QUERIED_TRANSFER_OBJECT = 1,
  QUERIED_PEER_OBJECT = 2,
  QUERIED_ALL_OBJECTS = 0xFFFF
} QUERIED_FLAGS;

//Globals
TRANSFER g_Transfer;             // Transfer object
PEER g_Peer;                     // Peer object
DWORD g_TransferIndex = 0;       // Index value for the Transfer object
DWORD g_PeerIndex = 0;           // Index value for the Peer object
DWORD g_QueriedObjects = 0;      // Objects that were queried
UNALIGNED LONG g_OpenCount = 0;  // Reference count for the number of times
                                 // that OpenPerfData is called.
#endif
```



En el ejemplo siguiente se muestra el archivo de definición de módulo (.def) utilizado para exportar las funciones open, collect y close.


```C++
LIBRARY    "PerfProvider"

EXPORTS
    OpenPerfData    @1
    CollectPerfData    @2
    ClosePerfData    @3
```



En el ejemplo siguiente se muestra una implementación de la [*función ClosePerformanceData.*](/windows/win32/api/winperf/nc-winperf-pm_close_proc) El sistema llama a la función close cuando un consumidor llama a [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) para cerrar **HKEY \_ PERFORMANCE \_ DATA**. Los proveedores usan esta llamada para liberar los recursos que han asignado.


```C++
// Callback that the performance service calls once for each consumer that has
// finished consuming your performance counters. Cleanup any resources that 
// you allocated for your performance counters.
extern "C" DWORD APIENTRY ClosePerfData(void)
{
    if (g_OpenCount > 0)
    {
        InterlockedDecrement(&g_OpenCount);
    }

    return ERROR_SUCCESS;
}
```



 

 
