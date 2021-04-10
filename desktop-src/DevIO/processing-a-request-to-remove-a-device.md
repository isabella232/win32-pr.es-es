---
description: Una aplicación recibe un \_ evento de dispositivo DBT DEVICEQUERYREMOVE cuando una característica del sistema ha decidido quitar un dispositivo especificado.
ms.assetid: 66f6c9f4-93fa-4ee8-adf8-cde4e63f9fb7
title: Procesamiento de una solicitud para quitar un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f6f1089cae0e4c9db964e3877cac8f8f8d8da4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153089"
---
# <a name="processing-a-request-to-remove-a-device"></a><span data-ttu-id="4a1fe-103">Procesamiento de una solicitud para quitar un dispositivo</span><span class="sxs-lookup"><span data-stu-id="4a1fe-103">Processing a Request to Remove a Device</span></span>

<span data-ttu-id="4a1fe-104">Una aplicación recibe un evento de dispositivo [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) cuando una característica del sistema ha decidido quitar un dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="4a1fe-104">An application receives a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) device event when a feature in the system has decided to remove a specified device.</span></span> <span data-ttu-id="4a1fe-105">Cuando la aplicación recibe este evento, debe determinar si está utilizando el dispositivo especificado y cancelar o preparar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="4a1fe-105">When the application receives this event, it should determine whether it is using the specified device and either cancel or prepare for the removal.</span></span>

<span data-ttu-id="4a1fe-106">En el ejemplo siguiente, una aplicación mantiene un identificador abierto, hFile, en el archivo o dispositivo representado por FileName.</span><span class="sxs-lookup"><span data-stu-id="4a1fe-106">In the following example, an application maintains an open handle, hFile, to the file or device represented by FileName.</span></span> <span data-ttu-id="4a1fe-107">La aplicación se registra para la notificación de eventos de dispositivo en el dispositivo subyacente mediante una llamada a la función [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) , mediante un filtro de notificación de tipo **DBT \_ DEVTYP \_ Handle** y especificando la variable hFile en el miembro de **\_ identificador dbch** del filtro.</span><span class="sxs-lookup"><span data-stu-id="4a1fe-107">The application registers for device event notification on the underlying device by calling the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function, using a **DBT\_DEVTYP\_HANDLE** type notification filter and specifying the hFile variable in the **dbch\_handle** member of the filter.</span></span>

<span data-ttu-id="4a1fe-108">La aplicación procesa el evento de dispositivo [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) cerrando el identificador de archivo abierto en el dispositivo que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="4a1fe-108">The application processes the [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) device event by closing the open file handle to the device that is to be removed.</span></span> <span data-ttu-id="4a1fe-109">En el caso de que se cancele la eliminación de este dispositivo, la aplicación procesa el evento de dispositivo [DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) para volver a abrir el identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a1fe-109">In the event that removal of this device is canceled, the application processes the [DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) device event to reopen the handle to the device.</span></span> <span data-ttu-id="4a1fe-110">Una vez que el dispositivo se ha quitado del sistema, la aplicación procesa los eventos de dispositivo [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) y [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) al anular el registro de su identificador de notificación para el dispositivo y cerrar los identificadores que todavía están abiertos en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a1fe-110">After the device has been removed from the system, the application processes the [DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) and [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) device events by unregistering its notification handle for the device and closing any handles that are still open to the device.</span></span>


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
  // ...

INT_PTR WINAPI WinProcCallback( HWND hWnd,
                                UINT message,
                                WPARAM wParam,
                                LPARAM lParam )
{
  LPCTSTR FileName = NULL;              // path to the file or device of interest
  HANDLE  hFile = INVALID_HANDLE_VALUE; // handle to the file or device

  PDEV_BROADCAST_HDR    pDBHdr;
  PDEV_BROADCAST_HANDLE pDBHandle;
  TCHAR szMsg[80];

  switch (message)
  {
  //...
  case WM_DEVICECHANGE:
    switch (wParam)
    {
      case DBT_DEVICEQUERYREMOVE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // A request has been made to remove the device;
            // close any open handles to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }
        }
        return TRUE;

      case DBT_DEVICEQUERYREMOVEFAILED:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // Removal of the device has failed;
            // reopen a handle to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            hFile = CreateFile(FileName,
                       GENERIC_READ,
                       FILE_SHARE_READ,
                       NULL,
                       OPEN_EXISTING,
                       FILE_ATTRIBUTE_NORMAL,
                       NULL);
            if (hFile == INVALID_HANDLE_VALUE) 
            {
              StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                               TEXT("CreateFile failed: %lx.\n"), 
                               GetLastError());
              MessageBox(hWnd, szMsg, TEXT("CreateFile"), MB_OK);
            }
        }
        return TRUE;

      case DBT_DEVICEREMOVEPENDING:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
          
            // The device is being removed;
            // close any open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      case DBT_DEVICEREMOVECOMPLETE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            // The device has been removed from the system;
            // unregister its notification handle

            UnregisterDeviceNotification(
              pDBHandle->dbch_hdevnotify);
              
            // The device has been removed;
            // close any remaining open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      default:
        return TRUE;
    }
  }
  default:
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="4a1fe-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4a1fe-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a1fe-112">Tipos de eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="4a1fe-112">Device Event Types</span></span>](device-event-types.md)
</dt> </dl>

 

 



