---
description: Las interfaces mediante programación que se usan para consultar los distintos tipos de espacios de nombres y para registrar información dentro de un espacio de nombres, si se admite, difieren ampliamente.
ms.assetid: 6a037e8d-49f3-4286-929a-8bb64ea0960f
title: Arquitectura del proveedor de espacios de nombres en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f2f29b0bb5d432639fddff94430e76970e14f8bbbfe91f8b8478f2ee804c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758035"
---
# <a name="namespace-provider-architecture-in-the-spi"></a>Arquitectura del proveedor de espacios de nombres en el SPI

Las interfaces mediante programación que se usan para consultar los distintos tipos de espacios de nombres y para registrar información dentro de un espacio de nombres, si se admite, difieren ampliamente. Un proveedor de espacios de nombres es una aplicación localmente residentes que se puede asignar entre el SPI del espacio de nombres Windows Sockets y algún espacio de nombres existente al que se podría implementar localmente o tener acceso a través de la red. Esto se ilustra de la siguiente manera:

![diagrama del proveedor de espacios de nombres](images/ovrvw3-1.png)

> [!Note]  
> Es posible que un espacio de nombres determinado, por ejemplo DNS, tenga más de un proveedor de espacios de nombres instalado en un equipo determinado.

 

Como se mencionó anteriormente, el término genérico, service, hace referencia a la mitad del servidor de una aplicación cliente/servidor. En Windows sockets, un servicio está asociado a una clase de servicio y cada instancia de un servicio determinado tiene un nombre de servicio que debe ser único dentro de la clase de servicio. Algunos ejemplos de clases de servicio son servidor FTP, SQL Server, xyz corp. servidor de información de empleado, y así sucesivamente.

Como se intenta ilustrar en el ejemplo, algunas clases de servicio son conocidas, mientras que otras son únicas y específicas de una aplicación vertical determinada. En cualquier caso, cada clase de servicio se representa mediante un nombre de clase y un identificador de clase. No es necesario que el nombre de clase sea único, pero el identificador de clase debe ser . Los identificadores únicos globales (GUID) se usan para representar los identificadores de clase de servicio. Para servicios conocidos, los nombres de clase y los identificadores de clase (GUID) se han preasignado y las macros están disponibles para convertir entre, por ejemplo, números de puerto TCP y los GUID de identificador de clase correspondientes. Para otros servicios, el desarrollador elige el nombre de clase y usa la utilidad Uuidgen.exe para generar un GUID para el identificador de clase.

El concepto de una clase de servicio existe para permitir que se establezca un conjunto de atributos que todas las instancias de un servicio determinado mantienen en común. Este conjunto de atributos se proporciona a Windows Sockets en el momento en que se define la clase de servicio y se conoce como información de esquema de clase de servicio. A su vez, el32.dll Ws2 \_ retransmite esta información a todos los proveedores de espacios de nombres activos. Cuando se instala una instancia de un servicio y está disponible en un equipo host, su nombre de servicio se usa para distinguir esta instancia en particular de otras que el espacio de nombres pueda conocer.

Tenga en cuenta que la instalación de una clase de servicio solo debe producirse en equipos donde se ejecuta el servicio, no en todos los clientes que pueden utilizar el servicio. Cuando sea posible, el32.dll Ws2 proporcionará información de esquema de clase de servicio a un proveedor de espacios de nombres en el momento en que se va a registrar una instancia de un servicio o se inicia una \_ consulta de servicio. Por supuesto,32.dll Ws2 no almacena esta información, sino que intenta recuperarla de un proveedor de espacios de nombres que ha indicado su capacidad para proporcionar \_ estos datos. Dado que no hay ninguna garantía de que el32.dll Ws2 pueda proporcionar el esquema de clase de servicio, los proveedores de espacios de nombres que requieren esta información deben tener un mecanismo de reserva para obtenerla a través de medios específicos del espacio de \_ nombres.

El sistema de nombres de dominio de Internet no tiene un medio bien definido para almacenar información de esquema de clase de servicio. Como resultado, los proveedores de espacios de nombres DNS solo podrán dar cabida a servicios TCP/IP conocidos para los que se ha preasignado un GUID de clase de servicio. En la práctica, esto no es una limitación grave, ya que los GUID de clase de servicio se han preasignado para todo el conjunto de puertos TCP y UDP, y las macros están disponibles para recuperar el GUID asociado a cualquier puerto TCP o UDP. Por lo tanto, todos los servicios conocidos, como ftp, telnet, whois, etc., son bien compatibles. Al consultar estos servicios, por convención, el nombre de host del equipo de destino es el nombre de instancia de servicio.

Siguiendo con nuestro ejemplo de clase de servicio, los nombres de instancia del servicio ftp pueden ser "alder.intel.com" o "rhino.microsoft.com", mientras que una instancia de XYZ Corp. Employee Info Server podría denominarse "XYZ Corp. Employee Info Server Version 3.5". En los dos primeros casos, la combinación del GUID de clase de servicio para ftp y el nombre del equipo (proporcionado como nombre de instancia de servicio) identifican de forma única el servicio deseado. En el tercer caso, el nombre de host donde reside el servicio se puede detectar en el momento de la consulta del servicio, por lo que el nombre de instancia de servicio no necesita incluir un nombre de host.

 

 



