---
description: En el ejemplo siguiente se usa la función GetSystemInfo para obtener información de hardware, como el identificador de OEM, el tipo de procesador, el tamaño de página, entre otros. En el ejemplo se muestra la información en la consola de .
ms.assetid: 9f943926-9ca7-4d4c-ad1e-b68c248e0e01
title: Obtener información de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d89ab5083e9d88e60d962ebcdd7b701a90e279cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073522"
---
# <a name="getting-hardware-information"></a>Obtener información de hardware

En el ejemplo siguiente se usa [**la función GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) para obtener información de hardware, como el identificador de OEM, el tipo de procesador, el tamaño de página, entre otros. En el ejemplo se muestra la información en la consola de .


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "user32.lib")

void main()
{
   SYSTEM_INFO siSysInfo;
 
   // Copy the hardware information to the SYSTEM_INFO structure. 
 
   GetSystemInfo(&siSysInfo); 
 
   // Display the contents of the SYSTEM_INFO structure. 

   printf("Hardware information: \n");  
   printf("  OEM ID: %u\n", siSysInfo.dwOemId);
   printf("  Number of processors: %u\n", 
      siSysInfo.dwNumberOfProcessors); 
   printf("  Page size: %u\n", siSysInfo.dwPageSize); 
   printf("  Processor type: %u\n", siSysInfo.dwProcessorType); 
   printf("  Minimum application address: %lx\n", 
      siSysInfo.lpMinimumApplicationAddress); 
   printf("  Maximum application address: %lx\n", 
      siSysInfo.lpMaximumApplicationAddress); 
   printf("  Active processor mask: %u\n", 
      siSysInfo.dwActiveProcessorMask); 
}
```



 

 
