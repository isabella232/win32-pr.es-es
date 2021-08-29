---
title: Creación de un adaptador de sensor
description: Estructura básica de un complemento de adaptador de sensor implementado como biblioteca de vínculos dinámicos (DLL) de C++.
ms.assetid: 4e78f0c2-177c-4e69-8bb6-c548a6f1ac46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ab84a32f69bfcef418ae8b5fa70bd8b9d093d4b76691e8b074088da99917b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993825"
---
# <a name="creating-a-sensor-adapter"></a>Creación de un adaptador de sensor

En el ejemplo de código siguiente se muestra la estructura básica de un complemento de adaptador de sensor implementado como una biblioteca de vínculos dinámicos (DLL) de C++. Para ver las implementaciones de pseudocódigo de cada función pública en el archivo DLL, vaya a [Funciones del adaptador de sensor](sensor-adapter-functions.md). Si decide no proporcionar funcionalidad para una función determinada, debe definir un código auxiliar para ella y devolver E \_ NOTIMPL.

> [!Note]  
> Se pueden crear adaptadores de sensor para las cámaras para la identificación de iris. Para la huella digital, use la solución de sensor de bandeja de entrada, disponible para los usuarios finales en Configuración. Las personalizaciones no están disponibles para el adaptador del sensor de huella digital.

 

``` syntax
C++
/*++
 
    THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
    ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
    THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
    PARTICULAR PURPOSE.

    Copyright (C) Microsoft. All rights reserved.

Module Name:

    SensorAdapter.cpp

Abstract:

    This module contains a stub implementation of a Sensor Adapter
    plug-in for the Windows Biometric service.


    -

Environment:

    Win32, user mode only.

Revision History:

NOTES:

    (None)

--*/

//////////////////////////////////////////////////////////////////////////////////////////
//
// Header files.
//
#include <Stdio.h>
#include <Tchar.h>
#include <Windows.h>
#include <Winbio_adapter.h>
#include <Winbio_ioctl.h>   // From the WDK
#include "SensorAdapter.h"


//////////////////////////////////////////////////////////////////////////////////////////
//
// Forward declarations for the sensor adapter interface routines.
//
static HRESULT
WINAPI
SensorAdapterAttach(
    __inout PWINBIO_PIPELINE Pipeline
    );

static HRESULT
WINAPI
SensorAdapterDetach(
    __inout PWINBIO_PIPELINE Pipeline
    );

static HRESULT
WINAPI
SensorAdapterClearContext(
    __inout PWINBIO_PIPELINE Pipeline
    );

static HRESULT
WINAPI
SensorAdapterQueryStatus(
    __inout PWINBIO_PIPELINE Pipeline,
    __out WINBIO_SENSOR_STATUS *Status
    );

static HRESULT
WINAPI
SensorAdapterReset(
    __inout PWINBIO_PIPELINE Pipeline
    );

static HRESULT
WINAPI
SensorAdapterSetMode(
    __inout PWINBIO_PIPELINE Pipeline,
    __in WINBIO_SENSOR_MODE Mode
    );

static HRESULT
WINAPI
SensorAdapterSetIndicatorStatus(
    __inout PWINBIO_PIPELINE Pipeline,
    __in WINBIO_INDICATOR_STATUS IndicatorStatus
    );

static HRESULT
WINAPI
SensorAdapterGetIndicatorStatus(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PWINBIO_INDICATOR_STATUS IndicatorStatus
    );

static HRESULT 
WINAPI
SensorAdapterStartCapture(
    __inout PWINBIO_PIPELINE Pipeline,
    __in WINBIO_BIR_PURPOSE Purpose,
    __out LPOVERLAPPED *Overlapped
    );

static HRESULT
WINAPI
SensorAdapterFinishCapture(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PWINBIO_REJECT_DETAIL RejectDetail
    );

static HRESULT
WINAPI
SensorAdapterExportSensorData(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PWINBIO_BIR *SampleBuffer,
    __out SIZE_T *SampleSize
    );

static HRESULT
WINAPI
SensorAdapterCancel(
    __inout PWINBIO_PIPELINE Pipeline
    );

static HRESULT
WINAPI
SensorAdapterPushDataToEngine(
    __inout PWINBIO_PIPELINE Pipeline,
    __in WINBIO_BIR_PURPOSE Purpose,
    __in WINBIO_BIR_DATA_FLAGS Flags,
    __out WINBIO_REJECT_DETAIL *RejectDetail
    );

static HRESULT
WINAPI
SensorAdapterControlUnit(
    __inout PWINBIO_PIPELINE Pipeline,
    __in ULONG ControlCode,
    __in_bcount(SendBufferSize) PUCHAR SendBuffer,
    __in SIZE_T SendBufferSize,
    __in_bcount(ReceiveBufferSize) PUCHAR ReceiveBuffer,
    __in SIZE_T ReceiveBufferSize,
    __out SIZE_T *ReceiveDataSize,
    __out ULONG *OperationStatus
    );

static HRESULT
WINAPI
SensorAdapterControlUnitPrivileged(
    __inout PWINBIO_PIPELINE Pipeline,
    __in ULONG ControlCode,
    __in_bcount(SendBufferSize) PUCHAR SendBuffer,
    __in SIZE_T SendBufferSize,
    __in_bcount(ReceiveBufferSize) PUCHAR ReceiveBuffer,
    __in SIZE_T ReceiveBufferSize,
    __out SIZE_T *ReceiveDataSize,
    __out ULONG *OperationStatus
    );


//////////////////////////////////////////////////////////////////////////////////////////
//
// Interface dispatch table
//
static WINBIO_SENSOR_INTERFACE g_SensorInterface = {
    WINBIO_STORAGE_INTERFACE_VERSION_1,
    WINBIO_ADAPTER_TYPE_SENSOR,
    sizeof(WINBIO_SENSOR_INTERFACE),
    {0xf6012694, 0xbed2, 0x4223, {0x81, 0xee, 0xf0, 0x7b, 0x44, 0xf0, 0x69, 0x13}},

    SensorAdapterAttach,
    SensorAdapterDetach,
    SensorAdapterClearContext,
    SensorAdapterQueryStatus,
    SensorAdapterReset,
    SensorAdapterSetMode,
    SensorAdapterSetIndicatorStatus,
    SensorAdapterGetIndicatorStatus,
    SensorAdapterStartCapture,
    SensorAdapterFinishCapture,
    SensorAdapterExportSensorData,
    SensorAdapterCancel,
    SensorAdapterPushDataToEngine,
    SensorAdapterControlUnit,
    SensorAdapterControlUnitPrivileged
};

//////////////////////////////////////////////////////////////////////////////////////////
//
// Mandatory DLL entry point function.
//
BOOL APIENTRY 
DllMain( 
    HANDLE ModuleHandle, 
    DWORD ReasonForCall, 
    LPVOID Reserved
    )
{
    UNREFERENCED_PARAMETER(ModuleHandle);
    UNREFERENCED_PARAMETER(ReasonForCall);
    UNREFERENCED_PARAMETER(Reserved);
    return TRUE;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// Well known interface discovery function exported by the Sensor Adapter.
//
HRESULT
WINAPI
WbioQuerySensorInterface(
    __out PWINBIO_SENSOR_INTERFACE *SensorInterface
    )
{
    *SensorInterface = &g_SensorInterface;
    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// Required routines.
//      This sample adapter assumes that the following three inline functions 
//      are declared in the private sensor adapter header file. The first two
//      perform memory management. The third normalizes error codes.
//
inline
PVOID
_AdapterAlloc(
    __in SIZE_T ByteCount
    )
{
    return HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, ByteCount);
}

inline
VOID
_AdapterRelease(
    __in PVOID Address
    )
{
    HeapFree(GetProcessHeap(), 0, Address);
}

inline HRESULT
_AdapterGetHresultFromWin32(
    __in DWORD Error
    )
{
    if ((Error == ERROR_CANCELLED) ||
        (Error == ERROR_OPERATION_ABORTED))
    {
        return WINBIO_E_CANCELED;
    }
    else
    {
        return WINBIO_E_DEVICE_FAILURE;
    }
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterAttach
//
// Purpose:
//      Performs any initialization required for later biometric operations.
//
static HRESULT
WINAPI
SensorAdapterAttach(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    
    // See the SensorAdapterAttach documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterDetach
//
// Purpose:
//      Cancels all pending sensor operations.
//      
static HRESULT
WINAPI
SensorAdapterDetach(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    
    // See the SensorAdapterDetach documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterClearContext
//
// Purpose:
//      Prepare the processing pipeline for a new operation. This function 
//      should flush temporary data from the sensor context and place the 
//      sensor adapter into a well-defined initial state.
//      
static HRESULT
WINAPI
SensorAdapterClearContext(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    
    // See the SensorAdapterClearContext documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterQueryStatus
//
// Purpose:
//      Retrieves information about the current status of the sensor device.
//      
static HRESULT
WINAPI
SensorAdapterQueryStatus(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PWINBIO_SENSOR_STATUS Status
    )
{
    
    // See the SensorAdapterQueryStatus documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterReset
//
// Purpose:
//      Reinitialize the sensor.
//      
static HRESULT
WINAPI
SensorAdapterReset(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    
    // See the SensorAdapterReset documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterSetMode
//
// Purpose:
//      Sets the sensor adapter mode.
//      
static HRESULT
WINAPI
SensorAdapterSetMode(
    __inout PWINBIO_PIPELINE Pipeline,
    __in WINBIO_SENSOR_MODE Mode
    )
{
    
    // See the SensorAdapterSetMode documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterSetIndicatorStatus
//
// Purpose:
//      Toggles the sensor indicator on or off.
//      
static HRESULT
WINAPI
SensorAdapterSetIndicatorStatus(
    __inout PWINBIO_PIPELINE Pipeline,
    __in WINBIO_INDICATOR_STATUS IndicatorStatus
     )
{
    
    // See the SensorAdapterSetIndicatorStatus documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterGetIndicatorStatus
//
// Purpose:
//      Retrieves a value that indicates whether the sensor indicator is 
//      on or off.
//      
static HRESULT
WINAPI
SensorAdapterGetIndicatorStatus(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PWINBIO_INDICATOR_STATUS IndicatorStatus
    )
{
    
    // See the SensorAdapterGetIndicatorStatus documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterStartCapture
//
// Purpose:
//      Begins an asynchronous biometric capture.
//      
static HRESULT 
WINAPI
SensorAdapterStartCapture(
    __inout PWINBIO_PIPELINE Pipeline,
    __in WINBIO_BIR_PURPOSE Purpose,
    __out LPOVERLAPPED *Overlapped
    )
{
    
    // See the SensorAdapterStartCapture documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterFinishCapture
//
// Purpose:
//      Waits for the completion of a capture operation initiated by the 
//      SensorAdapterStartCapture function.
//      
static HRESULT
WINAPI
SensorAdapterFinishCapture(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PWINBIO_REJECT_DETAIL RejectDetail
    )
{
    
    // See the SensorAdapterFinishCapture documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterExportSensorData
//
// Purpose:
//      Retrieves a copy of the most recently captured biometric sample.
//      
static HRESULT
WINAPI
SensorAdapterExportSensorData(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PWINBIO_BIR *SampleBuffer,
    __out SIZE_T *SampleSize
    )
{
    
    // See the SensorAdapterExportSensorData documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterCancel
//
// Purpose:
//      Cancels all pending sensor operations.
//      
static HRESULT
WINAPI
SensorAdapterCancel(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    
    // See the SensorAdapterCancel documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterPushDataToEngine
//
// Purpose:
//      Makes the current contents of the sample buffer available to the 
//      engine adapter.
//      
static HRESULT
WINAPI
SensorAdapterPushDataToEngine(
    __inout PWINBIO_PIPELINE Pipeline,
    __in WINBIO_BIR_PURPOSE Purpose,
    __in WINBIO_BIR_DATA_FLAGS Flags,
    __out PWINBIO_REJECT_DETAIL RejectDetail
    )
{
    
    // See the SensorAdapterPushDataToEngine documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterControlUnit
//
// Purpose:
//      Performs a vendor-defined control operation that does not require 
//      elevated privilege.
//
static HRESULT
WINAPI
SensorAdapterControlUnit(
    __inout PWINBIO_PIPELINE Pipeline,
    __in ULONG ControlCode,
    __in_bcount(SendBufferSize) PUCHAR SendBuffer,
    __in SIZE_T SendBufferSize,
    __in_bcount(ReceiveBufferSize) PUCHAR ReceiveBuffer,
    __in SIZE_T ReceiveBufferSize,
    __out SIZE_T *ReceiveDataSize,
    __out ULONG *OperationStatus
    )
{
    
    // See the SensorAdapterControlUnit documentation for an implementation example.

    return S_OK;
}

//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterControlUnitPrivileged
//
// Purpose:
//      Performs a vendor-defined control operation that requires elevated 
//      privilege.
//
static HRESULT
WINAPI
SensorAdapterControlUnitPrivileged(
    __inout PWINBIO_PIPELINE Pipeline,
    __in ULONG ControlCode,
    __in_bcount(SendBufferSize) PUCHAR SendBuffer,
    __in SIZE_T SendBufferSize,
    __in_bcount(ReceiveBufferSize) PUCHAR ReceiveBuffer,
    __in SIZE_T ReceiveBufferSize,
    __out SIZE_T *ReceiveDataSize,
    __out ULONG *OperationStatus
    )
{
    
    // See the SensorAdapterControlUnitPrivileged documentation for an implementation example.

    return S_OK;
}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear complementos de adaptador](creating-adapter-plug-ins.md)
</dt> </dl>

 

 




