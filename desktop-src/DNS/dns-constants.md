---
title: Constantes DNS
description: Las siguientes constantes se definen para DNS en orden de bytes de host.
ms.assetid: 95bc9193-7962-498a-9abd-c4718ac35f0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64497e14d6c4ae11f4a6ed68200614aa4f602270
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164745"
---
# <a name="dns-constants"></a>Constantes DNS

Las siguientes constantes se definen para DNS en orden de bytes de host.

## <a name="dns-record-types"></a>Tipos de registros DNS



| Constante           | Value            |
|--------------------|------------------|
| TIPO DE DNS \_ \_ A       | 0x0001           |
| DNS \_ TYPE \_ NS      | 0x0002           |
| MD \_ DE TIPO \_ DNS      | 0x0003           |
| TIPO DNS \_ \_ MF      | 0x0004           |
| TIPO \_ DNS \_ CNAME   | 0x0005           |
| SOA \_ DE TIPO \_ DNS     | 0x0006           |
| TIPO \_ DNS \_ MB      | 0x0007           |
| MG \_ DE TIPO \_ DNS      | 0x0008           |
| MR \_ DE TIPO \_ DNS      | 0x0009           |
| TIPO \_ DE \_ DNS NULL    | 0x000a           |
| \_ \_ WKS DE TIPO DNS     | 0x000b           |
| TIPO \_ DNS \_ PTR     | 0x000c           |
| HINFO \_ DE TIPO \_ DNS   | 0x000d           |
| MINFO \_ DE TIPO \_ DNS   | 0x000e           |
| DNS \_ TYPE \_ MX      | 0x000f           |
| TEXTO \_ DE TIPO \_ DNS    | 0x0010           |
| RP \_ DE TIPO \_ DNS      | 0x0011           |
| \_AFSDB DE TIPO \_ DNS   | 0x0012           |
| TIPO \_ DNS \_ X25     | 0x0013           |
| \_ISDN DE TIPO \_ DNS    | 0x0014           |
| TIPO \_ DE \_ DNS RT      | 0x0015           |
| \_NSAP DE \_ TIPO DNS    | 0x0016           |
| TIPO \_ DNS \_ NSAPPTR | 0x0017           |
| SIG \_ DE TIPO \_ DNS     | 0x0018           |
| CLAVE \_ DE TIPO \_ DNS     | 0x0019           |
| TIPO \_ \_ DE DNS PX      | 0x001a           |
| GPO \_ \_ DE TIPO DNS    | 0x001b           |
| TIPO \_ \_ DNS AAAA    | 0x001c           |
| LOC \_ DE \_ TIPO DNS     | 0x001d           |
| TIPO \_ \_ DNS NXT     | 0x001e           |
| EID \_ DE \_ TIPO DNS     | 0x001f           |
| TIPO \_ DNS \_ NIMLOC  | 0x0020           |
| SRV \_ DE TIPO \_ DNS     | 0x0021           |
| ATMA \_ DE TIPO \_ DNS    | 0x0022           |
| TIPO \_ DNS \_ NAPTR   | 0x0023           |
| DNS \_ TYPE \_ KX      | 0x0024           |
| CERTIFICADO \_ DE TIPO \_ DNS    | 0x0025           |
| TIPO \_ \_ DNS A6      | 0x0026           |
| DNS \_ TYPE \_ DNAME   | 0x0027           |
| RECEPTOR \_ DE TIPO \_ DNS    | 0x0028           |
| DNS \_ TYPE \_ OPT     | 0x0029           |
| DNS \_ TYPE \_ DS      | 0x002B           |
| \_RRSIG DE TIPO \_ DNS   | 0x002E           |
| TIPO \_ \_ DNS NSEC    | 0x002F           |
| DNS \_ TYPE \_ DNSKEY  | 0x0030           |
| TIPO \_ \_ DNS DHCID   | 0x0031           |
| TIPO \_ DNS \_ UINFO   | 0x0064           |
| UID \_ DE \_ TIPO DNS     | 0x0065           |
| GID \_ DE TIPO \_ DNS     | 0x0066           |
| TIPO \_ DNS \_ UNSPEC  | 0x0067           |
| DNS \_ TYPE \_ ADDRS   | 0x00f8           |
| TKEY \_ DE TIPO \_ DNS    | 0x00f9           |
| \_TSIG DE \_ TIPO DNS    | 0x00fa           |
| IXFR \_ DE TIPO \_ DNS    | 0x00fb           |
| AXFR \_ DE TIPO \_ DNS    | 0x00fc           |
| TIPO \_ DNS \_ MAILB   | 0x00fd           |
| TIPO \_ DNS \_ MAILA   | 0x00fe           |
| TIPO DE DNS \_ \_ ALL     | 0x00ff           |
| DNS \_ TYPE \_ ANY     | 0x00ff           |
| EL \_ TIPO DNS \_ GANA    | 0xff01           |
| WINSR \_ DE TIPO \_ DNS   | 0xff02           |
| TIPO \_ DNS \_ NBSTAT  | WINSR \_ DE TIPO \_ DNS |



 

## <a name="dns-class-types"></a>Tipos de clase DNS



| Constante             | Value  |
|----------------------|--------|
| CLASE \_ DNS \_ INTERNET | 0x0001 |
| CLASE \_ \_ DNS CSNET    | 0x0002 |
| CAOS \_ DE CLASE \_ DNS    | 0x0003 |
| CLASE \_ \_ DNS HESIOD   | 0x0004 |
| CLASE \_ DNS \_ NONE     | 0x00fe |
| DNS \_ CLASS \_ ALL      | 0x00ff |
| CLASE \_ DNS \_ ANY      | 0x00ff |



 

## <a name="dns-query-types"></a>Tipos de consultas DNS



| Constante                    | Value  |
|-----------------------------|--------|
| CONSULTA \_ DE CÓDIGO DE OPERACIÓN DE \_ DNS          | 0x0000 |
| IQUERY \_ DE CÓDIGO DE OPERACIÓN DE \_ DNS         | 0x0001 |
| ESTADO \_ DEL SERVIDOR DE CÓDIGO DE OPERACIÓN \_ \_ DNS | 0x0002 |
| CÓDIGO \_ DE OPERACIÓN DNS \_ DESCONOCIDO        | 0x0003 |
| NOTIFICACIÓN \_ DE CÓDIGO DE OPERACIÓN \_ DNS         | 0x0004 |
| ACTUALIZACIÓN \_ DE CÓDIGO DE OPERACIÓN DE \_ DNS         | 0x0005 |



 

## <a name="dns-record-flags"></a>Marcas de registro DNS

Las marcas siguientes hacen referencia a la sección de un registro de recursos (RR) dentro de un mensaje DNS:



| Constante           | Value      | Significado                         |
|--------------------|------------|---------------------------------|
| PREGUNTA \_ DE DNSREC   | 0x00000000 | RR está en la sección de preguntas   |
| RESPUESTA \_ DNSREC     | 0x00000001 | RR está en la sección de respuesta     |
| DNSREC \_ AUTHORITY  | 0x00000002 | RR está en la sección de autoridad.  |
| DNSREC \_ ADDITIONAL | 0x00000003 | RR está en la sección adicional. |



 

Las marcas siguientes hacen referencia a la sección de un RR dentro de un mensaje DNS de actualización por [RFC 2136](https://www.ietf.org/rfc/rfc2136.txt):



| Constante       | Value      | Significado                           |
|----------------|------------|-----------------------------------|
| ZONA \_ DNSREC   | 0x00000000 | RR está en la sección zona         |
| DNSREC \_ PREREQ | 0x00000001 | RR está en la sección de requisitos previos |
| ACTUALIZACIÓN \_ DE DNSREC | 0x00000002 | RR está en la sección de actualización.       |



 

Las marcas siguientes son mutuamente excluyentes:



| Constante        | Value      | Significado                                                    |
|-----------------|------------|------------------------------------------------------------|
| DNSREC \_ DELETE  | 0x00000004 | Eliminar un RR. Se usa junto con DNSREC \_ UPDATE       |
| DNSREC \_ NOEXIST | 0x00000004 | RR no existe. Se usa junto con DNSREC \_ PREREQ |



 

## <a name="dns-query-options"></a>Opciones de consulta DNS



| Constante                                | Value      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ESTÁNDAR \_ DE CONSULTA \_ DNS                    | 0x00000000 | Consulta estándar.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| RESPUESTA \_ TRUNCADA \_ DE \_ ACEPTACIÓN DE CONSULTAS \_ DNS | 0x00000001 | Devuelve resultados truncados. No vuelve a intentarlo en TCP.                                                                                                                                                                                                                                                                                                                                                                                                   |
| CONSULTA \_ DNS USE SOLO \_ \_ TCP \_              | 0x00000002 | Usa TCP solo para la consulta.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CONSULTA \_ DNS \_ SIN \_ RECURSIVIDAD               | 0x00000004 | Dirige al servidor DNS para que realice una consulta iterativa (en concreto, dirige al servidor DNS a no realizar una resolución recursiva para resolver la consulta).                                                                                                                                                                                                                                                                                                   |
| CACHÉ \_ DE \_ OMISIÓN DE CONSULTAS \_ DNS               | 0x00000008 | Omite la caché [*de resolución*](r-gly.md) en la búsqueda.                                                                                                                                                                                                                                                                                                                                                                            |
| CONSULTA DNS \_ \_ SIN CONSULTA DE \_ \_ CONEXIÓN             | 0x00000010 | Dirige a DNS para que realice una consulta solo en la memoria caché local. **Windows 2000 Server y Windows 2000 Professional:** Este valor no se admite. Para una funcionalidad similar, use **DNS \_ QUERY CACHE \_ \_ ONLY**.<br/>                                                                                                                                                                                                                                      |
| CONSULTA \_ DNS SIN NOMBRE \_ \_ \_ LOCAL             | 0x00000020 | Dirige a DNS para omitir el nombre local. **Windows 2000 Server y Windows 2000 Professional:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                    |
| CONSULTA DNS \_ \_ SIN ARCHIVO DE \_ \_ HOSTS             | 0x00000040 | Impide que la consulta DNS consulte el archivo HOSTS. **Windows 2000 Server y Windows 2000 Professional:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                   |
| CONSULTA \_ DNS \_ NO \_ NETBT                   | 0x00000080 | Impide que la consulta DNS use NetBT para la resolución. **Windows 2000 Server y Windows 2000 Professional:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                  |
| SOLO \_ CONEXIÓN DE CONSULTA \_ \_ DNS                  | 0x00000100 | Dirige a DNS para que realice una consulta solo mediante la red, omitiendo la información local. **Windows 2000 Server y Windows 2000 Professional:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                      |
| MENSAJE DE \_ DEVOLUCIÓN \_ DE CONSULTA \_ DNS             | 0x00000200 | Indica a DNS que devuelva el mensaje de respuesta DNS completo. **Windows 2000 Server y Windows 2000 Professional:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                   |
| SOLO \_ \_ MULTIDIFUSIÓN DE CONSULTAS \_ DNS             | 0x00000400 | Impide que la consulta use DNS y solo usa resolución de nombres de multidifusión de vínculos locales (LLMNR). **Windows Vista y Windows Server 2008 o posterior.** Se admite este valor.<br/>                                                                                                                                                                                                                                                                  |
| CONSULTA DNS \_ \_ SIN \_ MULTIDIFUSIÓN               | 0x00000800 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CONSULTA \_ DNS TRATAR COMO \_ \_ \_ FQDN             | 0x00001000 | Impide que la respuesta DNS adjunte sufijos al nombre enviado en un proceso de resolución de nombres.                                                                                                                                                                                                                                                                                                                                                  |
| DNS \_ QUERY \_ ADDRCONFIG                  | 0x00002000 | Windows 7: no envíe consultas de tipo [**A**](/windows/win32/api/windns/ns-windns-dns_a_data) si las direcciones IPv4 no están disponibles en una interfaz y no envían consultas de tipo [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) si las direcciones IPv6 no están disponibles.                                                                                                                                                                                                                                   |
| DNS \_ QUERY \_ DUAL \_ ADDR                  | 0x00004000 | Windows solo 7: consulte los registros de tipo [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) y [**A**](/windows/win32/api/windns/ns-windns-dns_a_data) y devuelva resultados para cada uno. Los resultados **de los** registros de tipo A se asignan al **tipo AAAA.**                                                                                                                                                                                                                                                           |
| ESPERA DE \_ \_ MULTIDIFUSIÓN DE CONSULTA \_ DNS             | 0x00020000 | Espera un tiempo de espera completo para recopilar todas las respuestas del vínculo local. Si no se establece, el comportamiento predeterminado es devolver con la primera respuesta. **Windows Vista y Windows Server 2008 o posterior.** Se admite este valor.<br/>                                                                                                                                                                                                              |
| COMPROBACIÓN DE \_ \_ MULTIDIFUSIÓN DE CONSULTA \_ DNS           | 0x00040000 | Dirige una prueba mediante el nombre de host del equipo local para comprobar la unidad de nombre en el mismo vínculo local. Recopila todas las respuestas incluso si el comportamiento normal del remitente de LLMNR no está habilitado. **Windows Vista y Windows Server 2008 o posterior.** Se admite este valor.<br/>                                                                                                                                                                                  |
| CONSULTA \_ DNS NO RESTABLECE VALORES DE \_ \_ \_ \_ TTL    | 0x00100000 | Si se establece, y si la respuesta contiene varios registros, los registros se almacenan con el TTL correspondiente al TTL de valor mínimo de entre todos los registros. Cuando se establece esta opción, "No cambiar el TTL de los registros individuales" en el conjunto de registros devuelto no se modifica.                                                                                                                                                                               |
| DESHABILITACIÓN \_ DE \_ LA \_ CODIFICACIÓN IDN DE LA CONSULTA \_ DNS      | 0x00200000 | Deshabilita la compatibilidad con codificación de nombre de dominio internacional (IDN) en las API [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a), [**DnsQueryEx,**](/windows/desktop/api/Windns/nf-windns-dnsqueryex) [**DnsModifyRecordsInSet**](/windows/desktop/api/Windns/nf-windns-dnsmodifyrecordsinset_a)y [**DnsReplaceRecordSet.**](/windows/desktop/api/Windns/nf-windns-dnsreplacerecordseta) Todos los nombres de código punycode se tratan como ASCII y se codificarán en ASCII en la conexión. Todos los nombres no ASCII se codifican en UTF8 en la conexión. **Windows 8 o posterior:** Se admite este valor.<br/> |
| DNS \_ QUERY \_ APPEND \_ MULTILABEL          | 0x00800000 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CONSULTA \_ DNS \_ RESERVADA                    | 0xf0000000 | Reservado.                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="dns-update-options"></a>Opciones de actualización de DNS



| Constante                                 | Value      | Significado                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DNS \_ UPDATE \_ SECURITY \_ USE \_ DEFAULT      | 0x00000000 | Usa el comportamiento predeterminado, que se especifica en el Registro, para las actualizaciones de DNS dinámicas seguras.                                                                |
| DNS \_ UPDATE \_ SECURITY \_ OFF               | 0x00000010 | No intenta proteger las actualizaciones dinámicas.                                                                                                                      |
| DNS \_ UPDATE \_ SECURITY \_ ON                | 0x00000020 | Intenta una actualización dinámica no segura; si se rechaza, intenta proteger la actualización dinámica.                                                                               |
| SOLO \_ SEGURIDAD DE ACTUALIZACIÓN DE \_ \_ DNS              | 0x00000100 | Solo intenta proteger las actualizaciones dinámicas.                                                                                                                         |
| CONTEXTO \_ DE SEGURIDAD DE LA CACHÉ DE ACTUALIZACIÓN \_ \_ \_ DE DNS    | 0x00000200 | Almacena en caché el contexto de seguridad para su uso en transacciones futuras.                                                                                                   |
| PRUEBA DE ACTUALIZACIÓN DE DNS \_ \_ USE EL \_ \_ \_ \_ ACCT DE SYS LOCAL | 0x00000400 | Usa las credenciales de la cuenta de equipo local.                                                                                                               |
| DNS \_ UPDATE \_ FORCE \_ SECURITY \_ NEGO       | 0x00000800 | No usa el contexto de seguridad almacenado en caché.                                                                                                                         |
| ACTUALIZACIÓN DE DNS \_ PRUEBE TODOS LOS SERVIDORES \_ \_ \_ \_ MAESTROS   | 0x00001000 | Envía actualizaciones de DNS a todos los servidores DNS de varios maestros.                                                                                                            |
| ADAPTADORES \_ DNS UPDATE SKIP NO \_ \_ \_ \_ UPDATE  | 0x00002000 | No actualice los adaptadores en los que las actualizaciones de DNS dinámicas estén deshabilitadas. **Windows 2000 Server con SP2 o posterior:** Se admite este valor.<br/>                 |
| SERVIDOR \_ REMOTO DE ACTUALIZACIÓN DE \_ \_ DNS              | 0x00004000 | Registre registros CNAME en un servidor remoto además del servidor DNS local. **Windows 2000 Server con SP2 o posterior:** Se admite este valor.<br/> |
| ACTUALIZACIÓN \_ RESERVADA DE \_ DNS                    | 0xffff0000 | Reservado para uso futuro.                                                                                                                                      |



 

## <a name="dns-response-codes"></a>Códigos de respuesta DNS



| Error                | Significado                                        |
|----------------------|------------------------------------------------|
| DNS \_ RCODE \_ NOERROR  | Sin errores                                       |
| DNS \_ RCODE \_ FORMERR  | Error de formato                                   |
| DNS \_ RCODE \_ SERVFAIL | Error del servidor                                 |
| DNS \_ RCODE \_ NXDOMAIN | Error de nombre                                     |
| DNS \_ RCODE \_ NOTIMPL  | No implementado                                |
| DNS \_ RCODE \_ RECHAZADO  | Conexión rechazada                             |
| DNS \_ RCODE \_ YXDOMAIN | El nombre de dominio no debe existir                   |
| DNS \_ RCODE \_ YXRRSET  | El conjunto de registros de recursos (RR) no debe existir      |
| DNS \_ RCODE \_ NXRRSET  | El conjunto RR no existe                          |
| DNS \_ RCODE \_ NOTAUTH  | No autoritativo para la zona                     |
| DNS \_ RCODE \_ NOTZONE  | Nombre no en zona                               |
| DNS \_ RCODE \_ BADVERS  | Versión del mecanismo de extensión no adecuado para DNS (EDNS) |
| DNS \_ RCODE \_ BADSIG   | Firma no válida                                  |
| CLAVE \_ BADKEY de RCODE DE DNS \_   | Clave no buena                                        |
| DNS \_ RCODE \_ BADTIME  | Marca de tiempo no válida                                  |



 

 

 





