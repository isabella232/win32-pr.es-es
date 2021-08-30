---
description: Este código de ejemplo es de una acción personalizada de ICE (ICE01). Valida que el mecanismo ICE funciona mostrando la hora. El ICE publica un mensaje que indica la hora a la que el instalador llamó al ICE. Este ICE nunca debe devolver un error.
ms.assetid: 7e580f6b-8adf-4b11-9072-5b2e1506fabb
title: ICE de ejemplo en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1ddf7dc4f2e650086ee99610a666636cdf5c9770e5979d39258fd746d48ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039585"
---
# <a name="sample-ice-in-c"></a>ICE de ejemplo en C++

Este código de ejemplo es de una acción personalizada de ICE [(ICE01).](ice01.md) Valida que el mecanismo ICE funciona mostrando la hora. El ICE publica un mensaje que indica la hora a la que el instalador llamó al ICE. Este ICE nunca debe devolver un error.


```C++
// 
// test of external database access
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <strsafe.h>
#include <MsiQuery.h>
#pragma comment(lib, "msi.lib")

///////////////////////////////////////////////////////////
// ICE01 - simple ICE that does not test anything
UINT __stdcall ICE01(MSIHANDLE hInstall)
{
    // setup the record to describe owner and date created
    PMSIHANDLE hRecCreated = ::MsiCreateRecord(1);
    ::MsiRecordSetString(hRecCreated, 0, TEXT("ICE01\t3\tCreated 04/29/1998 by <insert author's name here>"));

    // post the owner message
    ::MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_USER), hRecCreated); 
    // setup the record to describe the last time the ICE was modified
    ::MsiRecordSetString(hRecCreated, 0, TEXT("ICE01\t3\tLast modified 05/06/1998 by <insert author's name here>"));

    // post the last modification message
    ::MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_USER), hRecCreated);

    // setup the record to describe what the ICE evaluates
    ::MsiRecordSetString(hRecCreated, 0, TEXT("ICE01\t3\tSimple ICE illustrating the ICE concept"));

    // post the description of evaluation message
    ::MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_USER), hRecCreated);
    // time value to be sent on
    TCHAR szValue[200];
    DWORD cchValue = sizeof(szValue)/sizeof(TCHAR);

    // try to get the time of this call
    if (MsiGetProperty(hInstall, TEXT("Time"), szValue, &cchValue) != ERROR_SUCCESS)
        StringCchCopy(szValue,  sizeof("(none)")/sizeof(TCHAR)+1, TEXT("none"));// no time available

    // setup the record to be sent as a message
    PMSIHANDLE hRecTime = ::MsiCreateRecord(2);
    ::MsiRecordSetString(hRecTime, 0, TEXT("ICE01\t3\tCalled at [1]."));
    ::MsiRecordSetString(hRecTime, 1, szValue);

    // send the time
    ::MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_USER), hRecTime);

    return ERROR_SUCCESS; // allows other ICEs will continue
}
```



 

 



