---
title: Funciones SNMP
description: En este tema se describen tres agrupaciones de funciones SNMP y se enumeran las funciones que se incluyen en cada grupo.
ms.assetid: 8913caa9-6b2c-424c-a778-bd54d6584dac
keywords:
- Funciones SNMP SNMP
- Funciones SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f4cc98ce84fbb66f8beb59a6bf995dc4315159
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488150"
---
# <a name="snmp-functions"></a>Funciones SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

En este tema se describen tres agrupaciones de funciones SNMP y se enumeran las funciones que se incluyen en cada grupo:

-   [Funciones de API del agente de extensión SNMP](#snmp-extension-agent-api-functions)
-   [Funciones de la API de administración de SNMP](#snmp-management-api-functions)
-   [Funciones de la API de la utilidad SNMP](#snmp-utility-api-functions)

## <a name="snmp-extension-agent-api-functions"></a>Funciones de API del agente de extensión SNMP

Las funciones del agente de extensión SNMP definen la interfaz entre el servicio SNMP y los archivos DLL del agente de extensión SNMP de terceros. En la tabla siguiente se enumeran las funciones que las aplicaciones pueden utilizar para resolver los enlaces de variables especificados por las unidades de datos del protocolo SNMP (PDU) de entrada.

| Función de API del agente de extensión SNMP                    | Descripción                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**SnmpExtensionClose**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionclose)     | Solicita que el agente de extensión SNMP Desasigne recursos y finalice las operaciones.                                    |
| [**SnmpExtensionInit**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninit)       | Inicializa la DLL del agente de extensión SNMP.                                                                                |
| [**SnmpExtensionInitEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninitex)   | Identifica los subárboles de la base de datos de información de administración (MIB) adicionales que admite el agente de extensión SNMP.             |
| [**SnmpExtensionMonitor**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionmonitor) | Proporciona al agente de extensión SNMP información sobre los contadores internos y los parámetros del servicio.            |
| [**SnmpExtensionQuery**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionquery)     | Resuelve solicitudes SNMP que contienen variables en uno o varios de los subárboles MIB registrados del agente de extensión SNMP. |
| [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) | Procesa solicitudes SNMP que especifican variables en uno o más subárboles MIB registrados por agentes de extensión SNMP. |
| [**SnmpExtensionTrap**](/windows/desktop/api/Snmp/nf-snmp-snmpextensiontrap)       | Recupera información necesaria para que el servicio genere capturas para el agente de extensión SNMP.                          |



 

## <a name="snmp-management-api-functions"></a>Funciones de la API de administración de SNMP

Las funciones de administración de SNMP definen la interfaz entre las aplicaciones de administrador SNMP de terceros y la biblioteca de vínculos dinámicos (DLL) de la función de administración Mgmtapi.dll. La DLL funciona junto con el servicio de captura de SNMP (Snmptrap.exe) y puede interactuar con una o más aplicaciones de administrador SNMP de terceros. En la tabla siguiente se enumeran las funciones de administración que usan las aplicaciones de administrador de terceros para realizar operaciones del administrador SNMP.

| Función de API de administración de SNMP                   | Descripción                                                                                                                                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpMgrClose**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrclose)           | Cierra los sockets de comunicaciones y las estructuras de datos que están asociados a la sesión especificada.                                                                                                  |
| [**SnmpMgrCtl**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrctl)               | Establece un parámetro operativo que está asociado a una sesión SNMP.                                                                                                                                   |
| [**SnmpMgrGetTrap**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrap)       | Devuelve los datos de captura pendientes que el autor de la llamada no ha recibido si está habilitada la recepción de capturas.                                                                                                           |
| [**SnmpMgrGetTrapEx**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrapex)   | Devuelve los datos de captura pendientes que el autor de la llamada no ha recibido si está habilitada la recepción de capturas. También devuelve la dirección del origen de transporte y la captura de la comunidad que está asociada a la captura. |
| [**SnmpMgrOidToStr**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgroidtostr)     | Convierte una estructura de identificador de objeto interno en su representación de cadena.                                                                                                                         |
| [**SnmpMgrOpen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgropen)             | Inicializa sockets de comunicaciones y estructuras de datos que son necesarios para establecer la comunicación con el agente SNMP.                                                                               |
| [**SnmpMgrRequest**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrrequest)       | Solicita que el agente especificado realice la operación especificada.                                                                                                                             |
| [**SnmpMgrStrToOid**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrstrtooid)     | Convierte el formato de cadena de un identificador de objeto en su estructura interna de identificador de objeto.                                                                                                        |
| [**SnmpMgrTrapListen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrtraplisten) | Registra la capacidad de una aplicación de administrador SNMP de recibir capturas SNMP del servicio de captura SNMP.                                                                                                 |



 

## <a name="snmp-utility-api-functions"></a>Funciones de la API de la utilidad SNMP

Las funciones de la utilidad SNMP proporcionan funciones útiles durante el desarrollo de aplicaciones SNMP, incluida la simplificación de la manipulación de estructuras de datos SNMP. En la tabla siguiente se enumeran las funciones de la utilidad SNMP.

| Función de API de la utilidad SNMP                                  | Descripción                                                                                                                                                        |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpSvcGetUptime**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcgetuptime)               | Recupera la hora, en centiseconds, para la que se ha estado ejecutando el servicio SNMP.                                                                                  |
| [**SnmpSvcSetLogLevel**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetloglevel)           | Ajusta el nivel de detalle de la salida de depuración del servicio SNMP y de los agentes de extensión SNMP.                                                              |
| [**SnmpSvcSetLogType**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetlogtype)             | Ajusta el destino de la salida de depuración del servicio SNMP y de los agentes de extensión SNMP.                                                                 |
| [**SnmpUtilAsnAnyCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanycpy)             | Copia una estructura de [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) de origen en una estructura de **AsnAny** de destino.                                                                      |
| [**SnmpUtilAsnAnyFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanyfree)           | Libera la memoria asignada para una estructura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) especificada.                                                                        |
| [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)               | Establece el nivel de información de depuración que se va a recibir del servicio SNMP o de una llamada a [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint).                       |
| [**SnmpUtilIdsToA**](/windows/desktop/api/Snmp/nf-snmp-snmputilidstoa)                   | Convierte un identificador de objeto (OID) en una cadena terminada en NULL.                                                                                                   |
| [**SnmpUtilMemAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemalloc)               | Asigna memoria dinámica del montón del proceso.                                                                                                                    |
| [**SnmpUtilMemFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemfree)                 | Libera el objeto de memoria especificado.                                                                                                                                 |
| [**SnmpUtilMemReAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemrealloc)           | Cambia el tamaño del objeto de memoria especificado.                                                                                                                   |
| [**SnmpUtilOctetsCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscmp)             | Compara dos cadenas de octeto.                                                                                                                                        |
| [**SnmpUtilOctetsCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscpy)             | Copia una estructura de [**AsnOctetString**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring) de origen en una estructura de **AsnOctetString** de destino.                                              |
| [**SnmpUtilOctetsFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsfree)           | Libera la memoria asignada para la cadena de octeto especificada.                                                                                                |
| [**SnmpUtilOctetsNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsncmp)           | Realiza una comparación de dos cadenas de octeto con el número especificado de subidentificadors.                                                                              |
| [**SnmpUtilOidAppend**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidappend)             | Anexa un identificador de objeto de origen, contenido en una estructura [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) , a un identificador de objeto de destino.          |
| [**SnmpUtilOidCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcmp)                   | Compara dos identificadores de objeto contenidos en estructuras [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) .                                           |
| [**SnmpUtilOidCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcpy)                   | Copia una estructura de [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) de origen en una estructura de **AsnObjectIdentifier** de destino.                               |
| [**SnmpUtilOidFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidfree)                 | Libera la memoria asignada para el identificador de objeto especificado.                                                                                           |
| [**SnmpUtilOidNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidncmp)                 | Compara dos identificadores de objeto contenidos en estructuras [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) con el número especificado de subidentificadors. |
| [**SnmpUtilOidToA**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidtoa)                   | Convierte un identificador de objeto (OID) en una cadena terminada en NULL.                                                                                                   |
| [**SnmpUtilPrintAsnAny**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintasnany)         | Imprime un valor contenido en una estructura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) con fines de depuración y desarrollo.                                              |
| [**SnmpUtilPrintOid**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintoid)               | Da formato al identificador de objeto (OID) especificado e imprime el resultado en el dispositivo de salida estándar.                                                                 |
| [**SnmpUtilVarBindCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindcpy)           | Copia una estructura de [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) de origen en una estructura de **SnmpVarBind** de destino.                                                       |
| [**SnmpUtilVarBindListCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistcpy)   | Copia una estructura de [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) de origen en una estructura de **SnmpVarBindList** de destino.                                           |
| [**SnmpUtilVarBindFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindfree)         | Libera la memoria asignada para la estructura [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) especificada.                                                            |
| [**SnmpUtilVarBindListFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistfree) | Libera la memoria asignada para la estructura [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) especificada.                                                    |



 

 

 