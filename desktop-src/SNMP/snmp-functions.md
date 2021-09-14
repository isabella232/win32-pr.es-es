---
title: Funciones SNMP
description: En este tema se describen tres agrupaciones de funciones SNMP y se enumeran las funciones que se incluyen en cada grupo.
ms.assetid: 8913caa9-6b2c-424c-a778-bd54d6584dac
keywords:
- SNMP Functions SNMP
- Funciones SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f4cc98ce84fbb66f8beb59a6bf995dc4315159
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244382"
---
# <a name="snmp-functions"></a>Funciones SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

En este tema se describen tres agrupaciones de funciones SNMP y se enumeran las funciones que se incluyen en cada grupo:

-   [Funciones de LA API del agente de extensión SNMP](#snmp-extension-agent-api-functions)
-   [Funciones de API de Administración SNMP](#snmp-management-api-functions)
-   [Funciones de la API de la utilidad SNMP](#snmp-utility-api-functions)

## <a name="snmp-extension-agent-api-functions"></a>Funciones de LA API del agente de extensión SNMP

Las funciones del agente de extensión SNMP definen la interfaz entre el servicio SNMP y los archivos DLL del agente de extensión SNMP de terceros. En la tabla siguiente se enumeran las funciones que las aplicaciones pueden usar para resolver los enlaces de variables especificados por las unidades de datos (PDU) del protocolo SNMP entrantes.

| Función de API del agente de extensión SNMP                    | Descripción                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**SnmpExtensionClose**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionclose)     | Solicita que el agente de extensión SNMP desasigne los recursos y finalice las operaciones.                                    |
| [**SnmpExtensionInit**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninit)       | Inicializa el archivo DLL del agente de extensión SNMP.                                                                                |
| [**SnmpExtensionInitEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninitex)   | Identifica los subárboles adicionales de la base de información de administración (MIB) que admite el agente de extensión SNMP.             |
| [**SnmpExtensionMonitor**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionmonitor) | Proporciona al agente de extensión SNMP información sobre los contadores internos y los parámetros del servicio.            |
| [**SnmpExtensionQuery**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionquery)     | Resuelve las solicitudes SNMP que contienen variables en uno o varios de los subárboles MIB registrados del agente de extensión SNMP. |
| [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) | Procesa solicitudes SNMP que especifican variables en uno o varios subárboles MIB registrados por agentes de extensión SNMP. |
| [**SnmpExtensionTrap**](/windows/desktop/api/Snmp/nf-snmp-snmpextensiontrap)       | Recupera la información que el servicio requiere para generar capturas para el agente de extensión SNMP.                          |



 

## <a name="snmp-management-api-functions"></a>Funciones de API de Administración SNMP

Las funciones de administración de SNMP definen la interfaz entre las aplicaciones de administrador SNMP de terceros y la biblioteca de vínculos dinámicos (DLL) de la función de administración Mgmtapi.dll. El archivo DLL funciona junto con el servicio de captura de SNMP (Snmptrap.exe) y puede interactuar con una o varias aplicaciones de administrador SNMP de terceros. En la tabla siguiente se enumeran las funciones de administración que las aplicaciones de administrador de terceros usan para realizar operaciones de snmp manager.

| Función API de Administración SNMP                   | Descripción                                                                                                                                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpMgrClose**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrclose)           | Cierra los sockets de comunicaciones y las estructuras de datos asociadas a la sesión especificada.                                                                                                  |
| [**SnmpMgrCtl**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrctl)               | Establece un parámetro operativo asociado a una sesión SNMP.                                                                                                                                   |
| [**SnmpMgrGetTrap**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrap)       | Devuelve los datos de captura pendientes que el autor de la llamada no ha recibido si está habilitada la recepción de capturas.                                                                                                           |
| [**SnmpMgrGetTrapEx**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrapex)   | Devuelve los datos de captura pendientes que el autor de la llamada no ha recibido si está habilitada la recepción de capturas. También devuelve la dirección del origen de transporte y la captura de la comunidad que está asociada a la captura. |
| [**SnmpMgrOidToStr**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgroidtostr)     | Convierte una estructura de identificador de objeto interno en su representación de cadena.                                                                                                                         |
| [**SnmpMgrOpen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgropen)             | Inicializa los sockets de comunicaciones y las estructuras de datos necesarias para establecer la comunicación con el agente SNMP.                                                                               |
| [**SnmpMgrRequest**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrrequest)       | Solicita que el agente especificado realice la operación especificada.                                                                                                                             |
| [**SnmpMgrStrToOid**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrstrtooid)     | Convierte el formato de cadena de un identificador de objeto en su estructura de identificador de objeto interna.                                                                                                        |
| [**SnmpMgrTrapListen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrtraplisten) | Registra la capacidad de una aplicación de administrador SNMP de recibir capturas SNMP del servicio de captura de SNMP.                                                                                                 |



 

## <a name="snmp-utility-api-functions"></a>Funciones de la API de la utilidad SNMP

Las funciones de utilidad SNMP proporcionan funcionalidades que son útiles durante el desarrollo de aplicaciones SNMP, incluida la simplificación de la manipulación de estructuras de datos SNMP. En la tabla siguiente se enumeran las funciones de la utilidad SNMP.

| Función de LA API de la utilidad SNMP                                  | Descripción                                                                                                                                                        |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpSvcGetUptime**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcgetuptime)               | Recupera el tiempo, en centisegundos, durante el que se ha estado ejecutando el servicio SNMP.                                                                                  |
| [**SnmpSvcSetLogLevel**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetloglevel)           | Ajusta el nivel de detalle de la salida de depuración del servicio SNMP y de los agentes de extensión SNMP.                                                              |
| [**SnmpSvcSetLogType**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetlogtype)             | Ajusta el destino de la salida de depuración del servicio SNMP y de los agentes de extensión SNMP.                                                                 |
| [**SnmpUtilAsnAnyCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanycpy)             | Copia una estructura [**AsnAny de**](/windows/desktop/api/Snmp/ns-snmp-asnany) origen en una estructura **AsnAny de** destino.                                                                      |
| [**SnmpUtilAsnAnyFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanyfree)           | Libera la memoria que se asignó para una estructura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) especificada.                                                                        |
| [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)               | Establece el nivel de información de depuración que se va a recibir desde el servicio SNMP o desde una llamada a [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint).                       |
| [**SnmpUtilIdsToA**](/windows/desktop/api/Snmp/nf-snmp-snmputilidstoa)                   | Convierte un identificador de objeto (OID) en una cadena terminada en NULL.                                                                                                   |
| [**SnmpUtilMemAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemalloc)               | Asigna memoria dinámica desde el montón de procesos.                                                                                                                    |
| [**SnmpUtilMemFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemfree)                 | Libera el objeto de memoria especificado.                                                                                                                                 |
| [**SnmpUtilMemReAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemrealloc)           | Cambia el tamaño del objeto de memoria especificado.                                                                                                                   |
| [**SnmpUtilOctetsCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscmp)             | Compara dos cadenas de octeto.                                                                                                                                        |
| [**SnmpUtilOctetsCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscpy)             | Copia una estructura [**AsnOctetString de**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring) origen en una estructura **AsnOctetString de** destino.                                              |
| [**SnmpUtilOctetsFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsfree)           | Libera la memoria que se asignó para la cadena de octeto especificada.                                                                                                |
| [**SnmpUtilOctetsNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsncmp)           | Realiza una comparación de dos cadenas de octetos con el número especificado de subidentificadores.                                                                              |
| [**SnmpUtilOidAppend**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidappend)             | Anexa un identificador de objeto de origen, incluido en una [**estructura AsnObjectIdentifier,**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) a un identificador de objeto de destino.          |
| [**SnmpUtilOidCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcmp)                   | Compara dos identificadores de objeto contenidos en estructuras [**AsnObjectIdentifier.**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier)                                           |
| [**SnmpUtilOidCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcpy)                   | Copia una estructura [**AsnObjectIdentifier de origen**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) en una estructura **AsnObjectIdentifier de** destino.                               |
| [**SnmpUtilOidFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidfree)                 | Libera la memoria que se asignó para el identificador de objeto especificado.                                                                                           |
| [**SnmpUtilOidNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidncmp)                 | Compara dos identificadores de objeto contenidos en estructuras [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) con el número especificado de subidentificadores. |
| [**SnmpUtilOidToA**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidtoa)                   | Convierte un identificador de objeto (OID) en una cadena terminada en NULL.                                                                                                   |
| [**SnmpUtilPrintAsnAny**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintasnany)         | Imprime un valor contenido en una estructura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) con fines de depuración y desarrollo.                                              |
| [**SnmpUtilPrintOid**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintoid)               | Da formato al identificador de objeto (OID) especificado e imprime el resultado en el dispositivo de salida estándar.                                                                 |
| [**SnmpUtilVarBindCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindcpy)           | Copia una estructura [**SnmpVarBind de**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) origen en una **estructura SnmpVarBind de** destino.                                                       |
| [**SnmpUtilVarBindListCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistcpy)   | Copia una estructura [**SnmpVarBindList de**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) origen en una **estructura SnmpVarBindList de** destino.                                           |
| [**SnmpUtilVarBindFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindfree)         | Libera la memoria que se asignó para la estructura [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) especificada.                                                            |
| [**SnmpUtilVarBindListFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistfree) | Libera la memoria que se asignó para la estructura [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) especificada.                                                    |



 

 

 