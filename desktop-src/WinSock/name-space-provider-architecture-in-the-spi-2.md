---
description: Las interfaces de programación que se usan para consultar los distintos tipos de espacios de nombres y para registrar información dentro de un espacio de nombres, si se admiten, difieren ampliamente.
ms.assetid: 6a037e8d-49f3-4286-929a-8bb64ea0960f
title: Arquitectura de proveedor de espacio de nombres en SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1cb567933cae60f56137eba39845bf27ad8c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275393"
---
# <a name="namespace-provider-architecture-in-the-spi"></a>Arquitectura de proveedor de espacio de nombres en SPI

Las interfaces de programación que se usan para consultar los distintos tipos de espacios de nombres y para registrar información dentro de un espacio de nombres, si se admiten, difieren ampliamente. Un proveedor de espacios de nombres es una aplicación residente localmente que se puede asignar entre el espacio de nombres de Windows Sockets SPI y un espacio de nombres existente que podría implementarse localmente o tener acceso a ella a través de la red. Esto se muestra a continuación:

![diagrama del proveedor de espacios de nombres](images/ovrvw3-1.png)

> [!Note]  
> Es posible que un espacio de nombres determinado, por ejemplo, DNS, tenga más de un proveedor de espacios de nombres instalado en un equipo determinado.

 

Como se mencionó anteriormente, el término genérico servicio hace referencia a la mitad del servidor de una aplicación cliente/servidor. En Windows Sockets, un servicio está asociado a una clase de servicio y cada instancia de un servicio determinado tiene un nombre de servicio que debe ser único dentro de la clase de servicio. Entre los ejemplos de clases de servicio se incluyen FTP Server, SQL Server, XYZ Corp. Employee info Server, etc.

Como en el ejemplo se intenta ilustrar, algunas clases de servicio son muy conocidas, mientras que otras son únicas y específicas de una aplicación vertical concreta. En cualquier caso, cada clase de servicio se representa mediante un nombre de clase y un identificador de clase. No es necesario que el nombre de clase sea único, pero el identificador de clase debe ser. Los identificadores únicos globales (GUID) se usan para representar los ID. de clase de servicio. En el caso de los servicios conocidos, los nombres de clase y los identificadores de clase (GUID) se han asignado previamente, y las macros están disponibles para la conversión entre, por ejemplo, los números de puerto TCP y los GUID de identificador de clase correspondientes. Para otros servicios, el desarrollador elige el nombre de clase y usa la utilidad Uuidgen.exe para generar un GUID para el identificador de clase.

El concepto de una clase de servicio existe para permitir establecer un conjunto de atributos que se mantienen en común por todas las instancias de un servicio determinado. Este conjunto de atributos se proporciona a Windows Sockets en el momento en que se define la clase de servicio y se conoce como la información de esquema de la clase de servicio. \_A su vez, el32.dll Ws2 retransmite esta información a todos los proveedores de espacios de nombres activos. Cuando una instancia de un servicio se instala y se pone a disposición en un equipo host, su nombre de servicio se usa para distinguir esta instancia en particular de otras que puedan ser conocidas para el espacio de nombres.

Tenga en cuenta que la instalación de una clase de servicio solo tiene que producirse en los equipos en los que se ejecuta el servicio, no en todos los clientes que pueden utilizar el servicio. Cuando sea posible, el \_32.dll Ws2 proporcionará información de esquema de clase de servicio a un proveedor de espacios de nombres en el momento en que se registre una instancia de un servicio o se inicie una consulta de servicio. Por supuesto, el \_32.dll Ws2 no almacena esta información, sino que intenta recuperarla de un proveedor de espacios de nombres que ha indicado su capacidad para proporcionar estos datos. Dado que no hay ninguna garantía de que el \_32.dll Ws2 pueda proporcionar el esquema de clase de servicio, los proveedores de espacios de nombres que requieren esta información deben tener un mecanismo de reserva para obtenerlo a través de medios específicos del espacio de nombres.

El sistema de nombres de dominio de Internet no tiene un medio bien definido para almacenar información de esquema de clase de servicio. Como resultado, los proveedores de espacios de nombres DNS solo podrán alojar servicios de TCP/IP conocidos para los que se haya asignado previamente un GUID de clase de servicio. En la práctica, no se trata de una limitación seria, ya que los GUID de clase de servicio se han asignado previamente para todo el conjunto de puertos TCP y UDP, y las macros están disponibles para recuperar el GUID asociado a cualquier puerto TCP o UDP. Por lo tanto, todos los servicios que ya conoce, como FTP, Telnet, Whois, etc., son correctos. Al consultar estos servicios, por Convención, el nombre de host del equipo de destino es el nombre de la instancia de servicio.

Siguiendo con nuestro ejemplo de clase de servicio, los nombres de instancia del servicio FTP pueden ser "alder.intel.com" o "rhino.microsoft.com", mientras que una instancia del servidor XYZ Corp. info. employee puede denominarse "XYZ Corp. Employee info Server versión 3,5". En los dos primeros casos, la combinación del GUID de clase de servicio para FTP y el nombre de equipo (que se proporciona como nombre de instancia de servicio) identifica de forma única el servicio deseado. En el tercer caso, el nombre de host en el que reside el servicio se puede detectar en el momento de la consulta del servicio, por lo que el nombre de la instancia de servicio no necesita incluir un nombre de host.

 

 



