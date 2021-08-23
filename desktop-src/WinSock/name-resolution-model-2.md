---
description: Un espacio de nombres hace referencia a alguna funcionalidad para asociar (como mínimo) el protocolo y los atributos de direccionamiento de un servicio de red con uno o varios nombres descriptivos.
ms.assetid: 4139a8c2-d940-41e0-a3e8-fce3b70a1ff3
title: Modelo de resolución de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23395cc6db5a93ec572f59e0d5ac6aaa7890c5c42a7966b86601eb190a54796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822791"
---
# <a name="name-resolution-model"></a>Modelo de resolución de nombres

Un *espacio* de nombres hace referencia a alguna funcionalidad para asociar (como mínimo) el protocolo y los atributos de direccionamiento de un servicio de red con uno o varios nombres descriptivos. Muchos espacios de nombres están actualmente en [](../dns/dns-start-page.md) uso general, incluidos el Sistema de nombres de dominio (DNS) de Internet, [Active Directory Domain Services](../ad/active-directory-domain-services.md), el enlazador, Servicios de directorio NetWare (NDS) de Bind y X.500. Estos espacios de nombres varían ampliamente en la forma en que se organizan e implementan. Algunas de sus propiedades son especialmente importantes para comprender desde la perspectiva de la resolución de nombres winsock.

## <a name="types-of-namespaces"></a>Tipos de espacios de nombres

Hay tres tipos diferentes de espacios de nombres en los que se puede registrar un servicio:

-   Dinámica
-   estática
-   Persistente

Los espacios de nombres dinámicos permiten que los servicios se registren con el espacio de nombres sobre la marcha y que los clientes detecte los servicios disponibles en tiempo de ejecución. Los espacios de nombres dinámicos suelen basarse en difusión para indicar la disponibilidad continua de un servicio de red. Entre los ejemplos anteriores de espacios de nombres dinámicos se incluyen el espacio de nombres service advertising protocol (SAP) usado en un entorno de NetWare y el espacio de nombres del Protocolo de enlace de nombres (NBP) que usa AppleTalk. El espacio de nombres del Protocolo de resolución de nombres del mismo nivel (PNRP) Windows es un ejemplo más reciente de un espacio de nombres dinámico.

Los espacios de nombres estáticos requieren que todos los servicios se registren con antelación, es decir, cuando se crea el espacio de nombres. Un ejemplo de un espacio de nombres estático son los *hosts,* *el protocolo* y los archivos *de* servicios usados por la mayoría de las implementaciones de TCP/IP. En Windows, estos archivos normalmente se encuentran en la carpeta *C: \\ windows \\ system32 \\ drivers \\ etc.*

Los espacios de nombres persistentes permiten que los servicios se registren con el espacio de nombres sobre la marcha. Sin embargo, a diferencia de los espacios de nombres dinámicos, los espacios de nombres persistentes conservan la información de registro en el almacenamiento no volátil donde permanece hasta el momento en que el servicio solicita que se quite. Los espacios de nombres persistentes se tipifica por servicios de directorio como X.500 y NDS (NetWare Directory Service). Estos entornos permiten agregar, eliminar y modificar las propiedades del servicio. Además, el objeto de servicio que representa el servicio dentro del servicio de directorio podría tener una variedad de atributos asociados al servicio. El atributo más importante para las aplicaciones cliente es la información de direccionamiento del servicio. DNS es otro ejemplo de un espacio de nombres persistente. Aunque hay una manera mediante programación de resolver nombres DNS mediante sockets de Windows, el proveedor de espacios de nombres DNS de Windows no admite el registro de nuevos nombres DNS mediante Winsock. Debe usar las funciones DNS directamente para registrar nombres DNS. Para obtener más información, consulte la referencia [de DNS.](../dns/dns-reference.md)

## <a name="namespace-organization"></a>Organización del espacio de nombres

Muchos espacios de nombres se organizan jerárquicamente. Algunos, como X.500 y NDS, permiten anidamiento ilimitado. Otros permiten que los servicios se combinen en un único nivel de jerarquía o grupo. Esto se conoce normalmente como un grupo de *trabajo.* Al construir una consulta, a menudo es necesario establecer un punto de contexto dentro de una jerarquía de espacios de nombres desde la que se iniciará la búsqueda.

## <a name="namespace-provider-architecture"></a>Arquitectura del proveedor de espacios de nombres

Naturalmente, las interfaces de programación que se usan para consultar los distintos tipos de espacios de nombres y para registrar información dentro de un espacio de nombres (si se admite) difieren ampliamente. Un  proveedor de espacios de nombres es un fragmento de software localmente residentes que sabe cómo asignar entre el SPI del espacio de nombres Winsock y algún espacio de nombres existente (que se podría implementar localmente o al que se puede acceder a través de la red). La arquitectura del proveedor de espacios de nombres se ilustra de la siguiente manera:

![arquitectura del proveedor de espacios de nombres](images/ovrvw3-1.png)

Tenga en cuenta que es posible que un espacio de nombres determinado, por ejemplo, DNS, tenga más de un proveedor de espacios de nombres instalado en un equipo determinado.

Como se mencionó anteriormente, el término genérico *servicio* hace referencia a la mitad del servidor de una aplicación cliente/servidor. En Winsock, un servicio está asociado *a* una clase de  servicio y cada instancia de un servicio determinado tiene un nombre de servicio que debe ser único dentro de la clase de servicio. Algunos ejemplos de clases de servicio son ftp server, SQL Server, XYZ Corp. Employee Info Server, etc. Como se intenta ilustrar en el ejemplo, algunas clases de servicio son conocidas, mientras que otras son únicas y específicas de una aplicación vertical determinada. En cualquier caso, cada clase de servicio se representa mediante un nombre de clase y un identificador de clase. El nombre de clase no tiene que ser necesariamente único, pero el identificador de clase debe ser . Los identificadores únicos globales (GUID) se usan para representar identificadores de clase de servicio. En el caso de los servicios conocidos, los nombres de clase y los identificadores de clase (GUID) se han preasignado y las macros están disponibles para convertir entre, por ejemplo, números de puerto TCP (en orden de bytes de host) y los GUID de identificador de clase correspondientes. Para otros servicios, el desarrollador elige el nombre de clase y usa la utilidad Uuidgen.exe para generar un GUID para el identificador de clase.

La noción de una clase de servicio existe para permitir que se establezca un conjunto de atributos que todas las instancias de un servicio determinado mantienen en común. Este conjunto de atributos se proporciona en el momento en que la clase de servicio se define como Winsock y se conoce como información de esquema de clase de servicio. Cuando se instala un servicio y está disponible en un equipo host, se considera que se crea una instancia de ese servicio y su nombre de servicio se usa para distinguir una instancia determinada del servicio de otras instancias que el espacio de nombres puede conocer.

Tenga en cuenta que la instalación de una clase de servicio solo debe producirse en equipos donde se ejecuta el servicio, no en todos los clientes que pueden utilizar el servicio. Siempre que sea posible, el32.dll Ws2 proporciona información de esquema de clase de servicio a un proveedor de espacios de nombres en el momento en que se va a registrar una instancia de un servicio o se inicia una \_ consulta de servicio. Por supuesto,32.dll Ws2 no almacena esta información, sino que intenta recuperarla de un proveedor de espacios de nombres que ha indicado su capacidad para proporcionar \_ estos datos. Puesto que no hay ninguna garantía de que el32.dll Ws2 pueda proporcionar el esquema de clase de servicio, los proveedores de espacios de nombres que necesitan esta información deben tener un mecanismo de reserva para obtenerla a través de medios específicos del espacio de \_ nombres.

Como se indicó anteriormente, Internet ha adoptado lo que se puede denominar modelo de servicio centrado en el host. Por lo general, las aplicaciones que necesitan buscar la dirección de transporte de un servicio deben resolver primero la dirección de un host específico conocido para hospedar el servicio. A esta dirección agregan el número de puerto conocido y, por tanto, crean una dirección de transporte completa. Para facilitar la resolución de nombres de host, se ha preasignado un identificador de clase de servicio especial (NOMBRE DE HOST **DE SVCID). \_** Una consulta que especifica **SVCID \_ HOSTNAME** como clase de servicio y especifica un nombre de host para el nombre de instancia de servicio devolverá información de dirección de host si la consulta se realiza correctamente.

En Windows Sockets 2, las aplicaciones independientes del protocolo deben evitar la necesidad de comprender los detalles internos de una dirección de transporte. Por lo tanto, la necesidad de obtener primero una dirección de host y, a continuación, agregar en el puerto es problemática. Para evitar esto, las consultas también pueden incluir el nombre conocido de un servicio determinado y el protocolo sobre el que funciona el servicio, como FTP a través de TCP. En este caso, una consulta correcta devuelve una dirección de transporte completa para el servicio especificado en el host indicado y la aplicación no es necesaria para inspeccionar los internos de una estructura [**sockaddr.**](sockaddr-2.md)

El sistema de nombres de dominio de Internet no tiene un medio bien definido para almacenar información de esquema de clase de servicio. Como resultado, los proveedores de espacios de nombres DNS para Winsock solo pueden dar cabida a servicios TCP/IP conocidos para los que se ha preasignado un GUID de clase de servicio.

En la práctica, esto no es una limitación grave, ya que los GUID de clase de servicio se han preasignado para todo el conjunto de puertos TCP y UDP, y las macros están disponibles para recuperar el GUID asociado a cualquier puerto TCP o UDP con el puerto expresado en orden de bytes de host. Por lo tanto, todos los servicios conocidos, como HTTP, FTP, Telnet, Whois, etc., son bien compatibles.

Siguiendo con nuestro ejemplo de clase de servicio, los nombres de instancia del servicio FTP pueden ser "alder.intel.com" o "ftp.microsoft.com", mientras que una instancia de XYZ Corp. Employee Info Server podría denominarse "XYZ Corp. Employee Info Server Version 3.5".

En los dos primeros casos, la combinación del GUID de la clase de servicio para FTP y el nombre del equipo (proporcionado como nombre de instancia de servicio) identifican de forma única el servicio deseado. En el tercer caso, el nombre de host donde reside el servicio se puede detectar en el momento de la consulta del servicio, por lo que el nombre de instancia de servicio no necesita incluir un nombre de host.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de DNS](../dns/dns-reference.md)
</dt> <dt>

[Estructuras de datos de resolución de nombres](name-resolution-data-structures-2.md)
</dt> <dt>

[Resolución de nombres independiente del protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[Resumen de las funciones de resolución de nombres](summary-of-name-resolution-functions-2.md)
</dt> </dl>

 

 
