---
title: Traza
description: El seguimiento usa el seguimiento de eventos Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Seguimiento de servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace571c2639ddd1eb55ed1e4afd70bcef7318b44
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882307"
---
# <a name="tracing"></a>Traza

El seguimiento usa el seguimiento de eventos Windows (ETW). Para aprovechar las herramientas de seguimiento disponibles con Windows Server 2008 R2, instale el SDK de Microsoft Windows desde el sitio [de descargas de MSDN.](https://www.microsoft.com/download/details.aspx?id=8279)


Hay tres niveles de seguimiento admitidos:

-   Detallado (todos los seguimientos disponibles).
-   Información (seguimientos informativos).
-   Error (seguimientos de errores).

Se sigue el seguimiento de los siguientes eventos:

-   Cualquier error (Level=Error, Level=Info o Level=Verbose).
-   Entrada/salida de una API (Level=Info o Level=Verbose).
-   Inicio y finalización de cualquier E/S (Level=Info o Level=Verbose)
-   Mensajes SOAP intercambiados (Level=Verbose, disponible en Windows 2003 SP1 y versiones posteriores)

## <a name="generating-and-viewing-wwsapi-traces"></a>Generación y visualización de seguimientos de WWSAPI

WWSAPI usa los eventos basados en manifiestos en Windows Vista y versiones posteriores. Como resultado, la experiencia de seguimiento tiene algunas diferencias en función de la versión del sistema operativo. La generación de seguimientos de ETW se puede realizar mediante las herramientas ETW de la caja en todas las plataformas compatibles. Sin embargo, para ver los seguimientos de ETW en un formato correcto se requieren herramientas personalizadas en Windows XP SP2 y Windows 2003 SP1. Hay varias maneras diferentes de recopilar y ver seguimientos de eventos ETW de WWSAPI en función de la versión del sistema operativo.

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a>Habilitación y visualización de seguimientos de WWSAPI en Visor de eventos (funciona en Windows Vista y versiones posteriores)

-   Ejecute eventvwr.msc desde la línea de comandos o el menú ejecutar.
-   Haga clic en el vínculo de vista en el panel Acciones de la derecha y habilite la opción Mostrar registros analíticos y de depuración.
-   Vaya a Application and Service Logs \\ Microsoft Windows WebServices providers (Registros de aplicaciones y servicios) de Microsoft en \\ \\ el panel izquierdo.
-   Haga clic con el botón derecho en el proveedor de seguimiento y seleccione Habilitar registro.
-   Ejecute el escenario.
-   Al actualizar la página del visor de eventos, debería empezar a ver las entradas de seguimiento de WWSAPI.

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a>Habilitación y visualización de seguimientos de WWSAPI Wstrace.bat Script (funciona en XPSP2 y versiones posteriores)

El wstrace.bat por lotes proporciona una manera cómoda de:

-   Creación de un registro de seguimiento
-   Eliminación de un registro de seguimiento
-   Habilitación y deshabilitación del seguimiento
-   Actualización del nivel de seguimiento (info/error/verbose)
-   Conversión de registros de seguimiento en archivos CSV

El archivo por lotes usa logman.exe para todos los comandos, a excepción de convertir los registros en un archivo CSV, lo que requiere una herramienta personalizada (wstracedump.exe).

## <a name="using-tracing-commands"></a>Uso de comandos de seguimiento

El comando siguiente crea un registro que usa información, error o nivel detallado. Este comando requiere privilegios elevados.

**wstrace.bat el \[ error de \| información \| detallado\]**

El comando siguiente elimina el registro. Este comando requiere privilegios elevados.

**wstrace.bat eliminar**

El comando siguiente habilita el seguimiento. Primero debe crear un registro.

**wstrace.bat en**

El nivel de seguimiento (información, error o detallado) se puede modificar de la siguiente manera:

**wstrace.bat información \[ de \| actualización detallada \|\]**

Para volcar la salida de seguimiento, use el siguiente comando:

**wstrace.bat volcado > temp.csv**

Los eventos se volcarán en el archivo CSV hasta que se presione Ctrl-C o se deshabilite el seguimiento.

## <a name="tracing-file-format"></a>Formato de archivo de seguimiento

Los archivos CSV creados por wstrace.bat archivos de texto simples de variables separadas por comas. Estos archivos se pueden abrir en Excel, Bloc de notas, etc.

Las columnas del archivo son las siguientes:

-   TimeStamp: marca de tiempo de cuando se registró el evento
-   ProcessID: identificador ULONG del proceso que registra el evento
-   ThreadID: identificador ULONG del subproceso que registra el evento
-   Evento: el valor enumerado del tipo de evento puede ser ("api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" \| "io \| started" "io completed" \| "io failed" \| "error" \| "received message start" \| "received message start" \| "received message stop" \| "sending message start" \| "sending message" "sending message \| stop")
-   Operación: el nombre de la operación que se invoca. Normalmente, esto se asigna a la API a la que se llama.
-   Error: número de error HRESULT opcional
-   Información: información opcional sobre el evento

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a>Recopilación del archivo de seguimiento ETW de WWSAPI mediante herramientas ETW (funciona en XPSP2 y versiones posteriores)

Habilitación del seguimiento de ETW para WWSAPI

**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices \[ \[ flags level \] \] \[ -o &lt; EtlLogFileName &gt; \] -ets**

para crear e iniciar la sesión de seguimiento de ETW. Logman.exe es una herramienta ETW de serie disponible en todas las plataformas compatibles. Tenga en cuenta que debe usar Microsoft Windows WebServices como nombre del proveedor en \_ \_ XPSP2 y W2K3. Puede ejecutar proveedores de consultas logman para ver la lista de proveedores registrados. El proveedor Microsoft-Windows-WebServices (o Microsoft \_ Windows WebServices) debe aparecer a menos que \_ no esté registrado. El proveedor se registra normalmente durante la instalación. Sin embargo, también se puede registrar manualmente ejecutando wevtutil.exe im ManifestFileName (en Windows Vista y versiones posteriores) o &lt; &gt; mofcomp.exe &lt; MofFileName &gt; (en XPSP2 y W2K3).

Las marcas se pueden usar para filtrar los seguimientos por su tipo. Puede ser el valor or de los siguientes tipos de seguimiento. Si no se proporciona, se habilitan todos los tipos de seguimiento.

-   0x1: seguimientos de entrada y salida de API.
-   0x2: seguimientos de errores.
-   0x4: seguimientos de E/S.
-   0x8: seguimientos de mensajes SOAP.
-   0x10: seguimientos de mensajes binarios.

Level se puede usar para filtrar los seguimientos por su nivel. Debe ser uno de los siguientes valores. Si no se proporciona, se habilitan todos los niveles de seguimiento.

-   0x1: seguimientos irreales.
-   0x2: seguimientos de errores.
-   0x3: seguimientos de advertencia.
-   0x4: seguimientos informativos.
-   0x5: seguimientos detallados.

EtlLogFileName es la ruta de acceso al archivo de registro de eventos ETW que se va a crear (use la extensión .etl). Si no se proporciona, ETW elegirá un nombre aleatorio que se puede consultar más adelante. Este archivo no debe residir en el directorio de perfil del usuario. El archivo de registro de eventos ETW (archivo .etl) está en formato binario. Las aplicaciones ETW pueden consumirla, pero no en formato legible para el usuario. En el paso siguiente se describe cómo ver su contenido.

Ejecución del escenario

Recopilación del archivo de registro de eventos ETW.

**logman stop wstrace -ets**

para detener la sesión de seguimiento de ETW. Esto es cuando ETW deja de registrar los eventos. El archivo de registro de eventos ETW (especificado en el parámetro EtlLogFileName) está listo para consumirse. Se puede ver localmente (se proporcionan instrucciones a continuación) o enviarse al grupo de productos para su investigación.

Ejemplo de un extremo a otro mediante las herramientas etw:

**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices -o mytrace.etl -ets**

**Eco.. ejecute el escenario.**

**logman stop wstrace -ets**

**tracerpt mytrace.etl -o mytrace.xml**

**wstrace.htm**

**Eco.. use mytrace.xml y wstrace.xsl en la página abierta.**

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a>Visualización de seguimientos de archivos de seguimiento ETW de WWSAPI wstracedump.exe herramienta (funciona en Windows XP y versiones posteriores)

Wstracedump.exe es una herramienta de consumidor ETW desarrollada personalizada que procesa eventos en el archivo de seguimiento ETW de WWSAPI y genera resultados legibles por el usuario. Puede generar resultados de todas las plataformas admitidas. Consulte su uso (wstracedump.exe -?) para obtener más información.

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a>Visualización de seguimientos de archivos de seguimiento ETW de WWSAPI mediante herramientas ETW (funciona en Windows Vista y versiones posteriores)

Tracerpt.exe es la herramienta para ver el contenido de un archivo de registro de eventos ETW y disponible en todas las plataformas compatibles. Se puede usar para generar archivos de volcado CSV, EVTX o XML a partir de un archivo de registro de eventos ETW. Sin embargo, el archivo de salida generado tiene seguimientos legibles humanos solo en Windows Vista y versiones posteriores. En estas instrucciones se describe cómo generar el archivo de volcado XML y usarlo junto con un archivo xsl para mostrar los seguimientos en un formato correcto (el archivo xsl es muy trivial y se puede modificar si se desean formatos diferentes).

-   Ejecutar

    **tracerpt &lt; EtlLogFileName &gt; -o &lt; OutputXMLFileName&gt;**

    para crear un volcado XML a partir del archivo ETL binario (tracerpt.exe el archivo de salida en formato XML de forma predeterminada. Ejecute tracerpt -? Para ver otros formatos disponibles).

-   En este momento, puede ver la información de seguimiento en el archivo XML. Además, puede abrir el archivo wstrace.htm y usar el archivo de volcado xml y el archivo wstrace.xsl para ver los seguimientos en un formato mejor. Tenga en cuenta que los archivos deben estar en el equipo local para poder usar este archivo HTML en IE.

## <a name="security"></a>Seguridad

Al habilitar el seguimiento, los administradores deben tener en cuenta que consume espacio en disco adicional y potencia de cálculo. Un cliente o aplicación malintencionados puede agotar los recursos del sistema a menos que la configuración de seguimiento esté configurada con límites razonables. Al usar la característica de seguimiento de mensajes, los mensajes que transportan información confidencial, como credenciales, información personal, etc., pueden conservarse en el disco o ser vistos por cualquier persona que tenga acceso al visor de eventos del sistema. Como mitigación de este problema, los usuarios del sistema o administrador pueden habilitar el seguimiento en Windows 2003 y versiones posteriores. El seguimiento de mensajes está deshabilitado Windows XP en el que cualquier usuario puede activar el seguimiento.

La enumeración siguiente se usa con el seguimiento:

-   [**API DE SEGUIMIENTO DE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




