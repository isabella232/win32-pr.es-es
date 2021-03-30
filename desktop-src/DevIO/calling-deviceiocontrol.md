---
description: Llamar a DeviceIoControl
ms.assetid: b4dbda89-effb-43f7-b3cc-774db57862a9
title: Llamar a DeviceIoControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf032182b4c461f13ebc046d30bc445abbfc9a1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538896"
---
# <a name="calling-deviceiocontrol"></a><span data-ttu-id="2899e-103">Llamar a DeviceIoControl</span><span class="sxs-lookup"><span data-stu-id="2899e-103">Calling DeviceIoControl</span></span>

<span data-ttu-id="2899e-104">Una aplicación puede usar la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) para realizar operaciones de entrada y salida directas en, o recuperar información acerca de una unidad de disquete, una unidad de disco duro, una unidad de cinta o una unidad de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="2899e-104">An application can use the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function to perform direct input and output operations on, or retrieve information about, a floppy disk drive, hard disk drive, tape drive, or CD-ROM drive.</span></span> <span data-ttu-id="2899e-105">Para obtener una lista de los códigos de control estándar que se incluyen en la documentación del SDK, consulte la sección Comentarios de **DeviceIoControl**.</span><span class="sxs-lookup"><span data-stu-id="2899e-105">For a list of standard control codes included in the SDK documentation, see the Remarks section of **DeviceIoControl**.</span></span>

<span data-ttu-id="2899e-106">En el ejemplo siguiente se muestra cómo recuperar información sobre la primera unidad física del sistema.</span><span class="sxs-lookup"><span data-stu-id="2899e-106">The following example demonstrates how to retrieve information about the first physical drive in the system.</span></span> <span data-ttu-id="2899e-107">Usa la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para recuperar el identificador del dispositivo en la primera unidad física y, a continuación, usa [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con el código de control de [geometría del disco de ioctl \_ \_ Get \_ Drive \_](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_geometry) para rellenar una estructura de [**\_ geometría del disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) con información sobre la unidad.</span><span class="sxs-lookup"><span data-stu-id="2899e-107">It uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to retrieve the device handle to the first physical drive, and then uses [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) with the [IOCTL\_DISK\_GET\_DRIVE\_GEOMETRY](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_geometry) control code to fill a [**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) structure with information about the drive.</span></span>


```C++
#define UNICODE 1
#define _UNICODE 1

/* The code of interest is in the subroutine GetDriveGeometry. The 
   code in main shows how to interpret the results of the call. */

#include <windows.h>
#include <winioctl.h>
#include <stdio.h>

#define wszDrive L"\\\\.\\PhysicalDrive0"

BOOL GetDriveGeometry(LPWSTR wszPath, DISK_GEOMETRY *pdg)
{
  HANDLE hDevice = INVALID_HANDLE_VALUE;  // handle to the drive to be examined 
  BOOL bResult   = FALSE;                 // results flag
  DWORD junk     = 0;                     // discard results

  hDevice = CreateFileW(wszPath,          // drive to open
                        0,                // no access to the drive
                        FILE_SHARE_READ | // share mode
                        FILE_SHARE_WRITE, 
                        NULL,             // default security attributes
                        OPEN_EXISTING,    // disposition
                        0,                // file attributes
                        NULL);            // do not copy file attributes

  if (hDevice == INVALID_HANDLE_VALUE)    // cannot open the drive
  {
    return (FALSE);
  }

  bResult = DeviceIoControl(hDevice,                       // device to be queried
                            IOCTL_DISK_GET_DRIVE_GEOMETRY, // operation to perform
                            NULL, 0,                       // no input buffer
                            pdg, sizeof(*pdg),            // output buffer
                            &junk,                         // # bytes returned
                            (LPOVERLAPPED) NULL);          // synchronous I/O

  CloseHandle(hDevice);

  return (bResult);
}

int wmain(int argc, wchar_t *argv[])
{
  DISK_GEOMETRY pdg = { 0 }; // disk drive geometry structure
  BOOL bResult = FALSE;      // generic results flag
  ULONGLONG DiskSize = 0;    // size of the drive, in bytes

  bResult = GetDriveGeometry (wszDrive, &pdg);

  if (bResult) 
  {
    wprintf(L"Drive path      = %ws\n",   wszDrive);
    wprintf(L"Cylinders       = %I64d\n", pdg.Cylinders);
    wprintf(L"Tracks/cylinder = %ld\n",   (ULONG) pdg.TracksPerCylinder);
    wprintf(L"Sectors/track   = %ld\n",   (ULONG) pdg.SectorsPerTrack);
    wprintf(L"Bytes/sector    = %ld\n",   (ULONG) pdg.BytesPerSector);

    DiskSize = pdg.Cylinders.QuadPart * (ULONG)pdg.TracksPerCylinder *
               (ULONG)pdg.SectorsPerTrack * (ULONG)pdg.BytesPerSector;
    wprintf(L"Disk size       = %I64d (Bytes)\n"
            L"                = %.2f (Gb)\n", 
            DiskSize, (double) DiskSize / (1024 * 1024 * 1024));
  } 
  else 
  {
    wprintf (L"GetDriveGeometry failed. Error %ld.\n", GetLastError ());
  }

  return ((int)bResult);
}
```



 

 
