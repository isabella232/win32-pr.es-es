---
description: Cuando una llamada está activa en LINEBEARERMODE \_ PASSTHROUGH, el proveedor de servicios proporciona acceso directo al hardware asociado para que la aplicación lo controle.
ms.assetid: 75e31241-c782-4d50-9590-cf68c0505add
title: Modo de paso a través
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 985e1caf666fcb3278bacf5c5cfe9d8a4e847dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687063"
---
# <a name="passthrough-mode"></a>Modo de paso a través

Cuando una llamada está activa en **LINEBEARERMODE \_ PASSTHROUGH**, el proveedor de servicios proporciona acceso directo al hardware asociado para que la aplicación lo controle. Las aplicaciones pueden usar este modo para el control directo temporal a través de módems asincrónicos, al que se tiene acceso a través de las [funciones de comunicaciones](/windows/desktop/DevIO/communications-functions), con el fin de configurar o usar características especiales que no admite el proveedor de servicios, como facsímil (clase 1, 2, etc.). Este modo de portador es compatible con el proveedor de servicios del controlador de módem universal (Unimodem).

Los proveedores de servicios que admiten **LINEBEARERMODE \_ PASSTHROUGH** lo indican en el miembro **DwBearerModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) . Cuando se indica **LINEBEARERMODE \_ PASSTHROUGH** , el proveedor de servicios Unimodem también incluirá en el área **DevSpecific** de la estructura **LINEDEVCAPS** la clave del registro que se usa para tener acceso a los datos sobre el módem asociado con el dispositivo de línea, en el formato siguiente:

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

Esta clave del registro se puede abrir a continuación con la función [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) .

El modo de paso a través se invoca con mayor frecuencia mediante la función [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) , estableciendo el bit de **\_ paso de LINEBEARERMODE** en el miembro **dwBearerMode** de la estructura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) señalada por el parámetro *lpCallParams* . Cuando se hace esto, el proveedor de servicios abre el puerto serie al módem e inmediatamente coloca la llamada en **LINECALLSTATE \_ Connected**. A continuación, la aplicación puede usar la función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) con la clase de dispositivo "COMM/telemodem" para obtener un identificador de archivo abierto para leer y escribir en el puerto COMM.

También se puede invocar el modo de paso a través en respuesta a una llamada entrante. Por lo general, las aplicaciones invocarán el modo de paso a través mientras la llamada está en la **\_ oferta de LINECALLSTATE**, antes de que se haya respondido a la llamada. En lugar de llamar a [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer), la aplicación llama a [**LineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams), pasando **LINEBEARERMODE \_ PASSTHROUGH** como el parámetro *dwBearerMode* . Cuando esto se hace, al igual que con [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), la llamada se coloca inmediatamente en **LINECALLSTATE \_ conectado** por el proveedor de servicios y la aplicación puede obtener un identificador para el puerto abierto mediante [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid). Se puede llamar a la función **lineSetCallParams** cuando la llamada está en la **\_ oferta LINECALLSTATE**, **LINECALLSTATE \_ aceptada** o **LINECALLSTATE \_ conectada**.

Normalmente, el modo de paso a través llama a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) en el identificador de llamada Obtenido de [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) o el mensaje de la primera [**línea \_ CALLSTATE**](line-callstate.md) , si la llamada fue una llamada entrante. El proveedor de servicios cerrará el puerto y restaurará el módem a su estado predeterminado. La aplicación debe llamar a [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) en el identificador recibido de [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).

El modo de paso a través también puede terminar llamando a [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) con el parámetro *DwBearerMode* establecido en **LINEBEARERMODE \_ Voice**. Se supone que el tipo de medio (modo) establecido por [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode) está en vigor. Si **LINEMEDIAMODE \_** se encuentra activo, el proveedor de servicios tomará la llamada como si fuera una llamada al módem de datos ya en curso; si se llama a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) posteriormente, el proveedor de servicios emitirá los comandos de módem o los cambios de estado de la interfaz adecuados para quitar una llamada de datos.

> [!Note]  
> Si el modo de paso a través finaliza mientras la llamada está en curso, el proveedor de servicios TAPI (TSP) de la línea puede restaurar la configuración del módem a su estado predeterminado. Unimodem es un ejemplo de un TSP que siempre restaura la configuración del módem al finalizar el modo de paso a través. Por esta razón, no se puede usar el modo de paso a través como método para configurar el dispositivo. El modo de paso a través solo se debe usar para actividades distintas que se pueden considerar completadas cuando se termina el acceso directo. Entre los ejemplos de actividades que pueden usar el modo de paso a través se incluyen el envío de un fax o la reproducción de datos de audio o de voz mediante un protocolo de módem propietario.

 

 

 
