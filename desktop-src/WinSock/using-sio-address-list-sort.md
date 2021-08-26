---
description: SIO ADDRESS LIST SORT IOCTL permite a los desarrolladores de aplicaciones ordenar una lista de direcciones de destino \_ IPv6 e IPv4 para determinar la mejor dirección disponible para realizar \_ \_ una conexión. SIO \_ ADDRESS \_ LIST SORT \_ IOCTL se admite en Windows XP y versiones posteriores.
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Uso de SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0bce27088052bfc029047d5f498ad90962567b50015a5331b26016e455d770
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121154"
---
# <a name="using-sio_address_list_sort"></a>Usar SIO \_ ADDRESS \_ LIST \_ SORT

**SIO \_ ADDRESS \_ LIST \_ SORT** IOCTL permite a los desarrolladores de aplicaciones ordenar una lista de direcciones de destino IPv6 e IPv4 para determinar la mejor dirección disponible para realizar una conexión. **SIO \_ ADDRESS \_ LIST \_ SORT** IOCTL se admite en Windows XP y versiones posteriores.

En Windows Vista y versiones posteriores, la función [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) toma una lista proporcionada de posibles direcciones de destino IP, empareja las direcciones de destino con las direcciones IP locales del equipo host y ordena los pares según el par de direcciones que sea más adecuado para la comunicación entre los dos elementos del mismo nivel. Se debe usar la función **CreateSortedAddressPairs** en lugar de **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL en Windows Vista y versiones posteriores.

En las secciones siguientes se describen las consideraciones de uso para **SIO \_ ADDRESS LIST \_ \_ SORT**.

## <a name="parameters"></a>Parámetros

El búfer pasado a **SIO \_ ADDRESS LIST SORT \_ \_ es** una [**estructura SOCKET ADDRESS \_ \_ LIST.**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) Cada [**DIRECCIÓN \_ DE SOCKET**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) de la lista debe estar en formato SOCKADDR \_ IN6.

**SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL ordena las direcciones IPv6 e IPv4 en Windows Vista y versiones posteriores. Las direcciones IPv4 de la lista que se van a ordenar deben tener el formato de dirección IPv6 asignada a IPv4. Para obtener más información sobre el formato de dirección IPv6 asignado a IPv4, vea [Sockets de pila dual.](dual-stack-sockets.md)

En Windows Server 2003 y Windows XP, **SIO \_ ADDRESS LIST \_ \_ SORT** ordena solo las direcciones IPv6. No se admiten direcciones IPv4 en el formato de dirección IPv6 asignada a IPv4.

En la salida, el miembro **iAddressCount** de la estructura [**SOCKET ADDRESS \_ \_ LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) puede ser menor que en la entrada si el código IOCTL determina que algunas direcciones de destino no son válidas.

## <a name="sorting-determination"></a>Determinación de la ordenación

El criterio de ordenación de las direcciones IPv6 para SIO ADDRESS LIST SORT IOCTL se \_ basa en la tabla de directivas de \_ \_ prefijos. La tabla de directivas de prefijo se configura *mediante* laNetsh.exelínea de comandos. Los siguientes fragmentos de código de línea de comandos ilustran *losNetsh.exe* de configuración de la tabla de directivas de prefijos básicos:

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> En Windows Server 2003 y Windows XP, el primer comando netsh mencionado anteriormente era el siguiente. Todos los demás comandos relacionados son los mismos.

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

La ordenación de direcciones también se determina mediante un algoritmo descrito en rfc 3484 en selección de direcciones predeterminadas para el protocolo de Internet versión *6 (IPv6)* publicado por el IETF. Para más información, consulte [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484). (Este recurso solo puede estar disponible en inglés).

**SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL ordena las direcciones de mejor a peor y rellena los miembros del identificador de ámbito **sin6, \_ \_** si es necesario. En el caso de las direcciones locales del sitio, SIO ADDRESS LIST SORT rellena el identificador de ámbito \_ \_ o quita la \_ dirección.

**SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL omite la dirección de origen enlazada al socket y solo se ordena por la lista de direcciones de destino pasada como parámetro.

Se debe usar la función [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) en lugar de **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL en Windows Vista y versiones posteriores. La **función CreateSortedAddressPairs** devuelve una lista de pares de direcciones que contiene una dirección de origen local y una dirección de destino. Esto proporciona a una aplicación la dirección de origen correcta que se usará para cada dirección de destino. Una aplicación también puede filtrar los resultados buscando una dirección de origen específica. en los resultados.

## <a name="requirements"></a>Requisitos

**SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL se define en el *archivo de encabezado Winsock2.h.* En el Kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL se define en el archivo de encabezado *Ws2def.h.* Tenga en cuenta que el archivo de encabezado *Ws2def.h* se incluye automáticamente en *Winsock2.h* y nunca se debe usar directamente.

**SIO \_ ADDRESS \_ LIST \_ SORT** IOCTL se admite en Windows XP y versiones posteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
