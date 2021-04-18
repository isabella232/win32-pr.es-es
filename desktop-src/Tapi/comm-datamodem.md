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
# <a name="commdatamodem"></a><span data-ttu-id="a6dd3-103">COMM/telemodem</span><span class="sxs-lookup"><span data-stu-id="a6dd3-103">comm/datamodem</span></span>

<span data-ttu-id="a6dd3-104">La clase de dispositivo COMM/telemodem consta de los dispositivos de módem.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-104">The comm/datamodem device class consists of datamodem devices.</span></span> <span data-ttu-id="a6dd3-105">Puede tener acceso a estos dispositivos mediante las funciones de [archivo](/windows/desktop/FileIO/file-management-functions) y de [comunicaciones](/windows/desktop/DevIO/communications-functions).</span><span class="sxs-lookup"><span data-stu-id="a6dd3-105">You access these devices by using the [file](/windows/desktop/FileIO/file-management-functions) and [communications functions](/windows/desktop/DevIO/communications-functions).</span></span> <span data-ttu-id="a6dd3-106">Los dispositivos de esta clase están asociados a los dispositivos de línea que admiten el tipo de medio de LINEMEDIAMODE de los \_ archivos de módem, que se especifica en el miembro **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_DATAMODEM media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="a6dd3-107">La función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando estos miembros adicionales:</span><span class="sxs-lookup"><span data-stu-id="a6dd3-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to the STRINGFORMAT\_BINARY value and appending these additional members:</span></span>

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

<span data-ttu-id="a6dd3-108">El miembro **hComm** es el identificador del puerto de comunicaciones abierto.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-108">The **hComm** member is the handle of the open communications port.</span></span> <span data-ttu-id="a6dd3-109">Este miembro es **null** si el puerto todavía no está abierto o si el parámetro *dwSelect* de [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) no es el \_ valor de llamada LINECALLSELECT.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-109">This member is **NULL** if the port is not yet open or if the *dwSelect* parameter of [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) is not the LINECALLSELECT\_CALL value.</span></span> <span data-ttu-id="a6dd3-110">Si una llamada está activa, el proveedor de servicios normalmente abre el propio puerto para obtener el control directo del hardware de comunicaciones, pero solo es necesario devolver un identificador válido si la línea está conectada.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-110">If a call is active, the service provider typically opens the port itself to get direct control of the communications hardware, but is only required to return a valid handle if the line is connected.</span></span> <span data-ttu-id="a6dd3-111">El proveedor de servicios abre el puerto con el \_ valor de indicador de archivo \_ superpuesto y, a continuación, configura el puerto con la configuración especificada por la función [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .</span><span class="sxs-lookup"><span data-stu-id="a6dd3-111">The service provider opens the port using the FILE\_FLAG\_OVERLAPPED value and then configures the port using the settings specified by the [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) function.</span></span> <span data-ttu-id="a6dd3-112">Puede establecer opciones de configuración adicionales para el dispositivo mediante el uso de funciones de comunicaciones con el identificador devuelto.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-112">You can set additional configuration options for the device by using communications functions with the returned handle.</span></span>

<span data-ttu-id="a6dd3-113">El miembro **szDeviceName** es una cadena terminada en **null** que especifica el nombre del puerto de comunicaciones asociado a la línea, dirección o llamada.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-113">The **szDeviceName** member is a **null**-terminated string that specifies the name of the communications port associated with the line, address, or call.</span></span>

<span data-ttu-id="a6dd3-114">Si **hComm** es un identificador válido, puede usarlo en llamadas subsiguientes a funciones de archivo, como [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), para enviar y recibir datos en la llamada.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-114">If **hComm** is a valid handle, you can use it in subsequent calls to file functions, such as [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), to send and receive data on the call.</span></span> <span data-ttu-id="a6dd3-115">Cuando haya terminado de usar el puerto de comunicaciones y preferiblemente antes de usar la función [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) para desasignar la llamada, debe cerrar el puerto mediante la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="a6dd3-115">When you are finished using the communications port and preferably before you use the [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) function to deallocate the call, you must close the port by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="a6dd3-116">Cuando se usan las funciones [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) y [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) , algunos proveedores de servicios requieren que los datos de configuración de esta clase de dispositivo tengan el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="a6dd3-116">When using the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions, some service providers require that the configuration data for this device class have the following format:</span></span>

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

<span data-ttu-id="a6dd3-117">A continuación se proporciona información de configuración de dispositivos para su uso con las funciones [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) y [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .</span><span class="sxs-lookup"><span data-stu-id="a6dd3-117">The following is device configuration information for use with the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions.</span></span>

<dl> <dt>

<span data-ttu-id="a6dd3-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="a6dd3-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="a6dd3-119">Suma del tamaño de la estructura **DEVCFGHDR** y el tamaño real de la estructura [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) .</span><span class="sxs-lookup"><span data-stu-id="a6dd3-119">Sum of the size of the **DEVCFGHDR** structure and the actual size of the [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a6dd3-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="a6dd3-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a6dd3-121">Número de versión de la estructura **DevConfig** de Unimodem.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-121">Version number of the Unimodem **DevConfig** structure.</span></span> <span data-ttu-id="a6dd3-122">Este miembro puede ser MDMCFG \_ version (0x00010003).</span><span class="sxs-lookup"><span data-stu-id="a6dd3-122">This member can be MDMCFG\_VERSION (0x00010003).</span></span>

</dd> <dt>

<span data-ttu-id="a6dd3-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**</span><span class="sxs-lookup"><span data-stu-id="a6dd3-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**</span></span>
</dt> <dd>

<span data-ttu-id="a6dd3-124">Marcas de opciones que aparecen en la página de opciones de Unimodem.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-124">Option flags that appear on the Unimodem Option page.</span></span> <span data-ttu-id="a6dd3-125">Este miembro puede ser una combinación de estos valores:</span><span class="sxs-lookup"><span data-stu-id="a6dd3-125">This member can be a combination of these values:</span></span>

<dl> <dt>

<span data-ttu-id="a6dd3-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>TERMINAL \_ anterior (1)</span><span class="sxs-lookup"><span data-stu-id="a6dd3-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>TERMINAL\_PRE (1)</span></span>
</dt> <dd>

<span data-ttu-id="a6dd3-127">Muestra la pantalla del terminal anterior.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-127">Displays the pre-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="a6dd3-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>POST de TERMINAL \_ (2)</span><span class="sxs-lookup"><span data-stu-id="a6dd3-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>TERMINAL\_POST (2)</span></span>
</dt> <dd>

<span data-ttu-id="a6dd3-129">Muestra la pantalla posterior al terminal.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-129">Displays the post-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="a6dd3-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>\_Marcado manual (4)</span><span class="sxs-lookup"><span data-stu-id="a6dd3-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>MANUAL\_DIAL (4)</span></span>
</dt> <dd>

<span data-ttu-id="a6dd3-131">Marca el teléfono manualmente, si es capaz de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-131">Dials the phone manually, if capable of doing so.</span></span>

</dd> <dt>

<span data-ttu-id="a6dd3-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>Luces de lanzamiento \_ (8)</span><span class="sxs-lookup"><span data-stu-id="a6dd3-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>LAUNCH\_LIGHTS (8)</span></span>
</dt> <dd>

<span data-ttu-id="a6dd3-133">Muestra el icono del módem en el área de estado de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-133">Displays the modem icon in the status area of the taskbar.</span></span>

<span data-ttu-id="a6dd3-134">De \_ forma predeterminada, solo se establece el valor de las luces de inicio.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-134">Only the LAUNCH\_LIGHTS value is set by default</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a6dd3-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**</span><span class="sxs-lookup"><span data-stu-id="a6dd3-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**</span></span>
</dt> <dd>

<span data-ttu-id="a6dd3-136">Número de segundos (en granularidad de dos segundos) para reemplazar la espera del tono de crédito ($).</span><span class="sxs-lookup"><span data-stu-id="a6dd3-136">Number of seconds (in two seconds granularity) to replace the wait for credit tone ($).</span></span>

</dd> <dt>

<span data-ttu-id="a6dd3-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**</span><span class="sxs-lookup"><span data-stu-id="a6dd3-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**</span></span>
</dt> <dd>

<span data-ttu-id="a6dd3-138">Estructura [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) que se puede usar con las funciones de configuración del módem y las comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="a6dd3-138">[**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure that can be used with the communications and modem configuration functions.</span></span>

</dd> </dl>

 

 
