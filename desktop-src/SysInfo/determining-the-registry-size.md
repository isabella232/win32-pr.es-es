---
description: En Windows 2000, es habitual que una utilidad de instalación compruebe el tamaño actual y máximo del registro para determinar si hay suficiente espacio disponible para los nuevos datos que va a agregar.
ms.assetid: 87e7b9de-d571-41e4-817e-29023546e9bd
title: Determinar el tamaño del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4434b519625cf21c9e0076dc7c21d71e27c01778
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371900"
---
# <a name="determining-the-registry-size"></a>Determinar el tamaño del Registro

En Windows 2000, es habitual que una utilidad de instalación compruebe el tamaño actual y máximo del registro para determinar si hay suficiente espacio disponible para los nuevos datos que va a agregar. En este ejemplo se muestra cómo hacerlo mediante programación mediante el contador de rendimiento "% de cuota del Registro en uso" dentro del objeto System.

En el ejemplo siguiente se usa el asistente de datos de rendimiento (PDH) para obtener el valor del contador; debe estar vinculado a Pdh.lib. PDH es un conjunto de API de alto nivel que se usa para obtener datos de rendimiento.

> [!Note]  
> No es necesario implementar esta comprobación de tamaño del Registro en Windows Server 2003 o Windows XP porque no tienen un límite de cuota del Registro.

 


```C++
//*******************************************************************
// 
//  Determines the current and maximum registry size.
//
//*******************************************************************

#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <pdh.h>

PDH_STATUS GetRegistrySize( LPTSTR szMachineName, 
    LPDWORD lpdwCurrentSize, LPDWORD lpdwMaximumSize );

//*******************************************************************
// 
//  Entry point for the program. This function demonstrates how to
//  use the GetRegistrySize function implemented below.
// 
//  It will use the first argument, if present, as the name of the
//  computer whose registry you wish to determine. If unspecified,
//  it will use the local computer.
//*******************************************************************

int _tmain( int argc, TCHAR *argv[] ) 
{

    LPTSTR      szMachineName  = NULL;
    PDH_STATUS  pdhStatus      = 0;
    DWORD       dwCurrent      = 0;
    DWORD       dwMaximum      = 0;

    // Allow a computer name to be specified on the command line.
    if ( argc > 1 )
        szMachineName = argv[1];

    // Get the registry size.
    pdhStatus=GetRegistrySize(szMachineName, &dwCurrent, &dwMaximum);

    // Print the results.
    if ( pdhStatus == ERROR_SUCCESS ) 
    {
        _tprintf( TEXT("Registry size: %ld bytes\n"), dwCurrent );
        _tprintf( TEXT("Max registry size: %ld bytes\n"), dwMaximum );

    } 
    else 
    {
        // If the operation failed, print the PDH error message.
        LPTSTR szMessage = NULL;

        FormatMessage( FORMAT_MESSAGE_ALLOCATE_BUFFER |
            FORMAT_MESSAGE_FROM_HMODULE,
            GetModuleHandle( TEXT("PDH.DLL") ), pdhStatus,
            MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
            szMessage, 0, NULL );

        _tprintf( TEXT("GetRegistrySize failed:  %s"), szMessage );

        LocalFree( szMessage );
    }

    return 0;
}

//*******************************************************************
// 
//  Retrieves the current and maximum registry size. It gets this
//  information from the raw counter values for the "% Registry Quota 
//  In Use" performance counter within the System object.
// 
//  PARAMETERS:   
//      szMachineName - Null-terminated string that specifies the
//          name of the computer whose registry you wish to query.
//          If this parameter is NULL, the local computer is used.
// 
//      lpdwCurrentSize - Receives the current registry size.
// 
//      lpdwMaximumSize - Receives the maximum registry size.
// 
//  RETURN VALUE: 
//      ERROR_SUCCESS if successful. Otherwise, the function
//      returns a PDH error code. These error codes can be
//      found in PDHMSG.H. A textual error message can be
//      retrieved from PDH.DLL using the FormatMessage function.
// 
//******************************************************************

PDH_STATUS GetRegistrySize( LPTSTR szMachineName, 
    LPDWORD lpdwCurrentSize, LPDWORD lpdwMaximumSize ) 
{
    PDH_STATUS  pdhResult   = 0;
    TCHAR       szCounterPath[1024];
    DWORD       dwPathSize  = 1024;
    PDH_COUNTER_PATH_ELEMENTS pe;
    PDH_RAW_COUNTER pdhRawValues;
    HQUERY      hQuery      = NULL;
    HCOUNTER    hCounter    = NULL;
    DWORD       dwType      = 0;

    // Open PDH query
    pdhResult = PdhOpenQuery( NULL, 0, &hQuery );
    if ( pdhResult != ERROR_SUCCESS )
        return pdhResult;

    __try 
    {
        // Create counter path
        pe.szMachineName     = szMachineName;
        pe.szObjectName      = TEXT("System");
        pe.szInstanceName    = NULL;
        pe.szParentInstance  = NULL;
        pe.dwInstanceIndex   = 1;
        pe.szCounterName     = TEXT("% Registry Quota In Use");

        pdhResult = PdhMakeCounterPath( &pe, szCounterPath, 
            &dwPathSize, 0 );
        if ( pdhResult != ERROR_SUCCESS )
            __leave;

        // Add the counter to the query
        pdhResult=PdhAddCounter(hQuery, szCounterPath, 0, &hCounter);
        if ( pdhResult != ERROR_SUCCESS ) 
            __leave;

        // Run the query to collect the performance data
        pdhResult = PdhCollectQueryData( hQuery );
        if ( pdhResult != ERROR_SUCCESS ) 
            __leave;

        // Retrieve the raw counter data:
        //    The dividend (FirstValue) is the current registry size
        //    The divisor (SecondValue) is the maximum registry size
        ZeroMemory( &pdhRawValues, sizeof(pdhRawValues) );
        pdhResult = PdhGetRawCounterValue( hCounter, &dwType,
            &pdhRawValues );
        if ( pdhResult != ERROR_SUCCESS )
            __leave;

        // Store the sizes in variables.
        if ( lpdwCurrentSize )
            *lpdwCurrentSize = (DWORD) pdhRawValues.FirstValue;
         
        if ( lpdwMaximumSize )
            *lpdwMaximumSize = (DWORD) pdhRawValues.SecondValue;

    } 
    __finally 
    {
        // Close the query
        PdhCloseQuery( hQuery );
    }

    return 0;
}
```



 

 



