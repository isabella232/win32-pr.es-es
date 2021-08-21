---
description: Una aplicación recibe un evento de dispositivo DBT DEVICEQUERYREMOVE cuando una característica del sistema ha \_ decidido quitar un dispositivo especificado.
ms.assetid: 66f6c9f4-93fa-4ee8-adf8-cde4e63f9fb7
title: Procesamiento de una solicitud para quitar un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6432ba2709dd05589acd5f8e0a2d1de6547216c9d24d4c9d742b9ad6dcc838e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956784"
---
# <a name="processing-a-request-to-remove-a-device"></a>Procesamiento de una solicitud para quitar un dispositivo

Una aplicación recibe un [evento de dispositivo \_ DBT DEVICEQUERYREMOVE](dbt-devicequeryremove.md) cuando una característica del sistema ha decidido quitar un dispositivo especificado. Cuando la aplicación recibe este evento, debe determinar si usa el dispositivo especificado y cancelar o preparar la eliminación.

En el ejemplo siguiente, una aplicación mantiene un identificador abierto, hFile, en el archivo o dispositivo representado por FileName. La aplicación se registra para la notificación de eventos de dispositivo en el dispositivo subyacente mediante una llamada a la función [**RegisterDeviceNotification,**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) mediante un filtro de notificación de tipo HANDLE de **DBT \_ DEVTYP \_** y especificando la variable hFile en el miembro de identificador **dbch \_** del filtro.

La aplicación procesa el evento [de dispositivo DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) cerrando el identificador de archivo abierto al dispositivo que se va a quitar. En caso de que se cancele la eliminación de este dispositivo, la aplicación procesa el evento de dispositivo [DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) para volver a abrir el identificador en el dispositivo. Después de quitar el dispositivo del sistema, la aplicación procesa los eventos de dispositivo [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) y [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) anulando el registro de su identificador de notificación para el dispositivo y cerrando los identificadores que todavía están abiertos en el dispositivo.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de eventos de dispositivo](device-event-types.md)
</dt> </dl>

 

 



