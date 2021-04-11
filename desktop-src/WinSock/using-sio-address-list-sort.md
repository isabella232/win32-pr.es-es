---
description: El \_ ioctl de \_ \_ ordenación de la lista de direcciones de SiO permite a los desarrolladores de aplicaciones ordenar una lista de direcciones IPv6 e IPv4 de destino para determinar la mejor dirección disponible para establecer una conexión. El \_ \_ ioctl de ordenación de la lista de direcciones \_ de SiO es compatible con Windows XP y versiones posteriores.
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Usar SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6452023b69ccf72c78b393c5059fee497997af51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278785"
---
# <a name="using-sio_address_list_sort"></a>Usar la \_ ordenación de la lista de direcciones de SiO \_ \_

El ioctl de **\_ \_ \_ ordenación** de la lista de direcciones de SiO permite a los desarrolladores de aplicaciones ordenar una lista de direcciones IPv6 e IPv4 de destino para determinar la mejor dirección disponible para establecer una conexión. El ioctl de **\_ \_ \_ ordenación** de la lista de direcciones de SiO es compatible con Windows XP y versiones posteriores.

En Windows Vista y versiones posteriores, la función [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) toma una lista proporcionada de posibles direcciones IP de destino, empareja las direcciones de destino con las direcciones IP locales de la máquina host y ordena los pares según el par de direcciones más adecuado para la comunicación entre los dos elementos del mismo nivel. Se debe usar la función **CreateSortedAddressPairs** en lugar de la **lista de direcciones de SiO \_ \_ \_ ordenar** ioctl en Windows Vista y versiones posteriores.

En las secciones siguientes se describen las consideraciones de uso para la **\_ \_ \_ ordenación** de la lista de direcciones de SiO.

## <a name="parameters"></a>Parámetros

El búfer pasado a **la \_ \_ \_ ordenación** de la lista de direcciones de SiO es una estructura de [**\_ \_ lista de direcciones de socket**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) . Cada [**\_ dirección de socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) de la lista debe tener el \_ formato SOCKADDR IN6.

La **\_ \_ \_ ordenación** de la lista de direcciones de SiO ordena las direcciones IPv6 e IPv4 en Windows Vista y versiones posteriores. Cualquier dirección IPv4 de la lista que se va a ordenar debe estar en el formato de dirección IPv6 asignado a IPv4. Para obtener más información sobre el formato de dirección IPv6 asignado a IPv4, consulte [sockets de dos pilas](dual-stack-sockets.md).

En Windows Server 2003 y Windows XP, la **\_ \_ \_ ordenación** de la lista de direcciones de SiO solo ordena direcciones IPv6. No se admiten las direcciones IPv4 en el formato de dirección IPv6 asignado a IPv4.

En la salida, el miembro **iAddressCount** de la estructura de la [**lista de \_ direcciones \_ de socket**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) puede ser menor que en la entrada si el código ioctl determina que algunas direcciones de destino no son válidas.

## <a name="sorting-determination"></a>Determinación de ordenación

El criterio de ordenación para las direcciones IPv6 para la lista de direcciones de SIO la \_ \_ \_ ordenación ioctl se basa en la tabla de directivas de prefijos. La tabla de directivas de prefijos se configura mediante la utilidad de línea de comandos *Netsh.exe* . Los siguientes fragmentos de código de línea de comandos ilustran los comandos de configuración de tabla de directiva de prefijo *Netsh.exe* básica:

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> En Windows Server 2003 y Windows XP, el primer comando netsh indicado anteriormente era el siguiente. Todos los demás comandos relacionados son los mismos.

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

La ordenación de direcciones también viene determinada por un algoritmo descrito en la RFC 3484 en la *selección de direcciones predeterminada para el protocolo de Internet versión 6 (IPv6)* publicado por IETF. Para más información, consulte [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484). (Este recurso solo está disponible en inglés).

La **\_ \_ \_ ordenación** de la lista de direcciones de SiO ordena las direcciones de mejor a peor, y rellena los miembros de **\_ \_ identificador de ámbito de sin6** , si es necesario. En el caso de las direcciones locales del sitio, \_ la ordenación de la lista de direcciones de SiO se \_ \_ rellena en el identificador de ámbito o quita la dirección.

El ioctl de **\_ \_ \_ ordenación** de la lista de direcciones de SiO omite la dirección de origen enlazada al socket y solo ordena por la lista de direcciones de destino pasada como un parámetro.

Se debe usar la función [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) en lugar de la **lista de direcciones de SiO \_ \_ \_ ordenar** ioctl en Windows Vista y versiones posteriores. La función **CreateSortedAddressPairs** devuelve una lista de pares de direcciones que contiene una dirección de origen local y una dirección de destino. Esto proporciona a una aplicación la dirección de origen correcta que se va a usar para cada dirección de destino. Una aplicación también puede filtrar los resultados buscando una dirección de origen concreta. en los resultados.

## <a name="requirements"></a>Requisitos

El ioctl de **\_ \_ \_ ordenación** de la lista de direcciones de SiO se define en el archivo de encabezado *WinSock2. h* . En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y la **lista de direcciones de dirección de SiO \_ \_ \_** se define ioctl en el archivo de encabezado *Ws2def. h* . Tenga en cuenta que el archivo de encabezado *Ws2def. h* se incluye automáticamente en *WinSock2. h* y nunca se debe usar directamente.

El ioctl de **\_ \_ \_ ordenación** de la lista de direcciones de SiO es compatible con Windows XP y versiones posteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
