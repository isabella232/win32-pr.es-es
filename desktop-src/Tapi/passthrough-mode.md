---
description: Cuando una llamada está activa en LINEBEARERMODE PASSTHROUGH, el proveedor de servicios proporciona acceso directo al hardware conectado para que la aplicación \_ lo controle.
ms.assetid: 75e31241-c782-4d50-9590-cf68c0505add
title: Modo de acceso directo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 985e1caf666fcb3278bacf5c5cfe9d8a4e847dbb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068737"
---
# <a name="passthrough-mode"></a>Modo de acceso directo

Cuando una llamada está activa en **LINEBEARERMODE \_ PASSTHROUGH**, el proveedor de servicios proporciona acceso directo al hardware conectado para que la aplicación controle. Las aplicaciones pueden usar este modo para el control directo temporal sobre módems asincrónicos, a los que se accede a través de las funciones de comunicaciones [,](/windows/desktop/DevIO/communications-functions)con el fin de configurar o usar características especiales que el proveedor de servicios no admite de otro modo, como facsímil (clase 1, 2, y así sucesivamente). Este modo de portador es compatible con el proveedor de servicios del controlador de módem universal (UNIMODEM).

Los proveedores de servicios que **admiten LINEBEARERMODE \_ PASSTHROUGH** lo indican en el **miembro dwBearerModes** de la [**estructura LINEDEVCAPS.**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) Cuando se indica **LINEBEARERMODE \_ PASSTHROUGH,** el proveedor de servicios Unimodem también incluirá en el área **DevSpecific** de la estructura **LINEDEVCAPS** la clave del Registro utilizada para acceder a los datos sobre el módem asociado al dispositivo de línea, en el formato siguiente:

``` syntax
struct {
    DWORD dwContents;   // Set to 1 (indicates containing key).
    DWORD dwKeyOffset;  // Offset to key from start of this
                        // structure (not from start of
                        // LINEDEVCAPS structure).
                        // 8 in this case. 
    BYTE rgby[...];     // Place that contains null-terminated
                        // registry key. 
}
```

Por ejemplo:

``` syntax
    00000001 00000008 74737953 435c6d65  ........System\C
    65727275 6f43746e 6f72746e 7465536c  urrentControlSet
    7265535c 65636976 6c435c73 5c737361  urrentControlSet
    65646f4d 30305c6d xx003030 xxxxxxxx  Modem\0000.
```

Esta clave del Registro se podría abrir con la [**función RegOpenKey.**](/windows/desktop/api/winreg/nf-winreg-regopenkeya)

El modo de acceso directo se invoca con mayor frecuencia mediante la función [**lineMakeCall,**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) estableciendo el bit **LINEBEARERMODE \_ PASSTHROUGH** en el miembro **dwBearerMode** de la estructura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) a la que apunta el parámetro *lpCallParams.* Cuando esto se hace, el proveedor de servicios abre el puerto serie al módem y coloca inmediatamente la llamada en **LINECALLSTATE \_ CONNECTED.** Después, la aplicación puede usar la función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) con la clase de dispositivo "comm/datamodem" para obtener un identificador de archivo abierto desde el que leer y escribir en el puerto comm.

El modo de acceso directo también se puede invocar en respuesta a una llamada entrante. Por lo general, las aplicaciones invocarán el modo de acceso directo mientras la llamada está en **LINECALLSTATE \_ OFFERING**, antes de que se haya respondido a la llamada. En lugar de llamar [**a lineAnswer,**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)la aplicación llama a [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams)y pasa **LINEBEARERMODE \_ PASSTHROUGH** como *parámetro dwBearerMode.* Cuando esto se hace, al igual que con [**lineMakeCall,**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)el proveedor de servicios coloca inmediatamente la llamada a **LINECALLSTATE \_ CONNECTED** y la aplicación puede obtener un identificador para el puerto abierto mediante [**lineGetID.**](/windows/desktop/api/Tapi/nf-tapi-linegetid) Se puede llamar a la función **lineSetCallParams** cuando la llamada está en **LINECALLSTATE \_ OFFERING**, **LINECALLSTATE \_ ACCEPTED** o **LINECALLSTATE \_ CONNECTED.**

Normalmente, el modo de acceso directo finaliza mediante una llamada a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) en el identificador de llamada obtenido de [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) o el primer mensaje [**LINE \_ CALLSTATE,**](line-callstate.md) si la llamada era una llamada entrante. El proveedor de servicios cerrará el puerto y restaurará el módem a su estado predeterminado. La aplicación debe llamar [**a CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) en el identificador que recibió de [**lineGetID.**](/windows/desktop/api/Tapi/nf-tapi-linegetid)

El modo de acceso directo también se puede finalizar llamando [**a lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) con el parámetro *dwBearerMode* establecido en **LINEBEARERMODE \_ VOICE.** Se supone que el tipo de medio (modo) [**establecido por lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode) está en vigor. Si **LINEMEDIAMODE \_ DATAMODEM** está activo, el proveedor de servicios se hará cargo de la llamada como si se tratase de una llamada de módem de datos ya en curso; si posteriormente se llama a [**lineDrop,**](/windows/desktop/api/Tapi/nf-tapi-linedrop) el proveedor de servicios emitirá los comandos de módem adecuados o los cambios de estado de la interfaz para quitar una llamada de datos.

> [!Note]  
> Si el modo de acceso directo finaliza mientras la llamada está en curso, el proveedor de servicios TAPI (TSP) de la línea puede restaurar la configuración del módem a su estado predeterminado. Unimodem es un ejemplo de un TSP que siempre restaura la configuración del módem al finalizar el modo de paso a través. Por esta razón, el modo de acceso directo no se puede usar como método para configurar el dispositivo. El modo de acceso directo solo debe usarse para actividades distintas que se pueden considerar completas cuando finaliza el paso a través. Entre los ejemplos de actividades que pueden usar el modo de acceso directo se incluyen el envío de un fax o la reproducción de datos de onda/audio a través de un protocolo de módem propietario.

 

 

 
