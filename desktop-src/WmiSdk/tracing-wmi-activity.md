---
description: A partir de Windows Vista, el servicio WMI no utiliza los archivos de registro de WMI. En su lugar, utiliza el seguimiento de eventos para Windows (ETW) y los eventos están disponibles a través de Visor de eventos o la herramienta de línea de comandos wevtutil.
ms.assetid: bb6401e8-caf7-4f39-ab64-b7532723ce9a
ms.tgt_platform: multiple
title: Seguimiento de la actividad WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14371a4f18b81019073cd2b428500b12385719e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815699"
---
# <a name="tracing-wmi-activity"></a>Seguimiento de la actividad WMI

A partir de Windows Vista, el servicio WMI no utiliza los [archivos de registro de WMI](wmi-log-files.md). En su lugar, utiliza el [seguimiento de eventos para Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) y los eventos están disponibles a través de **visor de eventos** o la herramienta de línea de comandos wevtutil.

En este tema se describen las siguientes secciones:

-   [Obtención de eventos de WMI a través de Visor de eventos](#obtaining-wmi-events-through-event-viewer)
-   [Habilitación del seguimiento de WMI en el símbolo del sistema](#enabling-wmi-tracing-at-command-prompt)
-   [Uso del seguimiento de WMI basado en WPP](#using-wpp-based-wmi-tracing)
-   [Temas relacionados](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a>Obtención de eventos de WMI a través de Visor de eventos

El archivo WMITracing. log contiene los eventos de seguimiento de WMI. Sin embargo, se trata de un archivo binario. Para ver estos eventos en un formato legible por los usuarios, use el **visor de eventos**.

De forma predeterminada, no se realiza un seguimiento de los eventos WMI. En este procedimiento se describe cómo usar **visor de eventos** para habilitar el seguimiento de eventos WMI y buscar eventos WMI. Puede realizar las mismas operaciones a través de la herramienta de línea de comandos wevtutil.

**Para ver eventos WMI en Visor de eventos**

1.  Abra **Visor de eventos**. En el menú **Vista**, haga clic en **Mostrar registros analíticos y de depuración**. Busque el registro del canal de **seguimiento** para WMI en registros de aplicaciones y servicios \| actividad de WMI de Microsoft \| Windows \| .
2.  Haga clic con el botón secundario en el registro de **seguimiento** y seleccione **propiedades del registro**. Haga clic en la casilla **Habilitar registro** para iniciar el seguimiento de eventos WMI. Para obtener más información acerca de los canales, consulte [registros de eventos y canales en el registro de eventos de Windows](/previous-versions//aa385225(v=vs.85)).
3.  Los eventos WMI aparecen en la ventana de eventos para **la actividad WMI**. Haga doble clic en un evento de la lista para ver la información detallada. Puede ver un evento en la **vista XML** o en un formato de **vista descriptivo** .

El campo ID. de **evento** muestra un valor que contiene la siguiente información.

<dl> <dt>

<span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Evento 1
</dt> <dd>

Inicio de la secuencia de eventos para una operación específica. Una repetición para cada secuencia.

Los campos de evento para un evento 1 son:

-   **GroupOperationID** es un identificador único que se usa para todos los eventos informados para un cliente específico.
-   **OperationId** indica la secuencia de la operación.
-   **Operación** especifica la conexión o la solicitud a WMI.
-   El **usuario** indica la cuenta que realiza una solicitud a WMI mediante la ejecución de un script o de CIM Studio.
-   **Espacio de nombres** muestra el espacio de nombres WMI en el que se realiza la conexión.

Por ejemplo, un script puede solicitar todas las instancias de una clase WMI, como el [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service). La primera operación puede ser una conexión a WMI.

</dd> <dt>

<span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Evento 2
</dt> <dd>

Eventos que componen la operación. Una o más repeticiones de la secuencia.

Los campos de evento para un evento 2 son:

-   **GroupOperationID** indica la secuencia en la que se produce el evento.
-   **GroupOperationID** indica la secuencia en la que se produce el evento.
-   **ProviderName** indica el nombre del proveedor que proporciona los datos.
-   **Path** es la ruta de acceso WMI al objeto.

Por ejemplo, la operación puede ser una enumeración [**del \_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

<span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Evento 3
</dt> <dd>

Final de la secuencia de eventos para una operación específica. Una repetición para cada secuencia.

Solo se muestra el **GroupOperationID** .

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a>Habilitación del seguimiento de WMI en el símbolo del sistema

También puede habilitar el seguimiento de eventos WMI mediante la herramienta de línea de comandos wevtutil. Use el comando siguiente: **Wevtutil.exe SL Microsoft-Windows-WMI-Activity/Trace/e: true**. El origen del evento WMI es Microsoft-Windows-WMI. Para obtener más información acerca de Wevtutil.exe, consulte [acerca del registro de eventos de Windows](/previous-versions//aa382610(v=vs.85)).

## <a name="using-wpp-based-wmi-tracing"></a>Uso del seguimiento de WMI basado en WPP

En los sistemas operativos Windows a partir de Windows Vista, WMI crea un canal de seguimiento activo durante el proceso de arranque. El nombre del canal es sesión de \_ seguimiento de WMI \_ . Solo los errores se registran en el canal.

El preprocesador de seguimiento de software de Windows (WPP) registra información en un archivo binario. Para leer el archivo, primero debe convertirlo a un formato de texto legible. Use una herramienta llamada tracefmt.exe del kit de [controladores de Windows (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) para realizar la traducción. La herramienta requiere información almacenada en algunos archivos asociados. Los archivos se encuentran en el directorio% SystemRoot% \\ system32 \\ WBEM \\ TMF y tienen una extensión de nombre de archivo. TMF. La herramienta realmente requiere un único archivo. TMF. Para hacerlo, se concatenan todos los archivos. TMF en otro archivo. TMF. Para obtener más información acerca de los archivos. TMF, vea [archivo de formato de mensaje de seguimiento](/windows-hardware/drivers/devtest/trace-message-format-file).

Después de instalar [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) para obtener las herramientas de línea de comandos tracelog.exe y tracefmt.exe, realice los pasos siguientes para recopilar un seguimiento WMI basado en WPP.

**Para ver un seguimiento WMI basado en WPP**

1.  Para crear el archivo. TMF único, abra una ventana de símbolo del sistema con privilegios elevados y navegue hasta el directorio% SystemRoot% \\ system32 \\ WBEM \\ TMF

2.  Escriba **Copy/y% SystemRoot% \\ system32 \\ WBEM \\ TMF \\ \* . TMF% SystemRoot% \\ system32 \\ WBEM \\ TMF \\ WMI. TMF**. Se creará un archivo denominado WMI. TMF que incluye el contenido de todos los demás archivos. TMF.

3.  Escriba **tracelog-vaciar \_ la \_ sesión de seguimiento WMI**. Esto hará que se vacíen los búferes WPP en el disco.
4.  Escriba **set Trace \_ format \_ prefix = \[ %9! d! \] %8! 04X!. %3! 04X!. %3! 04X!:: %4! s! \[ %1! s! \] (%! COMPNAME!:%! FUNC!: %2! s!)**. La herramienta tracefmt agrega información predeterminada a cada mensaje de seguimiento. Para configurar la información que se incluye, establezca la \_ variable de \_ entorno prefijo de formato de seguimiento. Para obtener información sobre la sintaxis usada, consulte [Prefijo de mensaje de seguimiento](https://msdn.microsoft.com/library/aa139695.aspx).
5.  Escriba **tracefmt-TMF% SystemRoot% \\ system32 \\ WBEM \\ TMF \\ wmi. TMF-o OUTPUT.TXT% SystemRoot% \\ system32 \\ WBEM \\ logs \\ WMITracing. log**. Esto realiza la traducción desde el formato binario al formato de texto legible.
6.  Escriba **Notepad% SystemRoot% \\ system32 \\ WBEM \\ TMF \\OUTPUT.TXT**. Se abrirá el archivo de seguimiento en el Bloc de notas.

A continuación se indican algunas de las tareas relacionadas con WPP que podría necesitar realizar.

**Para detener el seguimiento de WMI basado en WPP**

-   Escriba **tracelog-STOP WMI \_ Trace \_ Session**.

**Para iniciar el seguimiento WMI basado en WPP**

-   Escriba **tracelog-Start WMI \_ Trace \_ Session-GUID \# 1FF6B227-2CA7-40f9-9A66-980EADAA602E-RT-LEVEL 5-Flag 0X7-f @ Trace. BIN**

**Windows Vista:** De forma predeterminada, el seguimiento de WMI basado en WPP se establece en el nivel 2, que incluye solo los mensajes de error. Para incluir también los mensajes informativos, establezca el nivel en 4. Se realiza un seguimiento de todas las áreas de WMI de forma predeterminada. Hay tres áreas distintas de las que se puede realizar un seguimiento: Core (flag = 0x1), ESS (flag = 0X2) y Prov (flag = 0x4). En el comando iniciar anterior, la **marca 0X7** hace que se haga un seguimiento de las tres áreas.

**Windows 7:** De forma predeterminada, el seguimiento de WMI basado en WPP está deshabilitado y establecido en el nivel 0. Para usar el seguimiento WMI basado en WPP, esta característica debe estar habilitada y establecida en el nivel 2 para los mensajes de error o el nivel 4 para los mensajes de error e informativos.

**Para enumerar todas las sesiones de seguimiento WPP**

-   Escriba **tracelog-l**.

**Para mostrar información acerca de la sesión de seguimiento WPP de WMI**

-   Escriba **tracelog-l \| Findstr/i "WMI \_ trace"**.

**Para ver los parámetros de la sesión de seguimiento WPP de WMI**

-   Escriba **tracelog-q \_ \_ sesión de seguimiento de WMI**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Archivos de registro de WMI](wmi-log-files.md)
</dt> </dl>

 

 
