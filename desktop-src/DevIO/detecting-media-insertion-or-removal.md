---
description: Windows envía a todas las ventanas de nivel superior un conjunto de mensajes PREDETERMINADOS DE WM DEVICECHANGE cuando se agregan nuevos dispositivos o medios (como un CD o DVD) y están disponibles, y cuando se quitan los dispositivos o medios \_ existentes.
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: Detección de inserción o eliminación de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6cfd4539d6f2ce5eac41e355f56a5a87835505
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164438"
---
# <a name="detecting-media-insertion-or-removal"></a>Detección de inserción o eliminación de medios

Windows envía a todas las ventanas de nivel superior un conjunto de mensajes [**DE WM \_ DEVICECHANGE**](wm-devicechange.md) predeterminados cuando se agregan nuevos dispositivos o medios (como un CD o DVD) y están disponibles, y cuando se quitan los dispositivos o medios existentes. No es necesario registrarse para recibir estos mensajes predeterminados. Consulte la sección Comentarios de [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) para obtener más información sobre qué mensajes se envían de forma predeterminada. Los mensajes del ejemplo de código siguiente se encuentran entre los mensajes predeterminados.

> [!Note]  
> Windows envía mensajes [**DE WM \_ DEVICECHANGE**](wm-devicechange.md) para eventos multimedia de CD o DVD a ventanas de nivel superior que pertenecen a aplicaciones que se ejecutan en la sesión de consola activa. Las ventanas de nivel superior que pertenecen a aplicaciones que se ejecutan en una sesión de Escritorio remoto no reciben mensajes [**DE WM \_ DEVICECHANGE**](wm-devicechange.md) para eventos multimedia de CD o DVD.

 

Cada [**mensaje \_ DEVICECHANGE de WM**](wm-devicechange.md) tiene un evento asociado que describe el cambio y una estructura que proporciona información detallada sobre el cambio. La estructura consta de un encabezado independiente del evento, [**DEV \_ BROADCAST \_ HDR,**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)seguido de miembros dependientes del evento. Los miembros dependientes del evento describen el dispositivo al que se aplica el evento. Para usar esta estructura, las aplicaciones deben determinar primero el tipo de evento y el tipo de dispositivo. A continuación, pueden usar la estructura correcta para tomar las medidas adecuadas.

Cuando el usuario inserta un nuevo CD o DVD en una unidad, las aplicaciones reciben un mensaje [**DE WM \_ DEVICECHANGE**](wm-devicechange.md) con un [evento \_ DBT DEVICEARRIVAL.](dbt-devicearrival.md) La aplicación debe comprobar el evento para asegurarse de que el tipo de dispositivo que llega es un volumen (el miembro **dbch \_ devicetype** es **DBT \_ DEVTYP \_ VOLUME**) y que el cambio afecta a los medios (el miembro **dbcv \_ flags** **es DBTF \_ MEDIA).**

Cuando el usuario quita un CD o DVD de una unidad, las aplicaciones reciben un mensaje [**DE WM \_ DEVICECHANGE**](wm-devicechange.md) con un [evento \_ DBT DEVICEREMOVECOMPLETE.](dbt-deviceremovecomplete.md) Una vez más, la aplicación debe comprobar el evento para asegurarse de que el dispositivo que se va a quitar es un volumen y de que el cambio afecta a los medios.

El código siguiente muestra cómo comprobar la inserción o eliminación de un CD o DVD.


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

 

 



