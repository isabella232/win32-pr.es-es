---
description: La clase de dispositivo COMM/telemodem consta de los dispositivos de módem.
ms.assetid: 6bc314c6-30ec-4318-856a-3ab2fa6aadfb
title: COMM/telemodem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89210bcf14931e3905f71cdbb8678f5519cc4c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687022"
---
# <a name="commdatamodem"></a>COMM/telemodem

La clase de dispositivo COMM/telemodem consta de los dispositivos de módem. Puede tener acceso a estos dispositivos mediante las funciones de [archivo](/windows/desktop/FileIO/file-management-functions) y de [comunicaciones](/windows/desktop/DevIO/communications-functions). Los dispositivos de esta clase están asociados a los dispositivos de línea que admiten el tipo de medio de LINEMEDIAMODE de los \_ archivos de módem, que se especifica en el miembro **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea.

La función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando estos miembros adicionales:

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

El miembro **hComm** es el identificador del puerto de comunicaciones abierto. Este miembro es **null** si el puerto todavía no está abierto o si el parámetro *dwSelect* de [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) no es el \_ valor de llamada LINECALLSELECT. Si una llamada está activa, el proveedor de servicios normalmente abre el propio puerto para obtener el control directo del hardware de comunicaciones, pero solo es necesario devolver un identificador válido si la línea está conectada. El proveedor de servicios abre el puerto con el \_ valor de indicador de archivo \_ superpuesto y, a continuación, configura el puerto con la configuración especificada por la función [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) . Puede establecer opciones de configuración adicionales para el dispositivo mediante el uso de funciones de comunicaciones con el identificador devuelto.

El miembro **szDeviceName** es una cadena terminada en **null** que especifica el nombre del puerto de comunicaciones asociado a la línea, dirección o llamada.

Si **hComm** es un identificador válido, puede usarlo en llamadas subsiguientes a funciones de archivo, como [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), para enviar y recibir datos en la llamada. Cuando haya terminado de usar el puerto de comunicaciones y preferiblemente antes de usar la función [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) para desasignar la llamada, debe cerrar el puerto mediante la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

Cuando se usan las funciones [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) y [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) , algunos proveedores de servicios requieren que los datos de configuración de esta clase de dispositivo tengan el siguiente formato:

``` syntax
typedef struct  tagDEVCFG  {
  DEVCFGHDR   dfgHdr;
  COMMCONFIG  commconfig;
} DEVCFG, *PDEVCFG, FAR* LPDEVCFG;

// Device setting information
typedef struct  tagDEVCFGDR  {
  DWORD       dwSize;
  DWORD       dwVersion;
  WORD        fwOptions;
  WORD        wWaitBong;
} DEVCFGHDR;
```

A continuación se proporciona información de configuración de dispositivos para su uso con las funciones [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) y [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Suma del tamaño de la estructura **DEVCFGHDR** y el tamaño real de la estructura [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) .

</dd> <dt>

<span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**
</dt> <dd>

Número de versión de la estructura **DevConfig** de Unimodem. Este miembro puede ser MDMCFG \_ version (0x00010003).

</dd> <dt>

<span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**
</dt> <dd>

Marcas de opciones que aparecen en la página de opciones de Unimodem. Este miembro puede ser una combinación de estos valores:

<dl> <dt>

<span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>TERMINAL \_ anterior (1)
</dt> <dd>

Muestra la pantalla del terminal anterior.

</dd> <dt>

<span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>POST de TERMINAL \_ (2)
</dt> <dd>

Muestra la pantalla posterior al terminal.

</dd> <dt>

<span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>\_Marcado manual (4)
</dt> <dd>

Marca el teléfono manualmente, si es capaz de hacerlo.

</dd> <dt>

<span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>Luces de lanzamiento \_ (8)
</dt> <dd>

Muestra el icono del módem en el área de estado de la barra de tareas.

De \_ forma predeterminada, solo se establece el valor de las luces de inicio.

</dd> </dl> </dd> <dt>

<span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**
</dt> <dd>

Número de segundos (en granularidad de dos segundos) para reemplazar la espera del tono de crédito ($).

</dd> <dt>

<span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**
</dt> <dd>

Estructura [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) que se puede usar con las funciones de configuración del módem y las comunicaciones.

</dd> </dl>

 

 
