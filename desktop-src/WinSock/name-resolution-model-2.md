---
description: Un espacio de nombres hace referencia a alguna funcionalidad para asociar (como mínimo) el protocolo y el direccionamiento de los atributos de un servicio de red con uno o más nombres descriptivos.
ms.assetid: 4139a8c2-d940-41e0-a3e8-fce3b70a1ff3
title: Modelo de resolución de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb209254dcee2419e1ed92c017fc7d37dc9c0a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541558"
---
# <a name="name-resolution-model"></a>Modelo de resolución de nombres

Un *espacio de nombres* hace referencia a alguna funcionalidad para asociar (como mínimo) el protocolo y el direccionamiento de los atributos de un servicio de red con uno o más nombres descriptivos. Muchos espacios de nombres están actualmente en uso general, incluidos el [sistema de nombres de dominio](../dns/dns-start-page.md) (DNS) de Internet, [Active Directory Domain Services](../ad/active-directory-domain-services.md), el enlace, el servicios de directorio NetWare (NDS) de Novell y X. 500. Estos espacios de nombres varían considerablemente en el modo en que se organizan e implementan. Algunas de sus propiedades son especialmente importantes para comprender desde la perspectiva de la resolución de nombres de Winsock.

## <a name="types-of-namespaces"></a>Tipos de espacios de nombres

Hay tres tipos diferentes de espacios de nombres en los que se puede registrar un servicio:

-   Dinámica
-   estática
-   Persistente

Los espacios de nombres dinámicos permiten que los servicios se registren en el espacio de nombres sobre la marcha y para que los clientes detecten los servicios disponibles en tiempo de ejecución. Los espacios de nombres dinámicos suelen basarse en difusiones para indicar la disponibilidad continua de un servicio de red. Los ejemplos más antiguos de espacios de nombres dinámicos incluyen el espacio de nombres del Protocolo de anuncio de servicio (SAP) usado en un entorno de NetWare y el espacio de nombres del Protocolo de enlace de nombres (NBP) que usa AppleTalk. El espacio de nombres del Protocolo de resolución de nombres de mismo nivel (PNRP) utilizado en Windows es un ejemplo más reciente de un espacio de nombres dinámico.

Los espacios de nombres estáticos requieren que todos los servicios se registren con anterioridad, es decir, cuando se crea el espacio de nombres. Un ejemplo de un espacio de nombres estático son los *hosts*, *protocolos* y *servicios* que utilizan la mayoría de las implementaciones de TCP/IP. En Windows, estos archivos se encuentran normalmente en la carpeta *C: \\ Windows \\ system32 drivers, \\ \\ etc* .

Los espacios de nombres persistentes permiten que los servicios se registren con el espacio de nombres sobre la marcha. Sin embargo, a diferencia de los espacios de nombres dinámicos, los espacios de nombres persistentes conservan la información de registro en un almacenamiento no volátil donde permanece hasta el momento en que el servicio solicita que se quite. Los espacios de nombres persistentes son typified por servicios de directorio como X. 500 y NDS (servicio de directorio NetWare). Estos entornos permiten agregar, eliminar y modificar las propiedades del servicio. Además, el objeto de servicio que representa el servicio dentro del servicio de directorio podría tener una variedad de atributos asociados al servicio. El atributo más importante para las aplicaciones cliente es la información de direccionamiento del servicio. DNS es otro ejemplo de un espacio de nombres persistente. Aunque existe una manera programática de resolver nombres DNS con Windows Sockets, el proveedor de espacios de nombres DNS en Windows no admite el registro de nuevos nombres DNS con Winsock. Debe usar las funciones de DNS directamente para registrar nombres DNS. Para obtener más información, consulte la [referencia de DNS](../dns/dns-reference.md).

## <a name="namespace-organization"></a>Organización del espacio de nombres

Muchos espacios de nombres se organizan jerárquicamente. Algunos, como X. 500 y NDS, permiten un anidamiento ilimitado. Otros permiten que los servicios se combinen en un solo nivel de jerarquía o grupo. Esto se conoce normalmente como grupo de *trabajo*. Al construir una consulta, a menudo es necesario establecer un punto de contexto dentro de una jerarquía de espacios de nombres desde la que comenzará la búsqueda.

## <a name="namespace-provider-architecture"></a>Arquitectura de proveedor de espacio de nombres

Naturalmente, las interfaces de programación que se usan para consultar los distintos tipos de espacios de nombres y registrar información dentro de un espacio de nombres (si se admite) difieren ampliamente. Un *proveedor de espacios de nombres* es un elemento de software residente localmente que sabe cómo asignar entre el espacio de nombres de Winsock y un espacio de nombres existente (que se puede implementar localmente o al que se puede tener acceso a través de la red). La arquitectura del proveedor de espacios de nombres se muestra a continuación:

![arquitectura de proveedor de espacio de nombres](images/ovrvw3-1.png)

Tenga en cuenta que es posible que un espacio de nombres determinado, por ejemplo, DNS, tenga más de un proveedor de espacios de nombres instalado en un equipo determinado.

Como se mencionó anteriormente, el término *servicio* genérico hace referencia a la mitad del servidor de una aplicación cliente/servidor. En Winsock, un servicio está asociado a una *clase de servicio* y cada instancia de un servicio determinado tiene un *nombre de servicio* que debe ser único dentro de la clase de servicio. Entre los ejemplos de clases de servicio se incluyen el servidor FTP, SQL Server, el servidor XYZ Corp. info. de empleado, etc. Como en el ejemplo se intenta ilustrar, algunas clases de servicio son muy conocidas, mientras que otras son únicas y específicas de una aplicación vertical concreta. En cualquier caso, cada clase de servicio se representa mediante un nombre de clase y un identificador de clase. No es necesario que el nombre de clase sea único, pero el identificador de clase debe ser. Los identificadores únicos globales (GUID) se usan para representar los identificadores de clase de servicio. En el caso de los servicios conocidos, los nombres de clase y los identificadores de clase (GUID) se han asignado previamente y las macros están disponibles para la conversión entre, por ejemplo, los números de puerto TCP (en el orden de bytes de host) y los GUID de identificador de clase correspondientes. Para otros servicios, el desarrollador elige el nombre de clase y usa la utilidad Uuidgen.exe para generar un GUID para el identificador de clase.

La noción de una clase de servicio existe para permitir establecer un conjunto de atributos que se mantienen en común por todas las instancias de un servicio determinado. Este conjunto de atributos se proporciona en el momento en que la clase de servicio se define en Winsock y se conoce como la información de esquema de la clase de servicio. Cuando un servicio se instala y se pone a disposición en un equipo host, se considera que se *crea una instancia* del servicio y su nombre de servicio se usa para distinguir una instancia determinada del servicio de otras instancias que se pueden conocer en el espacio de nombres.

Tenga en cuenta que la instalación de una clase de servicio solo tiene que producirse en los equipos en los que se ejecuta el servicio, no en todos los clientes que pueden emplear el servicio. Siempre que sea posible, el \_32.dll Ws2 proporciona información de esquema de clase de servicio a un proveedor de espacios de nombres en el momento en que se va a registrar una creación de instancias de un servicio o se inicie una consulta de servicio. Por supuesto, el \_32.dll Ws2 no almacena esta información, sino que intenta recuperarla de un proveedor de espacios de nombres que ha indicado su capacidad para proporcionar estos datos. Dado que no hay ninguna garantía de que el \_32.dll Ws2 puede proporcionar el esquema de clase de servicio, los proveedores de espacios de nombres que necesitan esta información deben tener un mecanismo de reserva para obtenerlo a través de medios específicos del espacio de nombres.

Como se indicó anteriormente, Internet ha adoptado lo que puede denominarse modelo de servicio centrado en el host. Las aplicaciones que necesitan buscar la dirección de transporte de un servicio generalmente deben resolver primero la dirección de un host específico conocido para hospedar el servicio. En esta dirección, agregan el número de puerto conocido y, por tanto, crean una dirección de transporte completa. Para facilitar la resolución de los nombres de host, se ha asignado previamente un identificador de clase de servicio especial (**SVCID \_ hostname**). Una consulta que especifica **SVCID \_ hostname** como clase de servicio y especifica un nombre de host para el nombre de la instancia de servicio devolverá la información de la dirección del host si la consulta se realiza correctamente.

En Windows Sockets 2, las aplicaciones que son independientes del protocolo deben evitar la necesidad de comprender los detalles internos de una dirección de transporte. Por lo tanto, la necesidad de obtener primero una dirección de host y, a continuación, agregar en el puerto es problemática. Para evitar esto, las consultas también pueden incluir el nombre conocido de un servicio determinado y el Protocolo sobre el que funciona el servicio, como FTP a través de TCP. En este caso, una consulta correcta devuelve una dirección de transporte completa para el servicio especificado en el host indicado y no es necesario que la aplicación Inspeccione los elementos internos de una estructura [**sockaddr**](sockaddr-2.md) .

El sistema de nombres de dominio de Internet no tiene un medio bien definido para almacenar información de esquema de clase de servicio. Como resultado, los proveedores de espacios de nombres DNS para Winsock solo pueden dar cabida a servicios conocidos de TCP/IP para los que se ha asignado previamente un GUID de clase de servicio.

En la práctica, no se trata de una limitación seria, ya que los GUID de clase de servicio se han asignado previamente para todo el conjunto de puertos TCP y UDP, y las macros están disponibles para recuperar el GUID asociado a cualquier puerto TCP o UDP con el puerto expresado en el orden de bytes del host. Por lo tanto, se admiten correctamente todos los servicios conocidos como HTTP, FTP, Telnet, Whois, etc.

Siguiendo con nuestro ejemplo de clase de servicio, los nombres de instancia del servicio FTP pueden ser "alder.intel.com" o "ftp.microsoft.com", mientras que una instancia del servidor XYZ Corp. info. employee puede denominarse "XYZ Corp. Employee info Server versión 3,5".

En los dos primeros casos, la combinación del GUID de clase de servicio para FTP y el nombre de equipo (que se proporciona como nombre de instancia de servicio) identifica de forma única el servicio deseado. En el tercer caso, el nombre de host en el que reside el servicio se puede detectar en el momento de la consulta del servicio, por lo que el nombre de la instancia de servicio no necesita incluir un nombre de host.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de DNS](../dns/dns-reference.md)
</dt> <dt>

[Estructuras de datos de resolución de nombres](name-resolution-data-structures-2.md)
</dt> <dt>

[Resolución de nombres independiente del Protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[Resumen de las funciones de resolución de nombres](summary-of-name-resolution-functions-2.md)
</dt> </dl>

 

 
