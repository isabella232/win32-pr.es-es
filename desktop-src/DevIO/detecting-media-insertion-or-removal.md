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
# <a name="detecting-media-insertion-or-removal"></a><span data-ttu-id="d1724-103">Detección de la inserción o eliminación de medios</span><span class="sxs-lookup"><span data-stu-id="d1724-103">Detecting Media Insertion or Removal</span></span>

<span data-ttu-id="d1724-104">Windows envía a todas las ventanas de nivel superior un conjunto de mensajes de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) predeterminados cuando se agregan nuevos dispositivos o medios (como un CD o DVD) y están disponibles, y cuando se quitan los dispositivos o medios existentes.</span><span class="sxs-lookup"><span data-stu-id="d1724-104">Windows sends all top-level windows a set of default [**WM\_DEVICECHANGE**](wm-devicechange.md) messages when new devices or media (such as a CD or DVD) are added and become available, and when existing devices or media are removed.</span></span> <span data-ttu-id="d1724-105">No es necesario registrarse para recibir estos mensajes predeterminados.</span><span class="sxs-lookup"><span data-stu-id="d1724-105">You do not need to register to receive these default messages.</span></span> <span data-ttu-id="d1724-106">Vea la sección Comentarios en [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) para obtener más información sobre los mensajes que se envían de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d1724-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details on which messages are sent by default.</span></span> <span data-ttu-id="d1724-107">Los mensajes del ejemplo de código siguiente se encuentran entre los mensajes predeterminados.</span><span class="sxs-lookup"><span data-stu-id="d1724-107">The messages in the code example below are among the default messages.</span></span>

> [!Note]  
> <span data-ttu-id="d1724-108">Windows solo envía mensajes de [**WM \_ DEVICECHANGE**](wm-devicechange.md) para eventos de medios de CD o DVD a ventanas de nivel superior que son propiedad de aplicaciones que se ejecutan en la sesión de consola activa.</span><span class="sxs-lookup"><span data-stu-id="d1724-108">Windows only sends [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events to top-level windows that are owned by applications that run in the active console session.</span></span> <span data-ttu-id="d1724-109">Las ventanas de nivel superior que son propiedad de las aplicaciones que se ejecutan en una sesión de escritorio remoto no reciben mensajes de [**WM \_ DEVICECHANGE**](wm-devicechange.md) para eventos de medios de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="d1724-109">Top-level windows that are owned by applications that run in a remote desktop session do not receive [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events.</span></span>

 

<span data-ttu-id="d1724-110">Cada mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) tiene un evento asociado que describe el cambio y una estructura que proporciona información detallada sobre el cambio.</span><span class="sxs-lookup"><span data-stu-id="d1724-110">Each [**WM\_DEVICECHANGE**](wm-devicechange.md) message has an associated event that describes the change, and a structure that provides detailed information about the change.</span></span> <span data-ttu-id="d1724-111">La estructura consta de un encabezado independiente de eventos, [**dev \_ Broadcast \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), seguido de miembros dependientes del evento.</span><span class="sxs-lookup"><span data-stu-id="d1724-111">The structure consists of an event-independent header, [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), followed by event-dependent members.</span></span> <span data-ttu-id="d1724-112">Los miembros dependientes del evento describen el dispositivo al que se aplica el evento.</span><span class="sxs-lookup"><span data-stu-id="d1724-112">The event-dependent members describe the device to which the event applies.</span></span> <span data-ttu-id="d1724-113">Para usar esta estructura, las aplicaciones deben determinar primero el tipo de evento y el tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1724-113">To use this structure, applications must first determine the event type and the device type.</span></span> <span data-ttu-id="d1724-114">A continuación, pueden usar la estructura correcta para tomar las medidas adecuadas.</span><span class="sxs-lookup"><span data-stu-id="d1724-114">Then, they can use the correct structure to take appropriate action.</span></span>

<span data-ttu-id="d1724-115">Cuando el usuario inserta un CD o DVD nuevo en una unidad de disco, las aplicaciones reciben un mensaje de [**WM \_ DEVICECHANGE**](wm-devicechange.md) con un evento [ \_ DEVICEARRIVAL de DBT](dbt-devicearrival.md) .</span><span class="sxs-lookup"><span data-stu-id="d1724-115">When the user inserts a new CD or DVD into a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEARRIVAL](dbt-devicearrival.md) event.</span></span> <span data-ttu-id="d1724-116">La aplicación debe comprobar el evento para asegurarse de que el tipo de dispositivo que llega es un volumen (el miembro **dbch \_ DeviceType** es **DBT \_ DEVTYP \_**) y que el cambio afecta a los medios (el miembro **dbcv \_ Flags** es **DBTF \_ medios**).</span><span class="sxs-lookup"><span data-stu-id="d1724-116">The application must check the event to ensure that the type of device arriving is a volume (the **dbch\_devicetype** member is **DBT\_DEVTYP\_VOLUME**) and that the change affects the media (the **dbcv\_flags** member is **DBTF\_MEDIA**).</span></span>

<span data-ttu-id="d1724-117">Cuando el usuario quita un CD o un DVD de una unidad, las aplicaciones reciben un mensaje de [**WM \_ DEVICECHANGE**](wm-devicechange.md) con un evento [ \_ DEVICEREMOVECOMPLETE de DBT](dbt-deviceremovecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="d1724-117">When the user removes a CD or DVD from a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) event.</span></span> <span data-ttu-id="d1724-118">De nuevo, la aplicación debe comprobar el evento para asegurarse de que el dispositivo que se va a quitar es un volumen y que el cambio afecta a los medios.</span><span class="sxs-lookup"><span data-stu-id="d1724-118">Again, the application must check the event to ensure that the device being removed is a volume and that the change affects the media.</span></span>

<span data-ttu-id="d1724-119">En el código siguiente se muestra cómo comprobar la inserción o eliminación de un CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="d1724-119">The following code demonstrates how to check for insertion or removal of a CD or DVD.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d1724-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1724-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1724-121">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d1724-121">Device Events</span></span>](device-events.md)
</dt> </dl>

 

 



