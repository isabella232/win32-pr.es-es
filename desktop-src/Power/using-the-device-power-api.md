---
description: Use los elementos de programación Device Power para administrar el rendimiento de los dispositivos mientras el sistema está en estado de suspensión.
ms.assetid: 44479f5d-2e92-4802-a633-3e0bb7d61e94
title: Uso de Device Power API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cabd7a54efc0979360a863dc9c0cf16d69d8d22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169130"
---
# <a name="using-the-device-power-api"></a>Uso de Device Power API

Use los elementos de programación Device Power para administrar el rendimiento de los dispositivos mientras el sistema está en estado de suspensión.

## <a name="opening-and-closing-the-device-list"></a>Apertura y cierre de la lista de dispositivos

Abrir y cerrar la lista de dispositivos es un proceso costoso en términos de tiempo de CPU. Las [**funciones DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) [**y DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) que hacen esto solo son necesarias si la aplicación necesita consultar la lista de dispositivos varias veces.

Si [**se llama a DevicePowerOpen,**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) se debe llamar a [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) cuando se completen las consultas de lista de dispositivos. [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) y [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) no cerrarán la lista de dispositivos si **DevicePowerOpen** la ha abierto explícitamente.

## <a name="enumerating-devices"></a>Enumeración de dispositivos

La [**función DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) detecta si la lista de dispositivos está abierta y, si no es así, la abre. **DevicePowerEnumDevices** enumera los dispositivos según los criterios de búsqueda especificados. Si la función abrió la lista de dispositivos, se cierra antes de que se devuelva la función.

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a>Habilitación y deshabilitación de un dispositivo para evitar la activación del sistema

La [**función DevicePowerSetDeviceState,**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) similar a [**DevicePowerEnumDevices,**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices)detecta si la lista de dispositivos está abierta y, si no es así, la abre. **DevicePowerSetDeviceState** establece los criterios especificados para el dispositivo especificado. Si la función abrió la lista de dispositivos, se cierra antes de que se devuelva la función.

## <a name="example-code"></a>Código de ejemplo

En el ejemplo siguiente se muestra el uso de Device Power API.


```C++
#define _WIN32_WINNT 0x0600
#include <Windows.h>
#include <PowrProf.h>
#include <stdio.h>
#include <tchar.h>

#pragma comment(lib, "PowrProf.lib")

int __cdecl main()
{
 // Define and initialize our return variables.
 LPWSTR  pRetBuf = NULL;
 ULONG bufSize = MAX_PATH * sizeof(WCHAR);
 ULONG uIndex = 0;
 BOOLEAN bRet = FALSE;

 // Open the device list, querying all devices
 if (!DevicePowerOpen(0)) 
  {
   printf("ERROR: The device database failed to initialize.\n");
   return FALSE;
  }

 // Enumerate the device list, searching for devices that support 
 // waking from either the S1 or S2 sleep state and are currently 
 // present in the system, and not devices that have drivers 
 // installed but are not currently attached to the system, such as 
 // in a laptop docking station.

 pRetBuf = (LPWSTR)LocalAlloc(LPTR, bufSize);

 while (NULL != pRetBuf && 
        0 != (bRet = DevicePowerEnumDevices(uIndex,
           DEVICEPOWER_FILTER_DEVICES_PRESENT,
           PDCAP_WAKE_FROM_S1_SUPPORTED|PDCAP_WAKE_FROM_S2_SUPPORTED,
           (PBYTE)pRetBuf,
           &bufSize)))
  {
   printf("Device name: %S\n", pRetBuf);

   // For the devices we found that have support for waking from 
   // S1 and S2 sleep states, disable them from waking the system.
   bRet = (0 != DevicePowerSetDeviceState((LPCWSTR)pRetBuf, 
                                  DEVICEPOWER_CLEAR_WAKEENABLED, 
                                  NULL));

   if (0 != bRet) 
    {
     printf("Warning: Failed to set device state.\n");
    }
   uIndex++;
  }

 // Close the device list.
 DevicePowerClose();
 if (pRetBuf!= NULL) LocalFree(pRetBuf);
 pRetBuf = NULL;

 return TRUE;
}
```



En este ejemplo, la lista de dispositivos se abre una vez y se cierra una vez. Si no se llamara a las funciones [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) y [**DevicePowerClose,**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) cada llamada a [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) y [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate)habría abierto y cerrado la lista de dispositivos. Al usar **DevicePowerOpen y** **DevicePowerClose,** hemos guardado la apertura de la lista de dispositivos dos veces innecesarias.

 

 



