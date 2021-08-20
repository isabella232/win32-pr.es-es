---
title: Categorización de aplicaciones y proveedores de servicios en capas
description: Winsock 2 admite protocolos por capas.
ms.assetid: 1c5efd2e-1b42-4c20-a4da-b81a5fc4243c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0993b7a4003b87cf902b9daccbea4742a0bcd0760642429db79b1f1bb0a22600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322396"
---
# <a name="categorizing-layered-service-providers-and-apps"></a>Categorización de aplicaciones y proveedores de servicios en capas

> [!Note]  
> Los proveedores de servicios por capas están en desuso. A partir de Windows 8 y Windows Server 2012, use [Windows filtering platform](../fwp/windows-filtering-platform-start-page.md).

 

Winsock 2 admite protocolos por capas. Un protocolo por capas es aquel que implementa solo funciones de comunicaciones de nivel superior, al tiempo que se basa en una pila de transporte subyacente para el intercambio real de datos con un punto de conexión remoto. Un ejemplo de un protocolo por capas o un proveedor de servicios por capas sería una capa de seguridad que agrega el protocolo al proceso de establecimiento de la conexión con el fin de realizar la autenticación y establecer un esquema de cifrado acordado mutuamente. Por lo general, este tipo de protocolo de seguridad requeriría los servicios de un protocolo de transporte confiable subyacente, como TCP o SPX. El término protocolo base implementado por el proveedor base hace referencia a un proveedor winsock que implementa un protocolo como TCP o SPX que es capaz de realizar comunicaciones de datos con un punto de conexión remoto. El término protocolo por capas se usa para describir un protocolo que no puede ser independiente. Estos protocolos por capas se instalan como proveedores de servicios en capas (LSP) de Winsock.

Un ejemplo de un LSP es el proveedor de servicios de cliente de Firewall de Microsoft instalado como parte del servidor de secutidad y autenticación de Internet (ISA) en los clientes. El proveedor de servicios de cliente de Microsoft Firewall se instala a través de los proveedores base winsock para TCP y UDP. Una biblioteca de vínculos dinámicos (DLL) en el software cliente de firewall de ISA se convierte en un proveedor de servicios en capas de Winsock que todas las aplicaciones Winsock usan de forma transparente. De este modo, el LSP del cliente de firewall de ISA puede interceptar llamadas de función Winsock desde aplicaciones cliente y, a continuación, enrutar una solicitud al proveedor de servicios base subyacente original si el destino es local o al servicio firewall en un equipo de servidor ISA si el destino es remoto. Se instala un LSP similar como parte del servicio Microsoft Forefront Firewall y del cliente de Threat Management Gateway (TMG) en los clientes.

Durante la inicialización de LSP, el LSP debe proporcionar punteros a varias funciones de la interfaz del proveedor de servicios (SPI) de Winsock. La capa directamente encima del LSP llamará a estas funciones durante el procesamiento normal (ya sea otro LSP o Ws2 \_32.DLL).

Es posible definir categorías LSP basadas en el subconjunto de funciones SPI que implementa un LSP y la naturaleza del procesamiento adicional realizado para cada una de esas funciones. Mediante la clasificación de LSP, así como la clasificación de aplicaciones que usan sockets Winsock, es posible determinar selectivamente si un LSP debe estar implicado en un proceso determinado en tiempo de ejecución.

En Windows Vista y versiones posteriores, se proporciona un nuevo método para categorizar tanto los proveedores de servicios en capas de Winsock como las aplicaciones para que solo se carguen determinados LSP. Hay varias razones para agregar estas características.

Una de las razones principales es que determinados procesos críticos del sistema, como winlogon y lsass, crean sockets, pero estos procesos no usan estos sockets para enviar tráfico en la red. Por lo tanto, la mayoría de los LSP no deben cargarse en estos procesos. También se han documentado varios casos en los que los LSP con errores pueden provocar *lsass.exe* bloqueo. Si lsass se bloquea, el sistema fuerza un apagado. Un efecto secundario de estos procesos del sistema que cargan LSP es que estos procesos nunca se cierran, por lo que cuando se instala o quita un LSP, se requiere un reinicio.

Una razón secundaria es que hay algunos casos en los que es posible que las aplicaciones no quieran cargar determinados LSP. Por ejemplo, es posible que algunas aplicaciones no quieran cargar LSP criptográficos, lo que podría impedir que la aplicación se comunique con otros sistemas que no tienen instalado el LSP criptográfico.

Por último, otras LSP pueden usar categorías LSP para determinar dónde se deben instalar en la cadena del protocolo Winsock. Durante años, varios desarrolladores de LSP han deseado una manera de saber cómo se comportará un LSP. Por ejemplo, un LSP que inspeccione el flujo de datos querrá estar por encima de un LSP que cifre los datos. Por supuesto, este método de categorización de LSP no es una prueba sencilla, ya que se basa en LSP de terceros para clasificarse adecuadamente.

La categorización de LSP y otras mejoras de seguridad en Windows Vista y versiones posteriores están diseñadas para ayudar a evitar que los usuarios instalen LSP malintencionados de forma involuntaria.

## <a name="lsp-categories"></a>Categorías LSP

En Windows Vista y versiones posteriores, un LSP se puede clasificar en función de cómo interactúa con Windows sockets y datos. Una categoría LSP es un grupo identificable de comportamientos en un subconjunto de funciones SPI de Winsock. Por ejemplo, un filtro de contenido HTTP se clasificaría como un inspector de datos (la categoría INSPECTOR de \_ LSP). La categoría INSPECTOR de LSP \_ inspeccionará (pero no modificará) los parámetros para las funciones SPI de transferencia de datos. Una aplicación puede consultar la categoría de un LSP y elegir no cargar el LSP en función de la categoría LSP y el conjunto de categorías LSP permitidas de la aplicación.

En la tabla siguiente se enumeran las categorías en las que se puede clasificar un LSP.

| Categoría LSP              | Descripción                                                     |
|---------------------------|-----------------------------------------------------------------|
| **COMPRESIÓN DE \_ CRIPTOGRAFÍA LSP \_** | El LSP es un proveedor de criptografía o compresión de datos.         |
| **FIREWALL de LSP \_**         | El LSP es un proveedor de firewall.                                 |
| **CACHÉ LOCAL de \_ \_ LSP**     | El LSP es un proveedor de caché local.                              |
| **LSP \_ INBOUND \_ MODIFY**  | El LSP modifica los datos entrantes.                                  |
| **LSP \_ INSPECTOR**        | El LSP inspecciona o filtra los datos.                               |
| **LSP \_ OUTBOUND \_ MODIFY** | El LSP modifica los datos salientes.                                 |
| **LSP \_ PROXY**            | El LSP actúa como proxy y redirige los paquetes.                  |
| **LSP \_ REDIRECTOR**       | El LSP es un redirector de red.                                |
| **LSP \_ SYSTEM**           | El LSP es aceptable para su uso en servicios y procesos del sistema. |



 

Un LSP puede pertenecer a más de una categoría. Por ejemplo, un LSP de seguridad o firewall podría pertenecer a las categorías inspector **\_ (INSPECTOR de LSP)** y firewall **\_ (FIREWALL de LSP).**

Si un LSP no tiene un conjunto de categorías, se considera que está en la categoría Todos los demás. Esta categoría LSP no se cargará en servicios o procesos del sistema (por ejemplo, lsass, winlogon y muchos procesos svchost).

## <a name="categorizing-lsps"></a>Categorización de LSP

Hay varias funciones nuevas disponibles en Windows Vista y versiones posteriores para categorizar un LSP:

-   [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo)
-   [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32)
-   [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo)
-   [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32)

Para clasificar un LSP, se llama a la función [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo) o [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32) con un GUID para identificar la entrada oculta de LSP, la clase de información que se va a establecer para esta entrada del protocolo LSP y un conjunto de marcas que se usan para modificar el comportamiento de la función.

La [**función WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo) o [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32) se usa de forma similar para recuperar los datos asociados a una clase de información para un LSP.

## <a name="categorizing-applications"></a>Categorización de aplicaciones

Hay varias funciones nuevas disponibles en Windows Vista y versiones posteriores para categorizar una aplicación:

-   [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory)
-   [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory)

Para clasificar una aplicación, se llama a la función [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory) con la ruta de acceso de carga a la imagen ejecutable para identificar la aplicación, los argumentos de línea de comandos utilizados al iniciar la aplicación y las categorías LSP que se permiten para todas las instancias de esta aplicación.

La [**función WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory) se usa de forma similar para recuperar las categorías de proveedor de servicios por capas (LSP) asociadas a una aplicación.

## <a name="determining-which-lsps-get-loaded"></a>Determinar qué LSP se cargan

La parte final de la categorización de LSP es determinar qué LSP se cargarán en qué procesos. Cuando un proceso carga Winsock, se realizan las siguientes comparaciones de la categoría de aplicación y las categorías LSP para todos los LSP instalados:

-   Si la aplicación no se clasifica por categorías, permita que todos los LSP se carguen en el proceso.
-   Si la aplicación y el LSP tienen categorías asignadas, deben cumplirse todas las condiciones siguientes: <dl> Al menos una de las categorías LSP está presente en las categorías especificadas de la aplicación.  
    Solo las categorías especificadas en las categorías especificadas de la aplicación se especifican en las categorías LSP. Por ejemplo, si la aplicación especifica una categoría, debe estar en la categoría del LSP.  
    Si la categoría LSP SYSTEM está presente en la categoría de la aplicación, debe estar presente en las categorías \_ del LSP.  
    </dl>

> [!Note]  
> Si un LSP no se clasifica por categorías, su categoría es cero en la práctica. Para que se produzca una coincidencia, todas las categorías especificadas del LSP deben estar presentes en las categorías de la aplicación (las categorías de la aplicación deben ser un superconjunto de las categorías del LSP) con la advertencia de que si LSP SYSTEM está presente en la categoría de la aplicación, también debe estar presente en la categoría del \_ LSP.

 

Considere el ejemplo siguiente:

La *Foo.exe* aplicación se clasifica como LSP \_ SYSTEM + LSP \_ FIREWALL + LSP \_ CRYPTO \_ COMPRESS. La aplicación *Bar.exe* se clasifica como FIREWALL de LSP \_ + COMPRESIÓN \_ CRIPTOGRÁFICA de LSP. \_ Hay cuatro LSP instalados en el sistema:

-   LSP1 ha establecido una categoría de LSP \_ SYSTEM.
-   LSP2 no se establece en categorías, por lo que su categoría es cero.
-   LSP3 ha establecido una categoría de FIREWALL de \_ LSP.
-   LSP4 ha establecido categorías de LSP \_ SYSTEM + LSP \_ FIREWALL + LSP \_ CRYPTO COMPRESS + \_ LSP \_ INSPECTOR

En este ejemplo, la *Foo.exe* solo cargaría LSP1, mientras queBar.exeaplicación cargaría LSP3. 

## <a name="determining-winsock-providers-installed"></a>Determinar los proveedores de Winsock instalados

Microsoft Windows Software Development Kit (SDK) incluye un programa Winsock de ejemplo que se puede usar para determinar los proveedores de transporte de Winsock instalados en un equipo local. De forma predeterminada, el código fuente de este ejemplo de Winsock se instala en el siguiente directorio del SDK de Windows para Windows 7:

*C: \\ Archivos de programa sdk de Microsoft Windows \\ \\ \\ v7.0 \\ Samples \\ NetDs \\ winsock \\ LSP*

Este ejemplo es una utilidad para instalar y probar proveedores de servicios por capas. Pero también se puede usar para recopilar información detallada del catálogo winsock mediante programación en un equipo local. Para enumerar todos los proveedores actuales de Winsock, incluidos los proveedores base y los proveedores de servicios de capa, compile este ejemplo de Winsock y ejecute el siguiente comando de consola:

**instlsp -p**

La salida será una lista de proveedores de Winsock instalados en el equipo local, incluidos los proveedores de servicios en capas. La salida muestra el identificador de catálogo y el nombre de cadena del proveedor winsock.

Para recopilar información más detallada sobre todos los proveedores de Winsock, ejecute el siguiente comando de consola:

**instlsp -p -v**

La salida será una lista de [**estructuras info de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) admitidas en el equipo local.

Para obtener una lista de solo los proveedores de servicios en capas instalados en el equipo local, ejecute el siguiente comando de consola:

**instlsp -l**

Para asignar la estructura LSP, ejecute el siguiente comando de consola:

**instlsp -m**

> [!Note]  
> La característica TDI está en desuso y se quitará en versiones futuras de Microsoft Windows. En función de cómo use TDI, use el kernel de Winsock (WSK) o Windows filtering platform (WFP). Para obtener más información sobre WFP y WSK, [vea Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md) y [Winsock Kernel](/windows-hardware/drivers/ddi/_netvista/). Para obtener una Windows blog de redes básicas sobre WSK y TDI, consulte Introducción al [kernel de Winsock (WSK).](/archive/blogs/wndp/)

 

 

 
