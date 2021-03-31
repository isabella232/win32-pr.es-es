---
description: Windows envía a todas las ventanas de nivel superior un conjunto de mensajes de DEVICECHANGE de WM predeterminados \_ cuando se agregan nuevos dispositivos o medios (como un CD o DVD) y están disponibles, y cuando se quitan los dispositivos o medios existentes.
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: Detección de la inserción o eliminación de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6cfd4539d6f2ce5eac41e355f56a5a87835505
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157016"
---
# <a name="detecting-media-insertion-or-removal"></a>Detección de la inserción o eliminación de medios

Windows envía a todas las ventanas de nivel superior un conjunto de mensajes de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) predeterminados cuando se agregan nuevos dispositivos o medios (como un CD o DVD) y están disponibles, y cuando se quitan los dispositivos o medios existentes. No es necesario registrarse para recibir estos mensajes predeterminados. Vea la sección Comentarios en [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) para obtener más información sobre los mensajes que se envían de forma predeterminada. Los mensajes del ejemplo de código siguiente se encuentran entre los mensajes predeterminados.

> [!Note]  
> Windows solo envía mensajes de [**WM \_ DEVICECHANGE**](wm-devicechange.md) para eventos de medios de CD o DVD a ventanas de nivel superior que son propiedad de aplicaciones que se ejecutan en la sesión de consola activa. Las ventanas de nivel superior que son propiedad de las aplicaciones que se ejecutan en una sesión de escritorio remoto no reciben mensajes de [**WM \_ DEVICECHANGE**](wm-devicechange.md) para eventos de medios de CD o DVD.

 

Cada mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) tiene un evento asociado que describe el cambio y una estructura que proporciona información detallada sobre el cambio. La estructura consta de un encabezado independiente de eventos, [**dev \_ Broadcast \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), seguido de miembros dependientes del evento. Los miembros dependientes del evento describen el dispositivo al que se aplica el evento. Para usar esta estructura, las aplicaciones deben determinar primero el tipo de evento y el tipo de dispositivo. A continuación, pueden usar la estructura correcta para tomar las medidas adecuadas.

Cuando el usuario inserta un CD o DVD nuevo en una unidad de disco, las aplicaciones reciben un mensaje de [**WM \_ DEVICECHANGE**](wm-devicechange.md) con un evento [ \_ DEVICEARRIVAL de DBT](dbt-devicearrival.md) . La aplicación debe comprobar el evento para asegurarse de que el tipo de dispositivo que llega es un volumen (el miembro **dbch \_ DeviceType** es **DBT \_ DEVTYP \_**) y que el cambio afecta a los medios (el miembro **dbcv \_ Flags** es **DBTF \_ medios**).

Cuando el usuario quita un CD o un DVD de una unidad, las aplicaciones reciben un mensaje de [**WM \_ DEVICECHANGE**](wm-devicechange.md) con un evento [ \_ DEVICEREMOVECOMPLETE de DBT](dbt-deviceremovecomplete.md) . De nuevo, la aplicación debe comprobar el evento para asegurarse de que el dispositivo que se va a quitar es un volumen y que el cambio afecta a los medios.

En el código siguiente se muestra cómo comprobar la inserción o eliminación de un CD o DVD.


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
#pragma comment(lib, "user32.lib" )

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam );
char FirstDriveFromMask( ULONG unitmask );  //prototype

/*------------------------------------------------------------------
   Main_OnDeviceChange( hwnd, wParam, lParam )

   Description
      Handles WM_DEVICECHANGE messages sent to the application's
      top-level window.
--------------------------------------------------------------------*/

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam )
 {
  PDEV_BROADCAST_HDR lpdb = (PDEV_BROADCAST_HDR)lParam;
  TCHAR szMsg[80];

  switch(wParam )
   {
    case DBT_DEVICEARRIVAL:
      // Check whether a CD or DVD was inserted into a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media has arrived.\n"), 
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE"), MB_OK );
         }
       }
      break;

    case DBT_DEVICEREMOVECOMPLETE:
      // Check whether a CD or DVD was removed from a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media was removed.\n" ),
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE" ), MB_OK );
         }
       }
      break;

    default:
      /*
        Process other WM_DEVICECHANGE notifications for other 
        devices or reasons.
      */ 
      ;
   }
}

/*------------------------------------------------------------------
   FirstDriveFromMask( unitmask )

   Description
     Finds the first valid drive letter from a mask of drive letters.
     The mask must be in the format bit 0 = A, bit 1 = B, bit 2 = C, 
     and so on. A valid drive letter is defined when the 
     corresponding bit is set to 1.

   Returns the first drive letter that was found.
--------------------------------------------------------------------*/

char FirstDriveFromMask( ULONG unitmask )
 {
  char i;

  for (i = 0; i < 26; ++i)
   {
    if (unitmask & 0x1)
      break;
    unitmask = unitmask >> 1;
   }

  return( i + 'A' );
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Eventos de dispositivo](device-events.md)
</dt> </dl>

 

 



