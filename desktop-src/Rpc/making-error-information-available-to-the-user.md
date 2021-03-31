---
title: Hacer que la información de error esté disponible para el usuario
description: Cuando un autor de llamada recibe un error y debe notificar al usuario sobre el error, se debe comprobar la presencia de información de error extendida y, si se encuentra, el llamador debe poner la información resultante a disposición del usuario.
ms.assetid: 18689280-7124-46e4-9341-ad8d0c1705db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18386dbebd443aced4f5680922549c0ecb0eba55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903913"
---
# <a name="making-error-information-available-to-the-user"></a>Hacer que la información de error esté disponible para el usuario

Cuando un autor de llamada recibe un error y debe notificar al usuario sobre el error, se debe comprobar la presencia de información de error extendida y, si se encuentra, el llamador debe poner la información resultante a disposición del usuario. El siguiente fragmento de código es un ejemplo de cómo hacer que esta información esté disponible para el usuario:


```C++
// Make an API
status = //...
if (status)
    {
    RPC_STATUS Status2;
    RPC_ERROR_ENUM_HANDLE EnumHandle;

    Status2 = RpcErrorStartEnumeration(&EnumHandle);
    if (Status2 == RPC_S_ENTRY_NOT_FOUND)
        {
        //...
        }
    else if (Status2 != RPC_S_OK)
        {
        PrintToConsole("Couldn't get EEInfo: %d\n", Status2);
        //...
        }
    else
        {
        RPC_EXTENDED_ERROR_INFO ErrorInfo;
        int Records;
        BOOL Result;
        BOOL CopyStrings = TRUE;
        BOOL fUseFileTime = TRUE;
        SYSTEMTIME *SystemTimeToUse;
        SYSTEMTIME SystemTimeBuffer;

        while (Status2 == RPC_S_OK)
            {
            ErrorInfo.Version = RPC_EEINFO_VERSION;
            ErrorInfo.Flags = 0;
            ErrorInfo.NumberOfParameters = 4;
            if (fUseFileTime)
                {
                ErrorInfo.Flags |= EEInfoUseFileTime;
                }

            Status2 = RpcErrorGetNextRecord(&EnumHandle, CopyStrings, &ErrorInfo);
            if (Status2 == RPC_S_ENTRY_NOT_FOUND)
                {
                break;
                }
            else if (Status2 != RPC_S_OK)
                {
                PrintToConsole("Couldn't finish enumeration: %d\n", Status2);
                break;
                }
            else
                {
                int i;

                if (ErrorInfo.ComputerName)
                    {
                    PrintToConsole("ComputerName is %S\n", ErrorInfo.ComputerName);
                    if (CopyStrings)
                        {
                        Result = HeapFree(GetProcessHeap(), 0, ErrorInfo.ComputerName);
                        ASSERT(Result);
                        }
                    }
                PrintToConsole("ProcessID is %d\n", ErrorInfo.ProcessID);
                if (fUseFileTime)
                    {
                    Result = FileTimeToSystemTime(&ErrorInfo.u.FileTime, 
                        &SystemTimeBuffer);
                    ASSERT(Result);
                    SystemTimeToUse = &SystemTimeBuffer;
                    }
                else
                    SystemTimeToUse = &ErrorInfo.u.SystemTime;

                PrintToConsole("System Time is: %d/%d/%d %d:%d:%d:%d\n", 
                    SystemTimeToUse->wMonth,
                    SystemTimeToUse->wDay,
                    SystemTimeToUse->wYear,
                    SystemTimeToUse->wHour,
                    SystemTimeToUse->wMinute,
                    SystemTimeToUse->wSecond,
                    SystemTimeToUse->wMilliseconds);
                PrintToConsole("Generating component is %d\n", 
                    ErrorInfo.GeneratingComponent);
                PrintToConsole("Status is %d\n", ErrorInfo.Status);
                PrintToConsole("Detection location is %d\n", 
                    (int)ErrorInfo.DetectionLocation);
                PrintToConsole("Flags is %d\n", ErrorInfo.Flags);
                PrintToConsole("NumberOfParameters is %d\n", 
                    ErrorInfo.NumberOfParameters);
                for (i = 0; i < ErrorInfo.NumberOfParameters; i ++)
                    {
                    switch(ErrorInfo.Parameters[i].ParameterType)
                        {
                        case eeptAnsiString:
                            PrintToConsole("Ansi string: %s\n", 
                                ErrorInfo.Parameters[i].u.AnsiString);
                            if (CopyStrings)
                                {
                                Result = HeapFree(GetProcessHeap(), 0, 
                                    ErrorInfo.Parameters[i].u.AnsiString);
                                ASSERT(Result);
                                }
                            break;

                        case eeptUnicodeString:
                            PrintToConsole("Unicode string: %S\n", 
                                ErrorInfo.Parameters[i].u.UnicodeString);
                            if (CopyStrings)
                                {
                                Result = HeapFree(GetProcessHeap(), 0, 
                                    ErrorInfo.Parameters[i].u.UnicodeString);
                                ASSERT(Result);
                                }
                            break;

                        case eeptLongVal:
                            PrintToConsole("Long val: %d\n", 
                                ErrorInfo.Parameters[i].u.LVal);
                            break;

                        case eeptShortVal:
                            PrintToConsole("Short val: %d\n", 
                                (int)ErrorInfo.Parameters[i].u.SVal);
                            break;

                        case eeptPointerVal:
                            PrintToConsole("Pointer val: %d\n", 
                                ErrorInfo.Parameters[i].u.PVal);
                            break;

                        case eeptNone:
                            PrintToConsole("Truncated\n");
                            break;

                        default:
                            PrintToConsole("Invalid type: %d\n", 
                                ErrorInfo.Parameters[i].ParameterType);
                        }
                    }
                }
            }
        RpcErrorEndEnumeration(&EnumHandle);
        }
    }
```



En este ejemplo, la información de error extendida se vuelca en la consola, pero el componente puede ponerla a disposición del usuario de cualquier otra manera. Si el componente decide guardar la información en el almacenamiento persistente y mostrarla más adelante, a menudo es más fácil usar el formato binario disponible mediante las llamadas a la función [**RpcErrorSaveErrorInfo**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorsaveerrorinfo) y [**RpcErrorLoadErrorInfo**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorloaderrorinfo) .

 

 




