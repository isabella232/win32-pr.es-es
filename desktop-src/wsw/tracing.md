---
title: Traza
description: El seguimiento utiliza el seguimiento de eventos para Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Seguimiento de servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c660884667cefae8067376075a30cbc41f70d4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421635"
---
# <a name="tracing"></a>Seguimiento

El seguimiento utiliza el seguimiento de eventos para Windows (ETW). Para beneficiarse de las herramientas de seguimiento disponibles con Windows Server 2008 R2, instale el Microsoft Windows SDK desde el sitio de [descargas de MSDN](https://www.microsoft.com/download/details.aspx?id=8279) .


Se admiten tres niveles de seguimiento:

-   Detallado (todos los seguimientos disponibles).
-   Info (seguimientos informativos).
-   Error (seguimientos de errores).

Se realiza un seguimiento de los siguientes eventos:

-   Cualquier error (LEVEL = error, Level = info o LEVEL = verbose).
-   Entrada/salida de una API (LEVEL = info o LEVEL = verbose).
-   Inicio y finalización de cualquier e/s (LEVEL = info o LEVEL = verbose)
-   Mensajes SOAP intercambiados (LEVEL = verbose, disponible en Windows 2003 SP1 y versiones posteriores)

## <a name="generating-and-viewing-wwsapi-traces"></a>Generar y ver seguimientos de WWSAPI

WWSAPI usa los eventos basados en manifiesto en Windows Vista y versiones posteriores. Como resultado, la experiencia de seguimiento tiene algunas diferencias en función de la versión del sistema operativo. La generación de seguimientos de ETW se puede realizar mediante las herramientas de ETW integradas en todas las plataformas compatibles. Sin embargo, la visualización de los seguimientos de ETW en un formato agradable requiere herramientas personalizadas en Windows XP SP2 y Windows 2003 SP1. Hay algunas maneras diferentes de recopilar y ver los seguimientos de eventos ETW de WWSAPI en función de la versión del sistema operativo.

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a>Habilitar y ver seguimientos de WWSAPI en Visor de eventos (funciona en Windows Vista y versiones posteriores)

-   Ejecute eventvwr. msc desde la línea de comandos o desde el menú ejecutar.
-   Haga clic en el vínculo ver del panel acciones de la derecha y habilite la opción Mostrar registros analíticos y de depuración.
-   Vaya a registros de aplicaciones y \\ servicios \\ \\ proveedores de servicios de Microsoft Windows en el panel izquierdo.
-   Haga clic con el botón derecho en el proveedor de seguimiento y seleccione Habilitar registro.
-   Ejecute el escenario.
-   Al actualizar la página del visor de eventos, debería empezar a ver las entradas de seguimiento de WWSAPI.

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a>Habilitación y visualización de seguimientos de WWSAPI mediante Wstrace.bat script (Works en XPSP2 y versiones posteriores)

El archivo por lotes wstrace.bat proporciona una manera cómoda de:

-   Crear un registro de seguimiento
-   Eliminar un registro de seguimiento
-   Habilitar y deshabilitar el seguimiento
-   Actualizar el nivel de seguimiento (info/error/verbose)
-   Convertir registros de seguimiento en archivos CSV

El archivo por lotes usa logman.exe para todos los comandos, a excepción de la conversión de los registros a un archivo CSV, que requiere una herramienta personalizada (wstracedump.exe).

## <a name="using-tracing-commands"></a>Usar comandos de seguimiento

El siguiente comando crea un registro que usa información, un error o un nivel detallado. Este comando requiere privilegios elevados.

**wstrace.bat Create \[ info \| error \| verbose\]**

El siguiente comando elimina el registro. Este comando requiere privilegios elevados.

**wstrace.bat eliminar**

El siguiente comando habilita el seguimiento. Primero debe crear un registro.

**wstrace.bat en**

El nivel de seguimiento (info, error o verbose) se puede modificar de la siguiente manera:

**wstrace.bat error de información de actualización \[ \| \| detallado\]**

Para volcar la salida del seguimiento, use el siguiente comando:

**wstrace.bat > de volcado de memoria temp.csv**

Los eventos se volcarán en el archivo CSV hasta que se presione Ctrl + C o se deshabilite el seguimiento.

## <a name="tracing-file-format"></a>Formato de archivo de seguimiento

Los archivos CSV creados por wstrace.bat son archivos de texto de variables separadas por comas simples. Estos archivos se pueden abrir en Excel, Bloc de notas, etc.

Las columnas del archivo son las siguientes:

-   Marca de tiempo de fecha y hora en que se registró el evento
-   ProcessID-ULONG ID. del proceso que registra el evento
-   ThreadID: ID. de ULONG del subproceso que registra el evento
-   El valor enumerado de eventos del tipo de evento puede ser ("API Enter" \| "API Pending" "API ExitSyncSuccess" "API ExitSyncFailure" "API \| \| \| ExitAsyncSuccess" \| "API ExitAsyncFailure" " \| IO Started" " \| e/s completada" "error de \| e/s" " \| error" "recepción de \| mensaje recibido" \| "mensaje recibido" "se \| ha recibido el mensaje \| \| \| "
-   Operación: el nombre de la operación que se va a invocar. Normalmente, se asigna a la API a la que se llama.
-   Error: número de error opcional de HRESULT
-   Info: información opcional sobre el evento

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a>Recopilación del archivo de seguimiento de ETW de WWSAPI con las herramientas de ETW (funciona en XPSP2 y versiones posteriores)

Habilitación del seguimiento de ETW para WWSAPI

**Logman Start wstrace-BS 64-ft 1-RT-p Microsoft-Windows-webservices \[ Flags \[ LEVEL \] \] \[ -o <EtlLogFileName> \] -ETS**

para crear e iniciar la sesión de seguimiento de ETW. Logman.exe es una herramienta de ETW integrada disponible en todas las plataformas compatibles. Tenga en cuenta que debe usar \_ \_ los servicios WebService de Microsoft Windows como nombre del proveedor en xpsp2 y W2K3. Puede ejecutar los proveedores de consultas Logman para ver la lista de proveedores registrados. El proveedor Microsoft-Windows-WebServices (o Microsoft \_ Windows \_ WebServices) debe aparecer en la lista a menos que no esté registrado. Normalmente, el proveedor se registra durante la instalación. Sin embargo, también se puede registrar manualmente mediante la ejecución de wevtutil.exe im <ManifestFileName> (en Windows Vista y versiones posteriores) o mofcomp.exe <MofFileName> (en xpsp2 y W2K3).

Las marcas se pueden utilizar para filtrar los seguimientos por su tipo. Puede ser o ser el valor de los siguientes tipos de seguimiento. Si no se proporciona, se habilitan todos los tipos de seguimiento.

-   0x1: seguimientos de entrada y salida de la API.
-   0X2: seguimientos de errores.
-   0x4: seguimientos de e/s.
-   0x8: seguimientos de mensajes SOAP.
-   0x10: seguimientos de mensajes binarios.

El nivel se puede usar para filtrar los seguimientos por su nivel. Debe ser uno de los valores siguientes. Si no se proporciona, se habilitan todos los niveles de seguimiento.

-   0x1-seguimientos irrecuperables.
-   0X2: seguimientos de errores.
-   0X3: seguimientos de advertencia.
-   0x4: seguimientos informativos.
-   0X5: seguimientos detallados.

EtlLogFileName es la ruta de acceso al archivo de registro de eventos ETW que se va a crear (use la extensión. ETL). Si no se proporciona, ETW elegirá un nombre aleatorio que se puede consultar más adelante. Este archivo no debe residir en el directorio del perfil del usuario. El archivo de registro de eventos ETW (archivo. ETL) está en formato binario. Puede ser utilizado por aplicaciones ETW, pero no está en formato legible. El paso siguiente describe cómo ver su contenido.

Ejecutar el escenario

Recopilando archivo de registro de eventos ETW.

**Logman STOP wstrace-ETS**

para detener la sesión de seguimiento de ETW. Es cuando ETW detiene el registro de eventos. El archivo de registro de eventos ETW (especificado en el parámetro EtlLogFileName) está listo para consumir. Puede verse localmente (las instrucciones se proporcionan a continuación) o enviarse al grupo de productos para su investigación.

Ejemplo de un extremo a otro con las herramientas de ETW:

**Logman Start wstrace-BS 64-ft 1-RT-p Microsoft-Windows-webservices-o mi Trace. ETL-ETS**

**echo... Ejecute el escenario.**

**Logman STOP wstrace-ETS**

**tracerpt sutrace. ETL-o mytrace.xml**

**wstrace.htm**

**echo... Utilice mytrace.xml y wstrace. xsl en la página abierta.**

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a>Ver seguimientos de archivos de seguimiento de WWSAPI ETW mediante wstracedump.exe Tool (funciona en Windows XP y versiones posteriores)

Wstracedump.exe es una herramienta de consumidor de ETW desarrollada personalizada que procesa los eventos en el archivo de seguimiento de ETW de WWSAPI y genera una salida legible para el usuario. Puede generar resultados de todas las plataformas admitidas. Para obtener más información, vea su uso (wstracedump.exe-?).

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a>Ver seguimientos de archivos de seguimiento de WWSAPI ETW mediante las herramientas de ETW (funciona en Windows Vista y versiones posteriores)

Tracerpt.exe es la herramienta para ver el contenido de un archivo de registro de eventos ETW y disponible en todas las plataformas admitidas. Se puede utilizar para generar archivos de volcado de memoria de CSV, EVTX o XML a partir de un archivo de registro de eventos ETW. Sin embargo, el archivo de salida generado solo tiene seguimientos legibles para el usuario en Windows Vista y versiones posteriores. Estas instrucciones describen cómo generar el archivo de volcado XML y usarlo junto con un archivo XSL para mostrar los seguimientos en un formato bonito (el archivo XSL es muy trivial y se puede modificar si se quieren formatos diferentes).

-   Ejecutar

    **tracerpt <EtlLogFileName> -o <OutputXMLFileName>**

    para crear un volcado XML a partir del archivo ETL binario (tracerpt.exe crea el archivo de salida en formato XML de forma predeterminada. Ejecute tracerpt-? Para ver otros formatos disponibles).

-   Llegados a este punto, puede ver la información de seguimiento en el archivo XML. Además, puede abrir el archivo wstrace.htm y utilizar el archivo de volcado de memoria XML y el archivo wstrace. xsl para ver los seguimientos en un formato más agradable. Tenga en cuenta que los archivos deben estar en el equipo local para poder usar este archivo HTML en Internet Explorer.

## <a name="security"></a>Seguridad

Al habilitar el seguimiento, los administradores deben tener en cuenta que consume espacio en disco adicional y potencia de cálculo. Un cliente o aplicación malintencionado puede agotar los recursos del sistema a menos que la configuración de seguimiento se configure con límites razonables. Al usar la característica de seguimiento de mensajes, los mensajes que llevan información confidencial, como las credenciales, la información personal, etc., pueden persistir en el disco o ser vistos por cualquier persona que tenga acceso al visor de eventos del sistema. Como mitigación de este problema, los usuarios del sistema o administradores pueden habilitar el seguimiento en Windows 2003 y versiones posteriores. El seguimiento de mensajes está deshabilitado en Windows XP en el que cualquier usuario puede activar el seguimiento.

La siguiente enumeración se usa con el seguimiento:

-   [**\_API de seguimiento de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




