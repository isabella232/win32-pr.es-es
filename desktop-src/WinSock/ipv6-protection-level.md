---
description: La \_ opción de socket de nivel de protección IPv6 \_ permite a los desarrolladores colocar restricciones de acceso en sockets IPv6.
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2a8dd70bb1fb5b21f74f8939f11da0d9e2a3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696375"
---
# <a name="ipv6_protection_level"></a>\_Nivel de protección IPv6 \_

La \_ opción de socket de nivel de protección IPv6 \_ permite a los desarrolladores colocar restricciones de acceso en sockets IPv6. Estas restricciones permiten que una aplicación que se ejecuta en una LAN privada se fortalezca de forma sencilla frente a ataques externos. La \_ \_ opción de socket de nivel de protección IPv6 amplía o reduce el ámbito de un socket de escucha, lo que permite el acceso no restringido de usuarios públicos y privados cuando sea adecuado, o restringiendo el acceso únicamente al mismo sitio, según sea necesario.

El \_ nivel de protección IPv6 \_ tiene actualmente tres niveles de protección definidos.



| Nivel de protección                                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>nivel de protección no \_ \_ restringido<br/>       | Lo usan las aplicaciones diseñadas para funcionar a través de Internet, incluidas las aplicaciones que aprovechan las capacidades transversales NAT de IPv6 integradas en Windows (por ejemplo, Teredo). Estas aplicaciones pueden eludir los firewalls de IPv4, lo que hace necesario protegerlas frente a los ataques por Internet dirigidos al puerto abierto.<br/> |
| <span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>nivel de protección \_ \_ EDGERESTRICTED<br/> | Lo usan las aplicaciones diseñadas para funcionar a través de Internet. Esta configuración no permite el cruce seguro de NAT mediante la implementación de Teredo de Windows. Estas aplicaciones pueden eludir los firewalls de IPv4, lo que hace necesario protegerlas frente a los ataques por Internet dirigidos al puerto abierto.<br/>                                   |
| <span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>nivel de protección \_ \_ restringido<br/>             | Lo usan las aplicaciones de intranet que no implementan escenarios de Internet. Estas aplicaciones no se suelen probar ni proteger frente a los ataques por Internet.<br/> Este valor limitará el tráfico recibido a las direcciones locales de vínculo.<br/>                                                                             |



 

En el ejemplo de código siguiente se proporcionan los valores definidos para cada uno de ellos:

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

Estos valores son mutuamente excluyentes y no se pueden combinar en una [**sola llamada**](/windows/desktop/api/winsock/nf-winsock-setsockopt) a la función de un solo valor. Otros valores para esta opción de socket están reservados. Estos niveles de protección solo se aplican a las conexiones entrantes. El establecimiento de esta opción de Socket no tiene ningún efecto en las conexiones o los paquetes salientes.

En Windows 7 y Windows Server 2008 R2, el valor predeterminado para el \_ nivel de protección IPv6 \_ es no especificado y el **nivel de protección \_ \_ predeterminado** está definido en-1, un valor no válido para el \_ nivel de protección IPv6 \_ .

En Windows Vista y Windows Server 2008, el valor predeterminado para el \_ nivel de protección IPv6 \_ es **nivel de protección no \_ \_ restringido** y el **nivel de protección \_ \_ predeterminado** está definido en-1, un valor no válido para el \_ nivel de protección IPv6 \_ .

En Windows Server 2003 y Windows XP, el valor predeterminado del nivel de protección IPV6 es el nivel de \_ \_ **protección \_ \_ EDGERESTRICTED** y el nivel de **protección \_ \_ predeterminado** se define como **nivel de protección \_ \_ EDGERESTRICTED**.

> [!Note]  
> La \_ opción de socket de nivel de protección IPv6 \_ debe establecerse antes de enlazar el socket. De lo contrario, los paquetes recibidos entre [**las llamadas de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) y el tipo de llamada se ajustarán al **nivel de protección \_ \_ EDGERESTRICTED** y se pueden entregar a la aplicación.

 

En la tabla siguiente se describe el efecto de aplicar cada nivel de protección a un socket de escucha.

Nivel de protección

Tráfico entrante permitido

Mismo sitio

Externo

NAT transversal (Teredo)

nivel de protección \_ \_ restringido

Sí

No

No

nivel de protección \_ \_ EDGERESTRICTED

Sí

Sí

No

nivel de protección no \_ \_ restringido

Sí

Sí

Sí



 

En la tabla anterior, la **misma** columna de sitio es una combinación de lo siguiente:

-   Vincular direcciones locales
-   Direcciones locales del sitio
-   Direcciones globales conocidas para pertenecer al mismo sitio (que coincide con la tabla de prefijo del sitio)

En Windows 7 y Windows Server 2008 R2, el valor predeterminado del \_ nivel de protección IPv6 \_ no está especificado. Si no hay ningún software de Firewall compatible con el recorrido perimetral instalado en el equipo local (Firewall de Windows está deshabilitado o hay otro Firewall instalado que omite el tráfico Teredo), recibirá el tráfico Teredo solo si establece la \_ opción de socket de nivel de protección IPv6 en el nivel de protección no \_ **\_ \_ restringido**. Sin embargo, el Firewall de Windows o cualquier directiva de Firewall compatible con el recorrido perimetral puede omitir esta opción en función de la configuración de directivas del firewall. Al establecer esta opción de socket en el **nivel de protección no \_ \_ restringido**, la aplicación está comunicando su intención explícita de recibir tráfico recorrido por el perímetro por el firewall del host instalado en el equipo local. Por tanto, si hay un firewall de host compatible con el recorrido perimetral instalado, tendrá la decisión final de aceptar un paquete. De forma predeterminada, sin ningún conjunto de opciones de socket:

-   o si firewall de Windows está habilitado (u otro Firewall de host compatible con el recorrido perimetral está instalado) en el equipo local, se observará lo que se aplique. El firewall del host con reconocimiento perimetral típico bloqueará el tráfico Teredo de forma predeterminada. Por lo tanto, las aplicaciones observarán el valor predeterminado como si fuera el **nivel de protección \_ \_ EDGERESTRICTED**.
-   o si firewall de Windows no está habilitado y ningún otro Firewall de host compatible con el recorrido perimetral está instalado en el sistema local, el valor predeterminado será **nivel de protección \_ \_ EDGERESTRICTED**.

En Windows Vista y Windows Server 2008, el valor predeterminado para el \_ nivel de protección IPv6 \_ es **nivel de protección no \_ \_ restringido**. Pero el valor efectivo depende de si firewall de Windows está habilitado. El Firewall de Windows es compatible con el recorrido perimetral (compatible con Teredo), independientemente del valor que se haya establecido para el \_ nivel de protección IPv6 \_ y se omite si el nivel de protección IPv6 \_ \_ es nivel de **protección no \_ \_ restringido**. Por lo tanto, el valor efectivo depende de la Directiva de Firewall. Cuando Firewall de Windows está deshabilitado y ningún otro Firewall compatible con el recorrido perimetral está instalado en el equipo local, el valor predeterminado para el \_ nivel de protección IPv6 \_ es nivel de **protección no \_ \_ restringido**.

En Windows Server 2003 y Windows XP, el valor predeterminado para el \_ nivel de protección IPv6 \_ es el nivel de **protección \_ \_ EDGERESTRICTED**. A menos que haya establecido la \_ opción de socket de nivel de protección IPv6 \_ en el nivel de **protección no \_ \_ restringido**, no recibirá ningún tráfico Teredo.

Según el nivel de protección de IPV6 \_ \_ , es posible que una aplicación que requiera tráfico no solicitado de Internet no pueda recibir tráfico no solicitado. Sin embargo, estos requisitos no son necesarios para recibir tráfico solicitado a través de la interfaz Teredo de Windows. Para obtener más información sobre la interacción con Teredo, consulte [recibir tráfico solicitado a través de Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).

Cuando se rechazan los paquetes entrantes o las conexiones debido al nivel de protección establecido, el rechazo se controla como si ninguna aplicación estuviera escuchando en ese socket.

> [!Note]
>
> La \_ opción de socket de nivel de protección IPv6 \_ no impone necesariamente restricciones de acceso en sockets IPv6 o restringe el recorrido NAT mediante algún método distinto de Teredo de Windows o incluso usando otra implementación de Teredo por otro proveedor.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[Recibir tráfico solicitado a través de Teredo](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
