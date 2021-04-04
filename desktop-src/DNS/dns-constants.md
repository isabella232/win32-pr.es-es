---
title: Constantes de DNS
description: Las siguientes constantes se definen para DNS en el orden de bytes del host.
ms.assetid: 95bc9193-7962-498a-9abd-c4718ac35f0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64497e14d6c4ae11f4a6ed68200614aa4f602270
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104077372"
---
# <a name="dns-constants"></a>Constantes de DNS

Las siguientes constantes se definen para DNS en el orden de bytes del host.

## <a name="dns-record-types"></a>Tipos de registros DNS



| Constante           | Value            |
|--------------------|------------------|
| \_tipo \_ de DNS A       | 0x0001           |
| tipo de DNS \_ \_ NS      | 0x0002           |
| tipo de DNS \_ \_ MD      | 0x0003           |
| tipo de DNS \_ \_ MF      | 0x0004           |
| tipo de DNS \_ \_ CNAME   | 0x0005           |
| tipo de DNS \_ \_ SOA     | 0x0006           |
| tipo de DNS \_ \_ MB      | 0x0007           |
| tipo de DNS \_ \_ mg      | 0x0008           |
| tipo de DNS \_ \_ Mr      | 0x0009           |
| tipo de DNS \_ \_ null    | 0x000a           |
| tipo de DNS \_ \_ WKS     | 0x000b           |
| tipo de DNS \_ \_ ptr     | 0x000c           |
| tipo de DNS \_ \_ HINFO   | 0x000d           |
| tipo de DNS \_ \_ MINFO   | 0x000e           |
| tipo de DNS \_ \_ mx      | 0x000f           |
| \_texto de tipo DNS \_    | 0x0010           |
| tipo de DNS \_ \_ RP      | 0x0011           |
| tipo de DNS \_ \_ AFSDB   | 0x0012           |
| Tipo de DNS \_ \_ x25     | 0x0013           |
| tipo de DNS \_ \_ ISDN    | 0x0014           |
| tipo de DNS \_ \_ RT      | 0x0015           |
| tipo de DNS \_ \_ NSAP    | 0x0016           |
| tipo de DNS \_ \_ NSAPPTR | 0x0017           |
| tipo de DNS \_ \_ SIG     | 0x0018           |
| \_clave de tipo DNS \_     | 0x0019           |
| tipo de DNS \_ \_ PX      | 0x001a           |
| \_GPO de tipo DNS \_    | 0x001b           |
| tipo de DNS \_ \_ AAAA    | 0x001c           |
| tipo de DNS \_ \_ Loc     | 0x001d           |
| tipo de DNS \_ \_ NXT     | 0x001e           |
| tipo de DNS \_ \_ Eid     | 0x001f           |
| tipo de DNS \_ \_ NIMLOC  | 0x0020           |
| tipo de DNS \_ \_ SRV     | 0x0021           |
| tipo de DNS \_ \_ Atma    | 0x0022           |
| tipo de DNS \_ \_ NAPTR   | 0x0023           |
| tipo de DNS \_ \_ KX      | 0x0024           |
| \_certificado de tipo DNS \_    | 0x0025           |
| Tipo de DNS \_ \_ A6      | 0x0026           |
| tipo de DNS \_ \_ dname   | 0x0027           |
| \_receptor de tipo DNS \_    | 0x0028           |
| tipo de DNS \_ \_ OPT     | 0x0029           |
| tipo de DNS \_ \_ DS      | 0x002B           |
| tipo de DNS \_ \_ RRSIG   | 0x002E           |
| tipo de DNS \_ \_ NSEC    | 0x002F           |
| tipo de DNS \_ \_ DNSKEY  | 0x0030           |
| tipo de DNS \_ \_ DHCID   | 0x0031           |
| tipo de DNS \_ \_ UINFO   | 0x0064           |
| \_UID de tipo DNS \_     | 0x0065           |
| tipo de DNS \_ \_ GID     | 0x0066           |
| tipo de DNS \_ sin \_ especificación  | 0x0067           |
| \_direcciones de tipo DNS \_   | 0x00f8           |
| tipo de DNS \_ \_ TKey    | 0x00f9           |
| tipo de DNS \_ \_ TSIG    | 0x00fa           |
| tipo de DNS \_ \_ IXFR    | 0x00fb           |
| tipo de DNS \_ \_ AXFR    | 0x00fc           |
| tipo de DNS \_ \_ MAILB   | 0x00fd           |
| tipo de DNS \_ \_ correo electrónico   | 0x00fe           |
| tipo de DNS \_ \_ todo     | 0x00ff           |
| \_tipo DNS \_ any     | 0x00ff           |
| \_tipo DNS \_ WINS    | 0xff01           |
| tipo de DNS \_ \_ WINSR   | 0xff02           |
| tipo de DNS \_ \_ NBSTAT  | tipo de DNS \_ \_ WINSR |



 

## <a name="dns-class-types"></a>Tipos de clase DNS



| Constante             | Value  |
|----------------------|--------|
| Internet de la \_ clase DNS \_ | 0x0001 |
| \_CSNET de clase DNS \_    | 0x0002 |
| \_caos de clase DNS \_    | 0x0003 |
| \_HESIOD de clase DNS \_   | 0x0004 |
| \_clase DNS \_ ninguno     | 0x00fe |
| \_clase DNS \_ All      | 0x00ff |
| \_clase DNS \_ any      | 0x00ff |



 

## <a name="dns-query-types"></a>Tipos de consultas DNS



| Constante                    | Value  |
|-----------------------------|--------|
| \_consulta de código de operación DNS \_          | 0x0000 |
| \_IQUERY de código de operación DNS \_         | 0x0001 |
| Estado del servidor de código de \_ operación DNS \_ \_ | 0x0002 |
| código de operación de DNS \_ \_ desconocido        | 0x0003 |
| \_notificación de código de operación DNS \_         | 0x0004 |
| \_actualización de código de operación DNS \_         | 0x0005 |



 

## <a name="dns-record-flags"></a>Marcas de registro DNS

Las marcas siguientes hacen referencia a la sección de un registro de recursos (RR) dentro de un mensaje DNS:



| Constante           | Value      | Significado                         |
|--------------------|------------|---------------------------------|
| DNSREC \_ pregunta   | 0x00000000 | RR está en la sección de preguntas   |
| respuesta de DNSREC \_     | 0x00000001 | RR está en la sección de respuestas     |
| \_autoridad DNSREC  | 0x00000002 | RR está en la sección Authority  |
| DNSREC \_ adicionales | 0x00000003 | RR está en la sección adicional |



 

Las marcas siguientes hacen referencia a la sección de un RR dentro de un mensaje de actualización de DNS por [RFC 2136](https://www.ietf.org/rfc/rfc2136.txt):



| Constante       | Value      | Significado                           |
|----------------|------------|-----------------------------------|
| \_zona DNSREC   | 0x00000000 | RR está en la sección Zone         |
| DNSREC \_ PREREQ | 0x00000001 | RR está en la sección de requisitos previos |
| actualización de DNSREC \_ | 0x00000002 | RR está en la sección de actualización       |



 

Las marcas siguientes se excluyen mutuamente:



| Constante        | Value      | Significado                                                    |
|-----------------|------------|------------------------------------------------------------|
| DNSREC \_ eliminar  | 0x00000004 | Elimine un RR. Se usa junto con la \_ actualización de DNSREC       |
| DNSREC no \_ existe | 0x00000004 | RR no existe. Se usa junto con DNSREC \_ PREREQ |



 

## <a name="dns-query-options"></a>Opciones de consulta de DNS



| Constante                                | Value      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_estándar de consulta DNS \_                    | 0x00000000 | Consulta estándar.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| la \_ consulta DNS \_ acepta la \_ respuesta truncada \_ | 0x00000001 | Devuelve los resultados truncados. No vuelve a intentarlo en TCP.                                                                                                                                                                                                                                                                                                                                                                                                   |
| la \_ consulta \_ DNS \_ usa \_ solo TCP              | 0x00000002 | Usa TCP solo para la consulta.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_consulta DNS \_ sin \_ recursividad               | 0x00000004 | Indica al servidor DNS que realice una consulta iterativa (concretamente indica al servidor DNS que no realice la resolución recursiva para resolver la consulta).                                                                                                                                                                                                                                                                                                   |
| \_caché de \_ omisión de consultas DNS \_               | 0x00000008 | Omite la memoria caché de la [*resolución*](r-gly.md) en la búsqueda.                                                                                                                                                                                                                                                                                                                                                                            |
| consulta \_ DNS \_ sin \_ conexión \_             | 0x00000010 | Indica a DNS que realice una consulta solo en la caché local. **Windows 2000 Server y windows 2000 Professional:** Este valor no se admite. Para obtener una funcionalidad similar, use la **caché de consultas de DNS \_ \_ \_ únicamente**.<br/>                                                                                                                                                                                                                                      |
| \_consulta DNS \_ sin \_ \_ nombre local             | 0x00000020 | Indica a DNS que omita el nombre local. **Windows 2000 Server y windows 2000 Professional:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                    |
| \_archivo de \_ no \_ hosts de consulta DNS \_             | 0x00000040 | Impide que la consulta DNS consulte el archivo de hosts. **Windows 2000 Server y windows 2000 Professional:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                   |
| \_consulta DNS \_ sin \_ NetBT                   | 0x00000080 | Impide que la consulta DNS use NetBT para la resolución. **Windows 2000 Server y windows 2000 Professional:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                  |
| \_ \_ solo conexión de \_ DNS                  | 0x00000100 | Indica a DNS que realice una consulta solo con la red, omitiendo la información local. **Windows 2000 Server y windows 2000 Professional:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                      |
| \_mensaje de \_ devolución de consulta DNS \_             | 0x00000200 | Indica a DNS que devuelva el mensaje de respuesta DNS completo. **Windows 2000 Server y windows 2000 Professional:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                   |
| \_ \_ solo multidifusión de consulta DNS \_             | 0x00000400 | Impide que la consulta use DNS y solo usa la resolución de nombres de multidifusión de vínculo local (LLMNR). **Windows Vista y Windows Server 2008 o posterior.:** Se admite este valor.<br/>                                                                                                                                                                                                                                                                  |
| \_consulta DNS \_ sin \_ multidifusión               | 0x00000800 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| la \_ consulta DNS se \_ trata \_ como \_ FQDN             | 0x00001000 | Impide que la respuesta DNS adjunte sufijos al nombre enviado en un proceso de resolución de nombres.                                                                                                                                                                                                                                                                                                                                                  |
| \_ADDRCONFIG de consulta DNS \_                  | 0x00002000 | Solo Windows 7: [**no enviar consultas de tipo**](/windows/win32/api/windns/ns-windns-dns_a_data) si las direcciones IPv4 no están disponibles en una interfaz y no envían consultas de tipo [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) si las direcciones IPv6 no están disponibles.                                                                                                                                                                                                                                   |
| dir de consulta de DNS \_ \_ dual \_                  | 0x00004000 | Solo Windows 7: consulta los registros de tipo [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) y [**a**](/windows/win32/api/windns/ns-windns-dns_a_data) y devuelve los resultados de cada uno de ellos. Los resultados de **un** tipo de registros se asignan al tipo **AAAA** .                                                                                                                                                                                                                                                           |
| \_espera de \_ multidifusión de consulta DNS \_             | 0x00020000 | Espera un tiempo de espera completo para recopilar todas las respuestas del vínculo local. Si no se establece, el comportamiento predeterminado es devolver con la primera respuesta. **Windows Vista y Windows Server 2008 o posterior.:** Se admite este valor.<br/>                                                                                                                                                                                                              |
| \_comprobación de \_ multidifusión de consulta DNS \_           | 0x00040000 | Dirige una prueba mediante el nombre de host del equipo local para comprobar la unicidad del nombre en el mismo vínculo local. Recopila todas las respuestas incluso si el comportamiento normal del remitente de LLMNR no está habilitado. **Windows Vista y Windows Server 2008 o posterior.:** Se admite este valor.<br/>                                                                                                                                                                                  |
| la \_ consulta DNS no \_ \_ restablece \_ \_ los valores de TTL    | 0x00100000 | Si se establece, y si la respuesta contiene varios registros, los registros se almacenan con el TTL correspondiente al valor TTL mínimo de entre todos los registros. Cuando se establece esta opción, no se modifica el valor "no cambiar el TTL de los registros individuales" del conjunto de registros devueltos.                                                                                                                                                                               |
| \_deshabilitar \_ la \_ \_ codificación IDN en la consulta DNS      | 0x00200000 | Deshabilita la compatibilidad con la codificación de nombres de dominio internacionales (IDN) en las API [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a), [**DnsQueryEx**](/windows/desktop/api/Windns/nf-windns-dnsqueryex), [**DnsModifyRecordsInSet**](/windows/desktop/api/Windns/nf-windns-dnsmodifyrecordsinset_a)y [**DnsReplaceRecordSet**](/windows/desktop/api/Windns/nf-windns-dnsreplacerecordseta) . Todos los nombres Punycode se tratan como ASCII y estarán codificados en ASCII en la conexión. Todos los nombres que no son ASCII se codifican en UTF8 en la conexión. **Windows 8 o posterior.:** Se admite este valor.<br/> |
| \_ \_ anexar una \_ etiqueta a la consulta DNS          | 0x00800000 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_consulta DNS \_ reservada                    | 0xf0000000 | Reservado.                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="dns-update-options"></a>Opciones de actualización de DNS



| Constante                                 | Value      | Significado                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ uso \_ predeterminado de la seguridad de actualización de DNS      | 0x00000000 | Usa el comportamiento predeterminado, que se especifica en el registro, para las actualizaciones DNS dinámicas seguras.                                                                |
| seguridad de actualización de DNS \_ \_ \_ desactivada               | 0x00000010 | No intenta realizar actualizaciones dinámicas seguras.                                                                                                                      |
| \_ \_ seguridad de actualización \_ de DNS activada                | 0x00000020 | Intenta una actualización dinámica no segura; Si se rechaza, intenta realizar una actualización dinámica segura.                                                                               |
| \_ \_ solo seguridad de actualización de DNS \_              | 0x00000100 | Intenta solo actualizaciones dinámicas seguras.                                                                                                                         |
| \_contexto de \_ seguridad de caché de actualización de DNS \_ \_    | 0x00000200 | Almacena en caché el contexto de seguridad para su uso en transacciones futuras.                                                                                                   |
| la \_ prueba de actualización de DNS \_ \_ usa \_ local \_ Sys \_ acct | 0x00000400 | Usa las credenciales de la cuenta de equipo local.                                                                                                               |
| seguridad de fuerza de actualización de DNS \_ \_ \_ \_ nego       | 0x00000800 | No utiliza el contexto de seguridad almacenado en caché.                                                                                                                         |
| actualización de DNS \_ \_ pruebe \_ todos los \_ \_ servidores maestros   | 0x00001000 | Envía actualizaciones de DNS a todos los servidores DNS con varios maestros.                                                                                                            |
| actualización de DNS \_ \_ no omitir \_ \_ adaptadores de actualización \_  | 0x00002000 | No actualice los adaptadores en los que estén deshabilitadas las actualizaciones de DNS dinámico. **Windows 2000 Server con SP2 o posterior.:** Se admite este valor.<br/>                 |
| \_ \_ servidor remoto de actualización de DNS \_              | 0x00004000 | Registrar registros CNAME en un servidor remoto además del servidor DNS local. **Windows 2000 Server con SP2 o posterior.:** Se admite este valor.<br/> |
| actualización de DNS \_ \_ reservada                    | 0xffff0000 | Reservado para uso futuro.                                                                                                                                      |



 

## <a name="dns-response-codes"></a>Códigos de respuesta DNS



| Error                | Significado                                        |
|----------------------|------------------------------------------------|
| \_error de RCODE de DNS \_  | Sin errores                                       |
| \_RCODE DNS \_ anterior  | Error de formato                                   |
| \_SERVFAIL RCODE \_ DNS | Error de servidor                                 |
| \_NXDOMAIN RCODE \_ DNS | Error de nombre                                     |
| \_NOTIMPL RCODE \_ DNS  | No implementado                                |
| \_RCODE DNS \_ rechazado  | Conexión rechazada                             |
| \_YXDOMAIN RCODE \_ DNS | No debe existir el nombre de dominio                   |
| \_YXRRSET RCODE \_ DNS  | No debe existir un conjunto de registros de recursos (RR)      |
| \_NXRRSET RCODE \_ DNS  | El conjunto de RR no existe                          |
| \_NOTAUTH RCODE \_ DNS  | No es autoritativo para la zona                     |
| \_NOTZONE RCODE \_ DNS  | Nombre no en zona                               |
| \_BADVERS RCODE \_ DNS  | Mecanismo de extensión incorrecta para la versión de DNS (EDNS) |
| \_BADSIG RCODE \_ DNS   | Firma incorrecta                                  |
| \_BADKEY RCODE \_ DNS   | Clave incorrecta                                        |
| \_BADTIME RCODE \_ DNS  | Marca de tiempo incorrecta                                  |



 

 

 





