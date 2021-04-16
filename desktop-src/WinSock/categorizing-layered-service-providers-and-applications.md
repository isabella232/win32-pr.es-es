---
title: Categorización de aplicaciones y proveedores de servicios en capas
description: Winsock 2 aloja protocolos en capas.
ms.assetid: 1c5efd2e-1b42-4c20-a4da-b81a5fc4243c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a966d54da0be26f75a074de18abe1b9e080c0c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705648"
---
# <a name="categorizing-layered-service-providers-and-apps"></a>Categorización de aplicaciones y proveedores de servicios en capas

> [!Note]  
> Los proveedores de servicios superpuestos están desusados. A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).

 

Winsock 2 aloja protocolos en capas. Un protocolo en capas es aquél que implementa solo funciones de comunicaciones de nivel superior, mientras que se basa en una pila de transporte subyacente para el intercambio de datos real con un punto de conexión remoto. Un ejemplo de un protocolo superpuesto o de un proveedor de servicios por capas sería un nivel de seguridad que agrega el protocolo al proceso de establecimiento de conexión para realizar la autenticación y establecer un esquema de cifrado acordado mutuamente. Por lo general, este protocolo de seguridad requeriría los servicios de un protocolo de transporte confiable subyacente, como TCP o SPX. El término protocolo base implementado por el proveedor base hace referencia a un proveedor Winsock que implementa un protocolo como TCP o SPX, que es capaz de realizar comunicaciones de datos con un punto de conexión remoto. El término protocolo superpuesto se usa para describir un protocolo que no puede ser independiente. Estos protocolos en capas se instalan como proveedores de servicios superpuestos (LSP) de Winsock.

Un ejemplo de un LSP es el proveedor de servicios de cliente de Firewall de Microsoft instalado como parte de Internet Secutity and Authentication Server (ISA) en los clientes. El proveedor de servicios de cliente de Firewall de Microsoft se instala a través de los proveedores base Winsock para TCP y UDP. Una biblioteca de vínculos dinámicos (DLL) en el software cliente de Firewall de ISA se convierte en un proveedor de servicios superpuesto de Winsock que utilizan todas las aplicaciones Winsock de forma transparente. De esta manera, el LSP del cliente de Firewall de ISA puede interceptar las llamadas de función de Winsock desde las aplicaciones cliente y, a continuación, enrutar una solicitud al proveedor de servicios base subyacente original si el destino es local o al servicio de firewall en un equipo servidor ISA si el destino es remoto. Un LSP similar se instala como parte del servicio de Firewall de Microsoft Forefront y del cliente de puerta de enlace de administración de amenazas (TMG) en los clientes.

Durante la inicialización del LSP, el LSP debe proporcionar punteros a un número de funciones de la interfaz del proveedor de servicios (SPI) de Winsock. Esta función se llamará durante el procesamiento normal mediante el nivel directamente por encima del LSP (otro LSP o Ws2 \_32.DLL).

Es posible definir categorías de LSP basadas en el subconjunto de funciones SPI que implementa un LSP y la naturaleza del procesamiento adicional que se realiza para cada una de esas funciones. Mediante la clasificación de los LSP, así como la clasificación de las aplicaciones que usan Sockets Winsock, se puede determinar de forma selectiva si un LSP debe estar implicado en un proceso determinado en tiempo de ejecución.

En Windows Vista y versiones posteriores, se proporciona un nuevo método para clasificar las aplicaciones y los proveedores de servicios con capas de Winsock de modo que solo se carguen determinados LSP. Hay varias razones para agregar estas características.

Uno de los motivos principales es que ciertos procesos críticos del sistema, como Winlogon y LSASS, crean sockets, pero estos procesos no usan estos Sockets para enviar tráfico en la red. Por lo tanto, la mayoría de los LSP no se deben cargar en estos procesos. También se han documentado varios casos en los que los LSP erróneos pueden hacer que *lsass.exe* bloqueen. Si LSASS se bloquea, el sistema fuerza el apagado. Un efecto secundario de estos procesos del sistema que cargan LSP es que estos procesos no salen nunca, por lo que cuando se instala o se quita un LSP, se requiere un reinicio.

Una razón secundaria es que hay algunos casos en los que es posible que las aplicaciones no quieran cargar determinados LSP. Por ejemplo, es posible que algunas aplicaciones no quieran cargar LSP de cifrado, lo que podría impedir que la aplicación se comunique con otros sistemas que no tienen instalado el LSP de cyptographic.

Por último, los LSP pueden utilizar categorías de LSP para determinar en qué punto de la cadena de protocolo Winsock deben instalarse por sí mismos. Durante años, varios desarrolladores de LSP han deseado una forma de saber cómo se comportará un LSP. Por ejemplo, un LSP que inspecciona el flujo de datos desearía estar por encima de un LSP que cifra los datos. Por supuesto, este método de categorización de LSP no es una prueba de engaño, ya que se basa en LSP de terceros para clasificarse adecuadamente.

La categorización de LSP y otras mejoras de seguridad en Windows Vista y versiones posteriores están diseñadas para ayudar a evitar que los usuarios instalen involuntariamente LSP malintencionados.

## <a name="lsp-categories"></a>Categorías de LSP

En Windows Vista y versiones posteriores, un LSP se puede clasificar en función de cómo interactúe con los datos y las llamadas de Windows Sockets. Una categoría de LSP es un grupo de comportamientos identificables en un subconjunto de las funciones de Winsock SPI. Por ejemplo, un filtro de contenido HTTP se clasificaría como un inspector de datos (la \_ categoría del inspector de LSP). La \_ categoría inspector de LSP inspeccionará (pero no modificará) los parámetros para las funciones de transferencia de datos. Una aplicación puede consultar la categoría de un LSP y elegir no cargar el LSP en función de la categoría de LSP y el conjunto de categorías de LSP permitidos de la aplicación.

En la tabla siguiente se enumeran las categorías en las que se puede clasificar un LSP.

| Categoría de LSP              | Descripción                                                     |
|---------------------------|-----------------------------------------------------------------|
| **\_compresión criptográfica de LSP \_** | El LSP es un proveedor de compresión de datos o criptografía.         |
| **Firewall de LSP \_**         | El LSP es un proveedor de Firewall.                                 |
| **\_caché local de LSP \_**     | El LSP es un proveedor de caché local.                              |
| **modificación de entrada de LSP \_ \_**  | El LSP modifica los datos de entrada.                                  |
| **Inspector de LSP \_**        | El LSP inspecciona o filtra los datos.                               |
| **modificación de salida de LSP \_ \_** | El LSP modifica los datos de salida.                                 |
| **\_proxy LSP**            | El LSP actúa como proxy y redirige los paquetes.                  |
| **redirector de LSP \_**       | El LSP es un redirector de red.                                |
| **\_sistema LSP**           | El LSP es aceptable para su uso en servicios y procesos del sistema. |



 

Un LSP puede pertenecer a más de una categoría. Por ejemplo, un firewall/LSP de seguridad puede pertenecer a las categorías Inspector (**\_ Inspector de LSP**) y firewall (**LSP \_**).

Si un LSP no tiene un conjunto de categorías, se considera que está en el resto de la categoría. Esta categoría de LSP no se cargará en los servicios o procesos del sistema (por ejemplo, LSASS, Winlogon y muchos procesos svchost).

## <a name="categorizing-lsps"></a>Categorización de LSP

Varias funciones nuevas están disponibles en Windows Vista y versiones posteriores para clasificar un LSP:

-   [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo)
-   [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32)
-   [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo)
-   [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32)

Para clasificar un LSP, se llama a la función [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo) o [**WSCSETPROVIDERINFO32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32) con un GUID para identificar la entrada oculta de LSP, la clase de información que se va a establecer para esta entrada del protocolo LSP y un conjunto de marcas que se usan para modificar el comportamiento de la función.

La función [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo) o [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32) se utiliza de forma similar para recuperar los datos asociados a una clase de información para un LSP.

## <a name="categorizing-applications"></a>Categorizar aplicaciones

Hay varias funciones nuevas disponibles en Windows Vista y versiones posteriores para clasificar una aplicación:

-   [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory)
-   [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory)

Para clasificar una aplicación, se llama a la función [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory) con la ruta de acceso de carga de la imagen ejecutable para identificar la aplicación, los argumentos de la línea de comandos usados al iniciar la aplicación y las categorías de LSP que se permiten para todas las instancias de esta aplicación.

La función [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory) se utiliza de forma similar para recuperar las categorías de proveedor de servicios por capas (LSP) asociadas a una aplicación.

## <a name="determining-which-lsps-get-loaded"></a>Determinar qué LSP se cargan

La última parte de la categorización del LSP es determinar qué LSP se cargarán en cada proceso. Cuando un proceso carga Winsock, se realizan las siguientes comparaciones de la categoría de la aplicación y de las categorías de LSP para todos los LSP instalados:

-   Si la aplicación no se clasifica por categorías, permita que se carguen todos los LSP en el proceso.
-   Si tanto la aplicación como el LSP tienen asignadas categorías, deben cumplirse todas las condiciones siguientes: <dl> Al menos una de las categorías de LSP está presente en las categorías especificadas de la aplicación.  
    Solo las categorías especificadas en las categorías especificadas de la aplicación se especifican en las categorías LSP. Por ejemplo, si la aplicación especifica una categoría, debe estar en la categoría del LSP.  
    Si la \_ categoría del sistema LSP está presente en la categoría de la aplicación, debe estar presente en las categorías del LSP.  
    </dl>

> [!Note]  
> Si no se clasifica un LSP, su categoría es realmente cero. Para que se produzca una coincidencia, todas las categorías especificadas del LSP deben estar presentes en las categorías de la aplicación (las categorías de la aplicación deben ser un superconjunto de las categorías del LSP) con la salvedad de que si \_ el sistema de LSP está presente en la categoría de la aplicación, también debe estar presente en la categoría del LSP.

 

Considere el ejemplo siguiente:

La aplicación *Foo.exe* se clasifica como sistema LSP \_ + firewall de LSP \_ + \_ compresión criptográfica de LSP \_ . La *Bar.exe* de la aplicación se clasifica como \_ firewall de LSP + \_ compresión criptográfica de LSP \_ . Hay cuatro LSP instalados en el sistema:

-   LSP1 ha establecido una categoría de \_ sistema LSP.
-   LSP2 no es un conjunto de categorías, por lo que su categoría es cero.
-   LSP3 ha establecido una categoría de Firewall de LSP \_ .
-   LSP4 tiene categorías establecidas de sistema de LSP + Firewall de LSP/ \_ \_ \_ compresión criptográfica de LSP \_ + Inspector de LSP \_

En este ejemplo, la aplicación de *Foo.exe* solo cargaría LSP1, mientras que la aplicación *Bar.exe* cargaría LSP3.

## <a name="determining-winsock-providers-installed"></a>Determinar los proveedores de Winsock instalados

El kit de desarrollo de software (SDK) de Microsoft Windows incluye un programa Winsock de ejemplo que se puede usar para determinar los proveedores de transporte Winsock instalados en un equipo local. De forma predeterminada, el código fuente de este ejemplo de Winsock se instala en el directorio siguiente del Windows SDK para Windows 7:

*C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ NetDs \\ Winsock \\ LSP*

Este ejemplo es una utilidad para instalar y probar proveedores de servicios superpuestos. Pero también se puede usar para recopilar mediante programación información detallada del catálogo de Winsock en un equipo local. Para enumerar todos los proveedores de Winsock actuales, incluidos los proveedores base y los proveedores de servicios de capa, compile este ejemplo de Winsock y ejecute el siguiente comando de la consola:

**instlsp-p**

La salida será una lista de proveedores de Winsock instalados en el equipo local, incluidos los proveedores de servicios superpuestos. La salida muestra el ID. de catálogo y el nombre de cadena del proveedor Winsock

Para recopilar información más detallada sobre todos los proveedores de Winsock, ejecute el siguiente comando de la consola:

**instlsp-p-v**

La salida será una lista de las estructuras [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que se admiten en el equipo local.

Para obtener una lista de los proveedores de servicios en capas instalados en el equipo local, ejecute el siguiente comando de la consola:

**instlsp-l**

Para asignar la estructura de LSP, ejecute el siguiente comando de la consola:

**instlsp-m**

> [!Note]  
> La característica TDI está en desuso y se quitará en versiones futuras de Microsoft Windows. En función de cómo use TDI, utilice el kernel de Winsock (WSK) o la plataforma de filtrado de Windows (WFP). Para obtener más información sobre WFP y WSK, consulte [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md) y kernel de [Winsock](/windows-hardware/drivers/ddi/_netvista/). Para obtener una entrada de blog sobre las redes de Windows Core sobre WSK y TDI, consulte [Introducción a Winsock kernel (WSK)](/archive/blogs/wndp/).

 

 

 
