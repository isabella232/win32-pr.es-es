---
description: Control del seguimiento de Winsock
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Control del seguimiento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc80251410b95e2d02106474ae97ab3c6ea57759dcfdbc76987d6621794c822e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996824"
---
# <a name="control-of-winsock-tracing"></a>Control del seguimiento de Winsock

El seguimiento de Winsock se puede controlar mediante cualquiera de los métodos siguientes:

-   Herramientas de la línea de comandos

    Se incluyen dos herramientas de línea de comandos con Windows Vista y Windows Server 2008 que se usan para controlar el seguimiento y convertir el archivo de registro de seguimiento binario en texto legible.

    La **logman.exe** se usa para iniciar o detener el seguimiento de Winsock.

    La **tracerpt.exe** se usa para convertir el archivo de registro de seguimiento binario en un archivo de texto legible.

-   Visor de eventos

    Los Visor de eventos en Windows Vista y versiones posteriores también se pueden usar para habilitar el seguimiento de Winsock. El Visor de eventos es accesible en Herramientas administrativas desde el menú Inicio.

## <a name="using-logman-and-tracert"></a>Uso de logman y tracert

El seguimiento de eventos de red de Winsock está deshabilitado de forma predeterminada Windows Vista y versiones posteriores.

El siguiente comando inicia el seguimiento de eventos de red de Winsock en un equipo, establece el nombre de la sesión de seguimiento de eventos en mywinsocksession y envía la salida a un archivo de registro binario denominado winsocklogfile.etl:

**logman start -ets mywinsocksession -o winsocklogfile.etl -p Microsoft-Windows-Winsock-AFD**

Los archivos de registro se crean en el directorio actual con nombres de archivo con el formato winsocklogfile \_ 000001.etl

El siguiente comando detiene el seguimiento de Winsock anterior en un equipo para la sesión denominada mywinsocksession:

**logman stop -ets mywinsocksession**

Se escribirá un archivo de registro binario en la ubicación especificada por el parámetro –o. Para convertir el archivo binario en un archivo de texto legible, **tracerpt.exe** se usa:

**tracerpt.exe <nombre del archivo .etl> –o winsocktracelog.txt**

Si se prefiere un archivo de salida que contiene xml en lugar de texto sin formato, se usa el siguiente comando:

**tracerpt.exe <nombre del archivo .etl> –o winsocktracelog.xml –of xml**

El seguimiento de cambios del catálogo de Winsock está habilitado de forma predeterminada Windows Vista y versiones posteriores.

> [!Note]  
> Los proveedores de servicios por capas están en desuso. A partir de Windows 8 y Windows Server 2012, use [Windows filtering platform](../fwp/windows-filtering-platform-start-page.md).

 

El siguiente comando inicia el seguimiento de cambios del catálogo de Winsock para proveedores de servicios en capas (LSP) en un equipo, establece el nombre de la sesión de seguimiento de eventos en mywinsockcatalogsession y envía la salida a un archivo de registro binario denominado winsockcataloglogfile.etl:

**logman start -ets mywinsockcatalogsession -o winsockcataloglogfile.etl -p Microsoft-Windows-Winsock-WS2HELP**

Los archivos de registro se crean en el directorio actual con nombres de archivo con el formato winsockcataloglogfile \_ 000001.etl

El comando siguiente detiene el seguimiento de Winsock anterior en un equipo para la sesión denominada mysession:

**logman stop -ets mywinsockcatalogsession**

Se escribirá un archivo de registro binario en la ubicación especificada por el parámetro –o. Para convertir el archivo binario en un archivo de texto legible, **tracerpt.exe** se usa:

**tracerpt.exe <nombre del archivo .etl> –o winsockcatalogtracelog.txt**

Si se prefiere un archivo de salida que contiene xml en lugar de texto sin formato, se usa el siguiente comando:

**tracerpt.exe <nombre del archivo .etl> –o winsockcatalogtracelog.xml –of xml**

## <a name="using-event-viewer-to-start-winsock-network-event-tracing"></a>Uso Visor de eventos iniciar el seguimiento de eventos de Winsock Network

Al abrir Visor de eventos, el panel izquierdo contiene la lista de eventos. Abra **Registros de aplicaciones y servicios,** vaya a Microsoft Windows Evento de red **\\ \\ Winsock** como origen y seleccione **Operativo.**

En el panel Acción, seleccione **Propiedades del registro y** active la **casilla** Habilitar registro . Una vez habilitado el registro, también puede cambiar el tamaño del archivo de registro si es necesario.

El seguimiento de eventos de red de Winsock ahora está habilitado y todo lo que necesita hacer es alcanzar la acción Actualizar para actualizar la lista de eventos que se han registrado. Para detener el registro, simplemente desactive el mismo botón de radio.

Es posible que tenga que aumentar el tamaño del registro en función del número de eventos que desee ver. Un inconveniente del uso del Visor de eventos para el seguimiento de Winsock es que no carga todos los recursos de cadena, por lo que los mensajes mostrados en el campo Descripción (una vez que seleccione un evento) a veces es difícil de leer (un argumento con formato hexadecimal se mostrará en decimal, por ejemplo). Sin embargo, puede seleccionar la **pestaña Detalles** en la descripción del evento, que muestra la entrada de registro XML sin formato que normalmente tiene argumentos más fáciles de entender.

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a>Uso de Visor de eventos para iniciar el seguimiento de cambios del catálogo de Winsock

Al abrir Visor de eventos, el panel izquierdo contiene la lista de eventos. Abra **Registros de aplicaciones y servicios,** vaya a Microsoft Windows Cambio de catálogo de **\\ \\ Winsock** como origen y seleccione **Operativo.**

En el panel Acción, seleccione **Propiedades del registro y** active la **casilla** Habilitar registro . Una vez habilitado el registro, también puede cambiar el tamaño del archivo de registro si es necesario.

El seguimiento de cambios del catálogo de Winsock ahora está habilitado y todo lo que necesita hacer es hacer clic en la acción Actualizar para actualizar la lista de eventos que se han registrado. Para detener el registro, simplemente desactive el mismo botón de radio.

Es posible que tenga que aumentar el tamaño del registro en función del número de eventos que desee ver. Un inconveniente del uso del Visor de eventos para el seguimiento de Winsock es que no carga todos los recursos de cadena, por lo que los mensajes mostrados en el campo Descripción (una vez que seleccione un evento) a veces es difícil de leer (un argumento con formato hexadecimal se mostrará en decimal, por ejemplo). Sin embargo, puede seleccionar la **pestaña Detalles** en la descripción del evento, que muestra la entrada de registro XML sin formato que normalmente tiene argumentos más fáciles de entender.

## <a name="interpreting-winsock-tracing-logs"></a>Interpretación de los registros de seguimiento de Winsock

Todos los eventos de seguimiento de Winsock de un registro contienen dos tipos de información:

-   Sistema
-   EventData

La información del sistema contiene el nivel de registro, la hora en que se creó la entrada de registro, el identificador de evento que representa el tipo de evento, el identificador de proceso de ejecución, el identificador del subproceso de ejecución y otra información del sistema. Un nivel de registro de 4 en el seguimiento de Winsock representa el registro de eventos de información. Un nivel de registro de 5 en el seguimiento de Winsock representa el registro detallado de eventos.

El identificador del proceso de ejecución y el identificador de subproceso de la información del sistema indican el proceso y el subproceso que se estaba ejecutando cuando se produjo el evento. En muchos casos, esto representará un kernel o subproceso de trabajo y un proceso, no un subproceso en modo de usuario ni el proceso de la aplicación. Por lo tanto, este campo normalmente no es muy útil.

Cada tipo de evento de seguimiento de Winsock tiene un identificador de evento único en la sección del sistema de los datos registrados. Estos iDs de evento se pueden usar fácilmente para filtrar un archivo de registro para eventos de seguimiento de Winsock específicos.

Eventdata contiene información específica del tipo de evento.

El parámetro Process de la información de eventdata es la dirección de la estructura EPROCESS del kernel para el proceso, no el PID real. Para hacer coincidir un evento con el PID en modo de usuario, tome el valor Process de la información de eventdata de cualquier entrada de registro y busque anteriormente en el registro un evento de creación de sockets con el valor Process. Una vez que se encuentra una coincidencia, el último parámetro de los datos del evento de creación del socket es el identificador de proceso en modo de usuario que creó el socket.

Se devuelve un parámetro Address en la información de eventdata en algunos eventos de seguimiento de Winsock. Un parámetro Address representa una dirección IP, pero se muestra en el archivo de texto creado por la herramienta **tracerpt.exe** o en Visor de eventos como bytes sin formato o un número. Las direcciones IPv6 se muestran en formato hexadecimal, por lo que se comprenden más fácilmente. Las direcciones IPv4 se muestran como un número decimal grande. Los desarrolladores tendrán que convertir manualmente los bytes sin procesar de una dirección IPv4 en la notación de dirección decimal con puntos IPv4 más conocida para poder interpretar mejor el valor.

Se devuelve un parámetro Error en eventdata en algunos eventos de seguimiento de Winsock. Un parámetro Error tiene la forma de un código de error NTSTATUS o HRESULT. Este parámetro de error se muestra en el archivo de texto creado por la herramienta **tracerpt.exe** o en Visor de eventos como un número decimal. Los desarrolladores tendrán que convertir manualmente el número decimal en un número hexadecimal para interpretar mejor el código de error en algunos casos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Detalles del seguimiento de cambios del catálogo de Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Detalles del seguimiento de eventos de Winsock Network](winsock-tracing-event-details.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> </dl>

 

 
