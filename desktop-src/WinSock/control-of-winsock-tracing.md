---
description: .
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Control de seguimiento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910b15ece4581525fddc25213c630e24d0e49110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705642"
---
# <a name="control-of-winsock-tracing"></a>Control de seguimiento de Winsock

El seguimiento de Winsock se puede controlar mediante cualquiera de los métodos siguientes:

-   Herramientas de línea de comandos

    En Windows Vista y Windows Server 2008 se incluyen dos herramientas de línea de comandos que se usan para controlar el seguimiento y convertir el archivo de registro de seguimiento binario en texto legible.

    La herramienta de **logman.exe** se utiliza para iniciar o detener el seguimiento de Winsock.

    La herramienta de **tracerpt.exe** se utiliza para convertir el archivo de registro de seguimiento binario en un archivo de texto legible.

-   Visor de eventos

    El Visor de eventos en Windows Vista y versiones posteriores también puede usarse para habilitar el seguimiento de Winsock. El Visor de eventos es accesible bajo Herramientas administrativas en el menú Inicio.

## <a name="using-logman-and-tracert"></a>Usar Logman y tracert

El seguimiento de eventos de red Winsock está deshabilitado de forma predeterminada en Windows Vista y versiones posteriores.

El comando siguiente inicia el seguimiento de eventos de red Winsock en un equipo, establece el nombre de la sesión de seguimiento de eventos en mywinsocksession y envía la salida a un archivo de registro binario denominado winsocklogfile. ETL:

**Logman Start-ETS mywinsocksession-o winsocklogfile. ETL-p Microsoft-Windows-Winsock-AFD**

Los archivos de registro se crean en el directorio actual con nombres de archivo con el formato winsocklogfile \_ 000001. ETL.

El comando siguiente detiene el seguimiento de Winsock anterior en un equipo para la sesión denominada mywinsocksession:

**Logman STOP-ETS mywinsocksession**

Un archivo de registro binario se escribirá en la ubicación especificada por el parámetro – o. Para traducir el archivo binario en un archivo de texto legible, se usa **tracerpt.exe** :

**tracerpt.exe <nombre del archivo. ETL> – o winsocktracelog.txt**

Si se prefiere un archivo de salida que contenga XML en lugar de texto sin formato, se utiliza el comando siguiente:

**tracerpt.exe <nombre del archivo. ETL> – o winsocktracelog.xml: de XML**

El seguimiento de cambios del catálogo Winsock está habilitado de forma predeterminada en Windows Vista y versiones posteriores.

> [!Note]  
> Los proveedores de servicios superpuestos están desusados. A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).

 

El comando siguiente inicia el seguimiento de cambios del catálogo Winsock para los proveedores de servicios por capas (LSP) en un equipo, establece el nombre de la sesión de seguimiento de eventos en mywinsockcatalogsession y envía la salida a un archivo de registro binario denominado winsockcataloglogfile. ETL:

**Logman Start-ETS mywinsockcatalogsession-o winsockcataloglogfile. ETL-p Microsoft-Windows-Winsock-WS2HELP**

Los archivos de registro se crean en el directorio actual con nombres de archivo con el formato winsockcataloglogfile \_ 000001. ETL.

El comando siguiente detiene el seguimiento de Winsock anterior en un equipo para la sesión denominada mi sesión:

**Logman STOP-ETS mywinsockcatalogsession**

Un archivo de registro binario se escribirá en la ubicación especificada por el parámetro – o. Para traducir el archivo binario en un archivo de texto legible, se usa **tracerpt.exe** :

**tracerpt.exe <nombre del archivo. ETL> – o winsockcatalogtracelog.txt**

Si se prefiere un archivo de salida que contenga XML en lugar de texto sin formato, se utiliza el comando siguiente:

**tracerpt.exe <nombre del archivo. ETL> – o winsockcatalogtracelog.xml: de XML**

## <a name="using-event-viewer-to-start-winsock-network-event-tracing"></a>Uso de Visor de eventos para iniciar el seguimiento de eventos de red Winsock

Al abrir Visor de eventos, el panel izquierdo contiene la lista de eventos. Abra **registros de aplicaciones y servicios** , vaya a **Microsoft \\ Windows \\ Winsock Network Event** como origen y seleccione **operativo**.

En el panel acción, seleccione **propiedades de registro** y active la casilla **Habilitar registro** . Una vez habilitado el registro, también puede cambiar el tamaño del archivo de registro si es necesario.

Ahora está habilitado el seguimiento de eventos de red Winsock y todo lo que necesita hacer es la acción actualizar para actualizar la lista de eventos que se han registrado. Para detener el registro, simplemente desactive el mismo botón de radio.

Es posible que tenga que aumentar el tamaño del registro en función del número de eventos que desee ver. Un inconveniente de usar la Visor de eventos para el seguimiento de Winsock es que no carga todos los recursos de cadena, por lo que los mensajes que se muestran en el campo de Descripción (una vez que se selecciona un evento) a veces son difíciles de leer (un argumento al que se debe dar formato como Hex se mostrará en formato decimal, por ejemplo). Sin embargo, puede seleccionar la pestaña **detalles** en la descripción del evento, que muestra la entrada del registro XML sin formato, que suele tener argumentos más fáciles de entender.

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a>Usar Visor de eventos para iniciar el seguimiento de cambios de catálogo Winsock

Al abrir Visor de eventos, el panel izquierdo contiene la lista de eventos. Abra **registros de aplicaciones y servicios** , vaya a **Microsoft \\ Windows \\ Winsock Catalog Change** como origen y seleccione **operativo**.

En el panel acción, seleccione **propiedades de registro** y active la casilla **Habilitar registro** . Una vez habilitado el registro, también puede cambiar el tamaño del archivo de registro si es necesario.

Ahora está habilitado el seguimiento de cambios del catálogo Winsock y lo único que debe hacer es la acción actualizar para actualizar la lista de eventos que se han registrado. Para detener el registro, simplemente desactive el mismo botón de radio.

Es posible que tenga que aumentar el tamaño del registro en función del número de eventos que desee ver. Un inconveniente de usar la Visor de eventos para el seguimiento de Winsock es que no carga todos los recursos de cadena, por lo que los mensajes que se muestran en el campo de Descripción (una vez que se selecciona un evento) a veces son difíciles de leer (un argumento al que se debe dar formato como Hex se mostrará en formato decimal, por ejemplo). Sin embargo, puede seleccionar la pestaña **detalles** en la descripción del evento, que muestra la entrada del registro XML sin formato, que suele tener argumentos más fáciles de entender.

## <a name="interpreting-winsock-tracing-logs"></a>Interpretar registros de seguimiento de Winsock

Todos los eventos de seguimiento de Winsock de un registro contienen dos tipos de información:

-   System
-   EventData

La información del sistema contiene el nivel de registro, la hora a la que se creó la entrada de registro, el identificador de evento que representa el tipo de evento, el identificador del proceso de ejecución, el identificador del subproceso de ejecución y otra información del sistema. Un nivel de registro 4 en seguimiento de Winsock representa el registro de eventos de información. Un nivel de registro 5 en el seguimiento de Winsock representa el registro detallado de eventos.

El identificador del proceso de ejecución y el ID. del subproceso en la información del sistema indica el proceso y el subproceso que se estaba ejecutando cuando se produjo el evento. En muchos casos, esto representa un kernel o subproceso de trabajo y proceso, no un subproceso en modo de usuario ni el proceso de la aplicación. Por lo tanto, este campo no suele ser muy útil.

Cada tipo de evento de seguimiento de Winsock tiene un identificador de evento único en la sección del sistema de los datos registrados. Estos identificadores de eventos se pueden usar fácilmente para filtrar un archivo de registro para eventos específicos de seguimiento de Winsock.

El EventData contiene información específica del tipo de evento.

El parámetro Process en la información de EventData es la dirección de la estructura EPROCESS del kernel para el proceso, no el PID real. Para hacer coincidir un evento con el PID de modo de usuario, tome el valor del proceso de la información de EventData desde cualquier entrada del registro y mire antes en el registro un evento de creación de sockets con el valor del proceso. Una vez que se encuentra una coincidencia, el último parámetro de los datos del evento de creación del socket es el identificador de proceso del modo de usuario que creó el socket.

Se devuelve un parámetro Address en la información de EventData en algunos eventos de seguimiento de Winsock. Un parámetro Address representa una dirección IP, pero se muestra en el archivo de texto creado por la herramienta **tracerpt.exe** o en visor de eventos como bytes sin formato o como un número. Las direcciones IPv6 se muestran en formato hexadecimal, por lo que son más fáciles de entender. Las direcciones IPv4 se muestran como un número decimal grande. Los desarrolladores deberán convertir manualmente los bytes sin formato de una dirección IPv4 en la notación de dirección decimal con punto de IPv4 más familiar para poder interpretar mejor el valor.

Se devuelve un parámetro de error en el EventData en algunos eventos de seguimiento de Winsock. Un parámetro de error tiene el formato de un código de error NTSTATUS o HRESULT. Este parámetro de error se muestra en el archivo de texto creado por la herramienta **tracerpt.exe** o en visor de eventos como un número decimal. Los desarrolladores deberán convertir manualmente el número decimal en un número hexadecimal para poder interpretar mejor el código de error en algunos casos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Detalles de seguimiento de cambios de catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Detalles de seguimiento de eventos de red Winsock](winsock-tracing-event-details.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> </dl>

 

 
