---
description: Indica el motivo por el que se ha dado error en una operación WLAN.
ms.assetid: 7b267f0b-b3f7-4729-bab4-de3bdd0a35a2
title: WLAN_REASON_CODE (Wlanapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f24b0ab902610408eb7b80b4a962fcc81d4598244714b8f30f0ebf350a7e628
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064565"
---
# <a name="wlan_reason_code"></a>CÓDIGO DE MOTIVO DE WLAN \_ \_

El **tipo DE CÓDIGO DE MOTIVO \_ \_ DE WLAN** indica el motivo por el que se ha generado un error en una operación WLAN.

Puede usar la función [**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring) para asignar un código de motivo numérico (por ejemplo, 0x00050007) a su significado de texto. También puede usar la tabla de búsqueda para ayudar a interpretar el valor numérico del código de motivo. Para ver la tabla de búsqueda, vea Apéndice E: Asignación de códigos de motivo a mensajes de eventos en el documento Solución de problemas Windows conexiones inalámbricas de [Vista 802.11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10)).


```C++
typedef DWORD WLAN_REASON_CODE, *PWLAN_REASON_CODE;
```



En la tabla siguiente se enumeran los códigos de error generales.



| Código del motivo                 | Significado                            |
|-----------------------------|------------------------------------|
| ÉXITO DEL \_ CÓDIGO DE \_ MOTIVO DE WLAN \_ | La operación se realiza correctamente.            |
| CÓDIGO DESCONOCIDO \_ DE MOTIVO \_ DE WLAN \_ | Se desconoce el motivo del error. |



 

En la tabla siguiente se enumeran los códigos de error de configuración automática.



| Código de motivo                                  | Significado                                         |
|----------------------------------------------|-------------------------------------------------|
| RED DE CÓDIGO DE MOTIVO DE WLAN \_ \_ NO \_ \_ \_ COMPATIBLE | La red inalámbrica no es compatible.         |
| PERFIL DE CÓDIGO DE MOTIVO DE WLAN \_ \_ NO \_ \_ \_ COMPATIBLE | El perfil de red inalámbrica no es compatible. |



 

En la tabla siguiente se enumeran los códigos de error de conexión automática.



| Código de motivo                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CÓDIGO DE \_ MOTIVO DE WLAN SIN CONEXIÓN \_ \_ \_ \_ AUTOMÁTICA                   | El perfil no especifica ninguna conexión automática.                                                                                                                                                                                                                                                                                                                                                                                                               |
| CÓDIGO DE \_ MOTIVO DE WLAN NO \_ \_ \_ VISIBLE                           | La red inalámbrica no está visible.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SE \_ DENEGÓ \_ EL CÓDIGO DE MOTIVO DE \_ WLAN. \_                             | La directiva de grupo bloquea la red inalámbrica.                                                                                                                                                                                                                                                                                                                                                                                                        |
| EL USUARIO \_ HA \_ DENEGADO EL CÓDIGO \_ DE MOTIVO DE \_ WLAN                           | El usuario bloquea la red inalámbrica.                                                                                                                                                                                                                                                                                                                                                                                                            |
| NO SE \_ \_ PERMITE EL TIPO \_ BSS \_ DEL CÓDIGO DE MOTIVO \_ DE \_ WLAN                | No se permite el tipo de conjunto de servicios básico (BSS) en este adaptador inalámbrico.                                                                                                                                                                                                                                                                                                                                                                               |
| CÓDIGO DE MOTIVO DE WLAN \_ EN LA LISTA DE \_ \_ \_ \_ ERRORES                       | La red inalámbrica está en la lista de errores.                                                                                                                                                                                                                                                                                                                                                                                                             |
| CÓDIGO DE MOTIVO DE WLAN \_ EN LA LISTA DE \_ \_ \_ \_ BLOQUEADOS                      | La red inalámbrica está en la lista de bloqueados.                                                                                                                                                                                                                                                                                                                                                                                                            |
| LISTA \_ DE \_ \_ SSID DE CÓDIGO DE MOTIVO \_ DE \_ \_ WLAN DEMASIADO LARGA                  | El tamaño de la lista de identificadores de conjunto de servicios (SSID) supera el tamaño máximo admitido por el adaptador.                                                                                                                                                                                                                                                                                                                                                  |
| ERROR EN \_ LA LLAMADA DE CONEXIÓN DEL CÓDIGO DE MOTIVO \_ \_ \_ DE \_ WLAN                    | Se produce un error en la llamada de conexión del módulo específico de medios (MSM).                                                                                                                                                                                                                                                                                                                                                                                                     |
| ERROR EN \_ LA LLAMADA DE EXAMEN DE CÓDIGO DE MOTIVO \_ \_ \_ DE \_ WLAN                       | Se produce un error en la llamada de examen de MSM.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| RED DE CÓDIGO DE MOTIVO DE WLAN \_ \_ NO \_ \_ \_ DISPONIBLE                | La red especificada no está disponible. Este código de motivo también se usa cuando hay una discrepancia entre las funcionalidades especificadas en un perfil XML y las funcionalidades de interfaz o red. Por ejemplo, si un perfil especifica el uso de WPA2 cuando la NIC solo admite WPA, se devuelve este código de error. Además, si un perfil especifica el uso del modo FIPS cuando la NIC no admite el modo FIPS, se devuelve este código de error.<br/> |
| PERFIL DE CÓDIGO DE MOTIVO DE WLAN \_ \_ CAMBIADO O \_ \_ \_ \_ ELIMINADO          | El perfil se cambió o eliminó antes de establecer la conexión.                                                                                                                                                                                                                                                                                                                                                                               |
| ERROR DE \_ COINCIDENCIA DE CLAVE DE CÓDIGO DE MOTIVO \_ \_ \_ DE WLAN                          | La clave de perfil no coincide con la clave de red.                                                                                                                                                                                                                                                                                                                                                                                                         |
| EL USUARIO DEL CÓDIGO DE MOTIVO DE WLAN \_ \_ NO \_ \_ \_ RESPONDE                     | El usuario no responde.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| PERFIL DE AP DE CÓDIGO DE MOTIVO DE WLAN \_ NO PERMITIDO PARA EL \_ \_ \_ \_ \_ \_ \_ CLIENTE | Una aplicación intentó aplicar un perfil de red hospedada inalámbrica a un adaptador de red inalámbrica físico mediante la [**función WlanSetProfile,**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) en lugar de a un dispositivo virtual.                                                                                                                                                                                                                                                    |
| PERFIL DE AP DE CÓDIGO DE MOTIVO DE WLAN \_ \_ NO \_ \_ \_ \_ PERMITIDO              | Una aplicación intentó aplicar un perfil de red hospedada inalámbrica a un adaptador de red inalámbrica físico mediante la [**función WlanSetProfile,**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) en lugar de a un dispositivo virtual.                                                                                                                                                                                                                                                    |



 

En la tabla siguiente se enumeran los códigos de error de validación de perfiles.



| Código de motivo                                                    | Significado                                                                                                                                                                                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ESQUEMA DE \_ PERFIL NO VÁLIDO DEL CÓDIGO DE MOTIVO \_ \_ \_ DE \_ WLAN                   | El perfil no es válido según el esquema.                                                                                                                                                                                                  |
| FALTA EL \_ PERFIL DE CÓDIGO DE MOTIVO \_ \_ DE \_ WLAN                           | Falta el elemento WLANProfile.                                                                                                                                                                                                           |
| NOMBRE DE \_ PERFIL NO VÁLIDO DEL CÓDIGO DE MOTIVO \_ \_ \_ DE \_ WLAN                     | El nombre del perfil no es válido.                                                                                                                                                                                                           |
| TIPO DE \_ PERFIL NO VÁLIDO DEL CÓDIGO DE MOTIVO \_ \_ \_ DE \_ WLAN                     | El tipo del perfil no es válido.                                                                                                                                                                                                           |
| TIPO \_ \_ \_ PHY NO VÁLIDO DEL \_ CÓDIGO DE MOTIVO DE \_ WLAN                         | El tipo PHY no es válido.                                                                                                                                                                                                                      |
| FALTA SEGURIDAD \_ \_ DE \_ MSM \_ \_ DEL CÓDIGO DE MOTIVO DE WLAN                     | Falta la configuración de seguridad de MSM.                                                                                                                                                                                                        |
| NO SE \_ ADMITE LA SEGURIDAD DE \_ \_ IHV DEL CÓDIGO \_ DE MOTIVO \_ DE \_ WLAN              | Falta la configuración de seguridad del proveedor de hardware independiente (IHV).                                                                                                                                                                          |
| ERROR DE COINCIDENCIA DEL CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ \_ IHV OUI \_                         | La OUI del perfil de IHV no coincide con la OUI del adaptador.                                                                                                                                                                                       |
| FALTA EL CÓDIGO DE RAZÓN DE WLAN \_ \_ \_ \_ IHV OUI \_                          | Falta la configuración de IHV OUI.                                                                                                                                                                                                             |
| FALTA LA \_ CONFIGURACIÓN \_ DE \_ IHV DEL CÓDIGO DE \_ MOTIVO DE \_ WLAN                     | Falta la configuración de seguridad de IHV.                                                                                                                                                                                                        |
| NO SE \_ ADMITE LA CONECTIVIDAD DE \_ \_ IHV DEL CÓDIGO \_ DE MOTIVO \_ DE \_ WLAN          | Una aplicación intentó aplicar un perfil de IHV en un adaptador que no admite la configuración de conectividad de IHV.                                                                                                                                   |
| SEGURIDAD DE \_ CONFLICTOS \_ DE CÓDIGO DE \_ MOTIVO DE \_ WLAN                         | Conflicto de configuración de seguridad.                                                                                                                                                                                                               |
| FALTA SEGURIDAD \_ DEL CÓDIGO DE MOTIVO \_ \_ DE \_ WLAN                          | Falta la configuración de seguridad.                                                                                                                                                                                                            |
| CÓDIGO DE \_ MOTIVO DE WLAN TIPO \_ \_ \_ BSS \_ NO VÁLIDO                         | El tipo BSS no es válido.                                                                                                                                                                                                                    |
| CÓDIGO DE \_ MOTIVO DE WLAN MODO DE CONEXIÓN \_ \_ \_ ADDHOC \_ NO \_ VÁLIDO           | No se puede establecer la conexión automática para una red ad hoc.                                                                                                                                                                                     |
| CÓDIGO DE MOTIVO DE WLAN QUE NO ES UN CONJUNTO \_ \_ DE \_ \_ \_ \_ \_ DIFUSIÓN PARA ADHOC            | No se puede establecer la no difusión para una red ad hoc.                                                                                                                                                                                            |
| CAMBIO AUTOMÁTICO DEL CÓDIGO DE MOTIVO DE WLAN \_ \_ ESTABLECIDO PARA \_ \_ \_ \_ \_ ADHOC              | No se puede establecer el conmutador automático para una red ad hoc.                                                                                                                                                                                              |
| CAMBIO AUTOMÁTICO DEL CÓDIGO DE MOTIVO DE WLAN \_ ESTABLECIDO PARA LA CONEXIÓN \_ \_ \_ \_ \_ \_ \_ MANUAL | No se puede establecer el modificador automático para un perfil de conexión manual.                                                                                                                                                                                    |
| FALTA EL CÓDIGO DE RAZÓN DE WLAN \_ \_ \_ \_ IHV SECURITY \_ ONEX \_               | Falta la configuración de seguridad de IHV 802.1X.                                                                                                                                                                                                 |
| SSID DE PERFIL DE CÓDIGO DE MOTIVO DE WLAN \_ \_ NO \_ \_ \_ VÁLIDO                     | El SSID del perfil no es válido o falta.                                                                                                                                                                                                |
| CÓDIGO DE \_ MOTIVO \_ DE WLAN \_ \_ \_ DEMASIADOS SSID                            | Se especificaron demasiados SSID en el perfil.                                                                                                                                                                                                 |
| NO SE \_ ADMITE LA CONECTIVIDAD DE \_ \_ IHV DEL CÓDIGO \_ DE MOTIVO \_ DE \_ WLAN          |                                                                                                                                                                                                                                               |
| CÓDIGO DE \_ MOTIVO DE WLAN NÚMERO MÁXIMO DE CLIENTES NO CORRECTO \_ PARA \_ \_ \_ \_ \_ \_ \_ AP     | Una aplicación intentó aplicar un perfil de red hospedada inalámbrica a una NIC del adaptador de red físico mediante la [**función WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) y especificó un valor inaceptable para el número máximo de clientes permitido. |
| CANAL DE CÓDIGO DE MOTIVO DE WLAN \_ \_ NO \_ \_ VÁLIDO                           | El canal especificado no es válido.                                                                                                                                                                                                             |
| NO SE \_ ADMITE EL MODO DE OPERACIÓN DE CÓDIGO DE MOTIVO \_ \_ \_ \_ DE \_ WLAN            |                                                                                                                                                                                                                                               |
| NO SE PERMITE EL PERFIL DE AP AUTOMÁTICO DE \_ \_ CÓDIGO DE MOTIVO \_ \_ \_ \_ DE \_ WLAN            | Error interno del sistema operativo con la red hospedada inalámbrica.                                                                                                                                                                 |
| NO SE \_ PERMITE LA CONEXIÓN AUTOMÁTICA DEL CÓDIGO DE MOTIVO \_ \_ \_ \_ DE \_ WLAN             |                                                                                                                                                                                                                                               |



 

En la tabla siguiente se enumeran los códigos de error de incompatibilidad de red de MSM.



| Código de motivo                                            | Significado                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| CÓDIGO DE MOTIVO DE WLAN \_ NO ADMITIDO ESTABLECIDO POR EL SISTEMA \_ \_ \_ \_ \_ \_ OPERATIVO | El sistema operativo no admite la configuración de seguridad. |
| CONJUNTO \_ DE SEGURIDAD NO COMPATIBLE CON EL CÓDIGO DE MOTIVO \_ \_ \_ DE \_ WLAN         | No se admite la configuración de seguridad.                         |
| WLAN \_ REASON \_ CODE \_ BSS \_ TYPE \_ UNMATCH                 | El tipo BSS no coincide.                                     |
| WLAN \_ REASON \_ CODE \_ PHY \_ TYPE \_ UNMATCH                 | El tipo PHY no coincide.                                     |
| WLAN \_ REASON \_ CODE \_ DATARATE \_ UNMATCH                  | La velocidad de datos no coincide.                                    |



 

En la tabla siguiente se enumeran los códigos de error de error de conexión de MSM.



| Código de motivo                                       | Significado                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| USUARIO DEL CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ \_ CANCELADO               | El usuario ha cancelado la operación.                                                                             |
| ERROR DE \_ ASOCIACIÓN \_ DE CÓDIGO DE \_ MOTIVO DE \_ WLAN          | Controlador desconectado durante la asociación.                                                                       |
| TIEMPO DE ESPERA \_ DE \_ ASOCIACIÓN DE \_ CÓDIGO DE MOTIVO \_ DE WLAN          | Se ha pasado el tiempo de espera de la asociación.                                                                                       |
| ERROR DE \_ SEGURIDAD PREVIA DEL CÓDIGO DE MOTIVO \_ \_ \_ DE \_ WLAN        | Error de seguridad previo a la asociación.                                                                            |
| ERROR DE \_ SEGURIDAD DE INICIO DEL CÓDIGO DE MOTIVO \_ \_ \_ DE \_ WLAN      | No se pudo iniciar la seguridad después de la asociación.                                                                  |
| ERROR DE \_ SEGURIDAD DEL CÓDIGO DE MOTIVO \_ \_ DE \_ WLAN             | La seguridad termina con un error.                                                                               |
| TIEMPO DE \_ ESPERA DE SEGURIDAD DEL CÓDIGO DE MOTIVO \_ \_ DE \_ WLAN             | Se ha pasado el tiempo de espera de la operación de seguridad.                                                                                |
| ERROR DE \_ \_ \_ ITINERANCIA DEL CÓDIGO DE MOTIVO DE \_ WLAN              | Controlador desconectado durante la itinerancia.                                                                           |
| ERROR DE \_ SEGURIDAD DE \_ \_ ITINERANCIA DE CÓDIGO \_ DE MOTIVO DE \_ WLAN    | No se pudo iniciar la seguridad para la itinerancia.                                                                        |
| ERROR \_ DE \_ SEGURIDAD \_ ADDHOC DEL CÓDIGO \_ DE MOTIVO DE \_ WLAN      | No se pudo iniciar la seguridad del mismo nivel ad hoc.                                                                    |
| CONTROLADOR DE CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ \_ DESCONECTADO          | Controlador desconectado.                                                                                         |
| ERROR EN \_ LA OPERACIÓN DEL CONTROLADOR DE CÓDIGO DE MOTIVO \_ \_ \_ DE \_ WLAN    | El controlador no pudo realizar algunas operaciones.                                                                    |
| EL CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ IHV \_ NO \_ ESTÁ DISPONIBLE           | El servicio IHV no está disponible.                                                                            |
| EL CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ IHV \_ NO \_ RESPONDE          | Se ha pasado el tiempo de espera de la respuesta del servicio IHV.                                                                 |
| TIEMPO DE \_ ESPERA DE \_ DESCONEXIÓN \_ DEL CÓDIGO DE MOTIVO DE \_ WLAN           | Se ha pasado el tiempo de espera a la espera de que el controlador se desconecte.                                                              |
| ERROR INTERNO \_ DEL CÓDIGO DE MOTIVO \_ \_ DE \_ WLAN             | Un error interno impidió que se completara la operación.                                              |
| TIEMPO DE ESPERA \_ DE SOLICITUD DE LA INTERFAZ DE USUARIO DEL CÓDIGO DE MOTIVO \_ \_ \_ \_ DE WLAN          | Se ha pasado el tiempo de espera de una solicitud de interacción del usuario.                                                                        |
| CÓDIGO DE \_ MOTIVO \_ DE WLAN \_ \_ DEMASIADOS \_ INTENTOS DE \_ SEGURIDAD | Itinerancia con demasiada frecuencia. La seguridad posterior no se completó después de 5 intentos.                                         |
| ERROR DE \_ INICIO DE LA APLICACIÓN DE CÓDIGO DE MOTIVO \_ \_ \_ DE \_ WLAN         | Se produjo un error interno del sistema operativo que produjo un error al iniciar la red hospedada inalámbrica. |



 

En la tabla siguiente se enumeran los códigos de error de seguridad de MSM.



| Código de motivo                                                             | Significado                                                                                                                                                                                   |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ÍNDICE DE \_ CLAVE NO VÁLIDA DEL PERFIL \_ \_ MSMSEC \_ \_ \_ \_ DEL CÓDIGO DE MOTIVO DE WLAN                | El índice de clave especificado no es válido.                                                                                                                                                         |
| CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ MSMSEC \_ PROFILE \_ PSK \_ PRESENT                       | Clave necesaria, PSK presente.                                                                                                                                                                |
| LONGITUD DE \_ CLAVE \_ DE PERFIL \_ MSMSEC \_ \_ \_ DEL CÓDIGO DE MOTIVO DE WLAN                        | Longitud de clave no válida.                                                                                                                                                                       |
| LONGITUD \_ DEL \_ \_ \_ \_ PSK DEL PERFIL MSMSEC DEL CÓDIGO \_ DE MOTIVO DE WLAN                        | Longitud de PSK no válida.                                                                                                                                                                       |
| PERFIL \_ \_ MSMSEC DE CÓDIGO DE MOTIVO DE WLAN \_ SIN CIFRADO DE \_ \_ \_ \_ \_ AUTENTICACIÓN ESPECIFICADO        | No se especifica ningún par de autenticación o cifrado.                                                                                                                                                           |
| PERFIL MSMSEC DE CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ \_ \_ \_ DEMASIADOS \_ CIFRADOS DE \_ \_ AUTENTICACIÓN ESPECIFICADOS | Se han especificado demasiados pares de autenticación y cifrado.                                                                                                                                                     |
| CIFRADO DE AUTENTICACIÓN DUPLICADO \_ \_ DE PERFIL \_ MSMSEC \_ \_ \_ \_ DE CÓDIGO DE MOTIVO DE WLAN            | El perfil contiene un par de autenticación y cifrado duplicados.                                                                                                                                              |
| CÓDIGO DE \_ MOTIVO \_ DE WLAN \_ MSMSEC \_ PROFILE \_ RAWDATA \_ INVALID                   | Los datos sin procesar del perfil no son válidos.                                                                                                                                                              |
| CIFRADO DE AUTENTICACIÓN NO VÁLIDA \_ \_ DEL PERFIL \_ MSMSEC \_ \_ \_ \_ DEL CÓDIGO DE MOTIVO DE WLAN              | Combinación de autenticación y cifrado no válida.                                                                                                                                                          |
| CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ MSMSEC \_ PROFILE \_ ONEX \_ DISABLED                     | 802.1X deshabilitado cuando es necesario habilitarlo.                                                                                                                                        |
| CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ MSMSEC \_ PROFILE \_ ONEX \_ ENABLED                      | 802.1X habilitado cuando es necesario deshabilitarlo.                                                                                                                                        |
| EL CÓDIGO \_ DE MOTIVO DE WLAN \_ \_ MSMSEC \_ NO ES VÁLIDO EN EL MODO \_ \_ PMKCACHE \_            | Modo de caché PMK no válido.                                                                                                                                                                   |
| TAMAÑO \_ DE \_ \_ \_ \_ \_ PMKCACHE \_ NO VÁLIDO DEL PERFIL MSMSEC DE CÓDIGO DE MOTIVO DE WLAN            | Tamaño de caché pmk no válido.                                                                                                                                                                   |
| CÓDIGO DE \_ \_ MOTIVO DE WLAN \_ MSMSEC \_ PROFILE INVALID \_ \_ PMKCACHE \_ TTL             | TTL de caché PMK no válida.                                                                                                                                                                    |
| MODO DE \_ \_ PREAUTORIZACIÓN \_ NO VÁLIDO DEL PERFIL MSMSEC \_ \_ \_ \_ DE CÓDIGO DE MOTIVO DE WLAN             | Modo de autenticación previa no válido.                                                                                                                                                                     |
| LIMITACIÓN \_ DE \_ AUTENTICACIÓN \_ PREVIA NO VÁLIDA DEL PERFIL MSMSEC \_ \_ DEL \_ \_ CÓDIGO DE MOTIVO DE WLAN         | Limitación de la autenticación previa no válida.                                                                                                                                                                 |
| SOLO HABILITADA LA AUTENTICACIÓN PREVIA DEL PERFIL \_ \_ \_ MSMSEC \_ DEL \_ \_ \_ CÓDIGO DE MOTIVO DE WLAN             | Autenticación previa habilitada cuando la caché de PMK está deshabilitada.                                                                                                                                               |
| RED DE \_ FUNCIONALIDAD \_ \_ MSMSEC \_ \_ DEL CÓDIGO DE MOTIVO DE WLAN                         | Error de coincidencia de funcionalidad en la red.                                                                                                                                                    |
| NIC \_ DE \_ FUNCIONALIDAD \_ MSMSEC \_ \_ DEL CÓDIGO DE MOTIVO DE WLAN                             | Error de coincidencia de funcionalidad en la NIC.                                                                                                                                                        |
| PERFIL \_ DE \_ FUNCIONALIDAD \_ MSMSEC \_ \_ DEL CÓDIGO DE MOTIVO DE WLAN                         | Error de coincidencia de funcionalidad en el perfil.                                                                                                                                                    |
| DETECCIÓN \_ DE \_ FUNCIONALIDAD \_ MSMSEC DEL \_ \_ CÓDIGO DE MOTIVO DE WLAN                       | La red no admite el tipo de funcionalidad especificado.                                                                                                                                       |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ PASSPHRASE \_ CHAR                   | La frase de contraseña contiene un carácter no válido.                                                                                                                                                    |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEYMATERIAL \_ CHAR                  | El material de clave contiene caracteres no válidos.                                                                                                                                                  |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ WRONG \_ KEYTYPE                     | El tipo de clave especificado no coincide con el material de clave.                                                                                                                                   |
| CELDA \_ MIXTA \_ \_ MSMSEC \_ DE \_ CÓDIGO DE MOTIVO DE WLAN                                 | Se sospecha que hay una celda mixta. El PUNTO de acceso no indica que sea compatible con un perfil habilitado para la privacidad.                                                                                  |
| TEMPORIZADORES DE AUTENTICACIÓN DE \_ \_ PERFIL \_ MSMSEC DE CÓDIGO DE MOTIVO DE WLAN \_ \_ NO \_ \_ VÁLIDOS              | El número de temporizadores de autenticación o el número de tiempos de espera especificados en el perfil no es válido.                                                                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ GKEY \_ INTV                | El intervalo de actualización de clave de grupo especificado en el perfil no es válido.                                                                                                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ TRANSITION \_ NETWORK                         | Se sospecha que hay una "red de transición". La seguridad heredada 802.11 se usa para el siguiente intento de autenticación.                                                                                  |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEY \_ UNMAPPED \_ CHAR                | La clave contiene caracteres que no están en el juego de caracteres ASCII.                                                                                                                      |
| AUTENTICACIÓN \_ DEL PERFIL DE FUNCIONALIDAD \_ \_ MSMSEC \_ DEL \_ \_ CÓDIGO DE MOTIVO DE WLAN                   | Error de coincidencia de funcionalidad porque la red no admite el método de autenticación en el perfil.                                                                                 |
| CIFRADO DE \_ PERFIL \_ DE FUNCIONALIDAD \_ MSMSEC \_ DEL \_ \_ CÓDIGO DE MOTIVO DE WLAN                 | Error de coincidencia de funcionalidad porque la red no admite el algoritmo de cifrado en el perfil.                                                                                      |
| MODO SEGURO \_ DE \_ PERFIL \_ MSMSEC \_ \_ \_ DE CÓDIGO DE MOTIVO DE WLAN                         | El valor del modo FIPS 140-2 en el perfil no es válido.                                                                                                                                          |
| NIC DE MODO SEGURO DEL PERFIL DE FUNCIONALIDAD \_ \_ \_ MSMSEC DEL \_ \_ \_ \_ CÓDIGO \_ DE MOTIVO DE WLAN        | El perfil requiere el modo FIPS 140-2, que no es compatible con la tarjeta de interfaz de red (NIC).                                                                                                 |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ PROFILE \_ SAFE \_ MODE \_ NW         | El perfil requiere el modo FIPS 140-2, que no es compatible con la red.                                                                                                                      |
| AUTENTICACIÓN NO ADMITIDA DEL \_ \_ PERFIL \_ MSMSEC \_ \_ DEL \_ CÓDIGO DE MOTIVO DE WLAN                  | Profile especifica un mecanismo de autenticación no compatible.                                                                                                                               |
| CIFRADO \_ NO ADMITIDO DEL PERFIL \_ \_ MSMSEC \_ \_ \_ DEL CÓDIGO DE MOTIVO DE WLAN                | Profile especifica un cifrado no admitido.                                                                                                                                                  |
| ERROR DE \_ SOLICITUD DE LA INTERFAZ DE USUARIO \_ \_ MSMSEC \_ \_ \_ DEL CÓDIGO DE MOTIVO DE WLAN                        | No se pudo poner en cola la solicitud de interfaz de usuario.                                                                                                                                               |
| NIC DE \_ \_ \_ MSMSEC DE FUNCIONALIDAD MSMSEC \_ \_ \_ DEL \_ CÓDIGO DE MOTIVO DE WLAN                    | La LAN inalámbrica requiere protección de marco de administración (MFP) y la interfaz de red no admite MFP. Para más información, consulte la modificación ieee 802.11w del estándar 802.11. |



 

En la tabla siguiente se enumeran los códigos de error de conexión de MSM.



| Código de motivo                                             | Significado                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| TIEMPO DE ESPERA DE INICIO DE \_ \_ \_ AUTENTICACIÓN MSMSEC DEL CÓDIGO \_ DE MOTIVO \_ DE \_ WLAN        | La autenticación 802.1X no se hizo en el tiempo configurado.                                                      |
| TIEMPO DE \_ ESPERA DE ÉXITO DE \_ \_ AUTENTICACIÓN MSMSEC \_ DEL \_ \_ CÓDIGO DE MOTIVO DE WLAN      | La autenticación 802.1X no se ha completado en el tiempo configurado.                                                   |
| TIEMPO DE \_ ESPERA DE INICIO DE CLAVE \_ \_ MSMSEC \_ DEL CÓDIGO DE MOTIVO \_ DE \_ WLAN         | El intercambio dinámico de claves no se hizo en el tiempo configurado.                                                       |
| TIEMPO DE \_ ESPERA DE ÉXITO DE CLAVE \_ \_ MSMSEC \_ DEL \_ \_ CÓDIGO DE MOTIVO DE WLAN       | El intercambio dinámico de claves no se ha completado en el tiempo configurado.                                                    |
| CÓDIGO DE \_ \_ MOTIVO DE WLAN \_ MSMSEC \_ M3 MISSING KEY \_ \_ \_ DATA      | El mensaje 3 del protocolo de enlace de 4 vías no tiene datos clave.                                                                    |
| FALTA \_ EL CÓDIGO DE MOTIVO DE WLAN \_ \_ MSMSEC \_ M3 \_ \_ IE             | El mensaje 3 del protocolo de enlace de 4 vías no tiene IE.                                                                          |
| FALTA LA CLAVE GRP DEL CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ MSMSEC \_ M3 \_ \_ \_       | El mensaje 3 del protocolo de enlace de 4 vías no tiene ninguna clave GRP.                                                                     |
| COINCIDENCIA \_ DEL CÓDIGO DE MOTIVO DE WLAN \_ \_ MSMSEC \_ PR \_ IE \_            | Error al coincidir las funcionalidades de seguridad de IE en M3.                                                               |
| COINCIDENCIA \_ DE CÓDIGO DE MOTIVO DE WLAN \_ \_ MSMSEC \_ SEC \_ IE \_           | Error al coincidir las funcionalidades de seguridad del IE secundario en M3.                                                     |
| CÓDIGO \_ DE MOTIVO DE WLAN \_ \_ MSMSEC \_ SIN CLAVE EN \_ PARES \_           | Se requiere una clave en pares, pero el punto de acceso (AP) solo ha configurado claves de grupo.                                        |
| FALTA \_ EL CÓDIGO DE MOTIVO DE WLAN \_ \_ MSMSEC \_ G1 KEY \_ \_ \_ DATA      | El mensaje 1 del protocolo de enlace de clave de grupo no tiene datos de clave.                                                                |
| FALTA LA CLAVE GRP DEL CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ MSMSEC \_ G1 \_ \_ \_       | El mensaje 1 del protocolo de enlace de clave de grupo no tiene ninguna clave de grupo.                                                               |
| CÓDIGO \_ DE MOTIVO DE WLAN \_ \_ MSMSEC \_ PEER \_ INDICATED \_ INSECURE   | Restablezca el punto de conexión seguro después de proteger la conexión.                                                                |
| CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ MSMSEC \_ SIN \_ AUTENTICADOR           | 802.1X indicó que no hay ningún autenticador, pero el perfil requiere uno.                                   |
| ERROR \_ DE NIC \_ \_ MSMSEC DE CÓDIGO DE \_ MOTIVO DE \_ WLAN                | Error en la configuración de la instalación de NIC.                                                                                 |
| \_ \_ \_ MSMSEC CANCELED DEL CÓDIGO DE MOTIVO \_ DE WLAN                   | Un autor de la llamada canceló la operación.                                                                              |
| FORMATO \_ DE CLAVE \_ \_ MSMSEC \_ \_ DEL CÓDIGO DE MOTIVO DE WLAN                 | El formato de clave especificado no está en un formato válido.                                                                     |
| SE \_ DETECTÓ \_ UNA DEGRADACIÓN \_ MSMSEC \_ DEL CÓDIGO DE \_ MOTIVO DE WLAN         | Se detectó una degradación de seguridad.                                                                               |
| SOSPECHA DE DISCREPANCIA DE CÓDIGO DE MOTIVO \_ \_ DE WLAN \_ MSMSEC \_ PSK \_ \_    | Se sospecha que hay una discrepancia de PSK.                                                                                     |
| ERROR \_ FORZADO DEL CÓDIGO DE MOTIVO DE WLAN \_ \_ MSMSEC \_ \_             | Se ha debido a un error forzado porque el método de conexión no era seguro.                                         |
| CÓDIGO \_ DE MOTIVO DE WLAN \_ \_ MSMSEC \_ M3 \_ \_ \_ DEMASIADAS RSNIE        | El mensaje 3 del protocolo de enlace de 4 formas contiene demasiados RSN IE (RSN).                                                     |
| CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ MSMSEC \_ M2 \_ MISSING KEY \_ \_ DATA      | El mensaje 2 del protocolo de enlace de 4 maneras no tiene datos clave (RSN Adhoc).                                                        |
| FALTA \_ EL CÓDIGO DE MOTIVO DE WLAN \_ \_ MSMSEC \_ M2 \_ \_ IE             | El mensaje 2 del protocolo de enlace de 4 maneras no tiene IE (RSN Adhoc).                                                              |
| CÓDIGO \_ DE MOTIVO DE WLAN \_ \_ MSMSEC \_ AUTH \_ WCN \_ COMPLETADO        |                                                                                                                  |
| ERROR DE \_ LA INTERFAZ DE USUARIO DE SEGURIDAD DE \_ \_ MSMSEC \_ EN \_ \_ EL CÓDIGO DE MOTIVO DE WLAN       | Error en la solicitud de la interfaz de usuario de seguridad porque no se pudo poner en cola o porque el usuario canceló la solicitud. |
| FALTA LA CLAVE GRP DE MGMT DEL CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ MSMSEC \_ M3 \_ \_ \_ \_ | El mensaje 3 del protocolo de enlace de cuatro maneras no tiene ninguna clave de grupo Mgmt (RSN).                                                        |
| FALTA LA CLAVE GRP DE MGMT DEL CÓDIGO DE MOTIVO DE WLAN \_ \_ \_ MSMSEC \_ G1 \_ \_ \_ \_ | El mensaje 1 del protocolo de enlace de clave de grupo no tiene ninguna clave de administración de grupo.                                                    |



 

En la tabla siguiente se enumeran los códigos de motivo 802.1X. Los elementos de esquema que se indican a continuación se definen en el esquema OneX y se especifican en el perfil WLAN.



| Código de motivo                                         | Significado                                                                                                                                                                            |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ONEX \_ NO PUEDE IDENTIFICAR AL \_ \_ \_ USUARIO                    | Ningún usuario está disponible para la autenticación 802.1X. Este error puede producirse cuando la autenticación de la máquina está deshabilitada y ningún usuario ha iniciado sesión en la máquina.                              |
| NO SE \_ ENCONTRÓ LA IDENTIDAD DE \_ \_ ONEX                          | No se encontró la identidad 802.1X.                                                                                                                                            |
| INTERFAZ DE USUARIO DE ONEX \_ \_ DESHABILITADA                                  | La autenticación solo se pudo completar a través de la interfaz de usuario y esta interfaz no se pudo mostrar.                                                                       |
| ERROR \_ DE EAP ONEX \_ \_ RECIBIDO                        | Error de autenticación eap.                                                                                                                                                     |
| ONEX \_ AUTHENTICATOR YA NO ESTÁ \_ \_ \_ PRESENTE            | El autenticador 802.1X salió de la red.                                                                                                                               |
| NO SE ADMITE \_ LA VERSIÓN DEL PERFIL \_ \_ DE \_ ONEX              | No se admite la versión del perfil de OneX proporcionada.                                                                                                                         |
| LONGITUD NO \_ VÁLIDA DEL PERFIL \_ DE ONEX \_                      | El perfil de OneX tiene una longitud no válida.                                                                                                                                            |
| TIPO DE \_ EAP NO PERMITIDO DE PERFIL \_ \_ \_ DE ONEX                | No se permite el tipo de EAP especificado en el perfil de OneX (posiblemente proporcionado por el elemento EAPType).                                                                               |
| MARCA O TIPO DE EAP NO VÁLIDO DE PERFIL \_ \_ \_ \_ \_ \_ DE ONEX         | El tipo de EAP especificado en el perfil de OneX (posiblemente proporcionado por el elemento EAPType) no es válido o una de las marcas de EAP (posiblemente proporcionadas en el elemento EAPConfig) no es válida. |
| ONEX \_ PROFILE \_ INVALID \_ ONEX \_ FLAGS                 | Las marcas suplicantes (posiblemente proporcionadas en el elemento EAPConfig) del perfil de OneX no son válidas.                                                                                 |
| VALOR DE TEMPORIZADOR \_ NO VÁLIDO DEL PERFIL \_ \_ \_ DE ONEX                | Un temporizador especificado en el perfil de OneX (posiblemente proporcionado por el elemento heldPeriod, authPeriod o startPeriod) no es válido.                                                        |
| MODO \_ \_ SUPLICANTE NO VÁLIDO DE PERFIL \_ \_ DE ONEX            | El modo de suplicación especificado en el perfil de OneX (posiblemente proporcionado por el elemento supplicantMode) no es válido.                                                                    |
| MODO DE AUTENTICACIÓN NO VÁLIDO DE PERFIL \_ \_ \_ \_ DE ONEX                  | El modo de autenticación especificado en el perfil de OneX (posiblemente proporcionado por el elemento authMode) no es válido.                                                                      |
| PROPIEDADES DE CONEXIÓN \_ DE \_ EAP NO \_ VÁLIDAS DE \_ \_ PERFIL DE ONEX | Las propiedades de conexión especificadas en el perfil de OneX (posiblemente proporcionadas por el elemento EAPConfig) no son válidas.                                                                  |



 

## <a name="remarks"></a>Comentarios

Se admite un conjunto limitado de códigos de motivo en Windows XP con Service Pack 3 (SP3) y en la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2). Los códigos de error de validación de perfil admitidos en Windows XP con SP3 y en la API de LAN inalámbrica para Windows XP con SP2 son los siguientes:

-   ESQUEMA DE \_ PERFIL NO VÁLIDO DEL CÓDIGO DE MOTIVO \_ \_ \_ DE \_ WLAN
-   FALTA EL \_ PERFIL DE CÓDIGO DE MOTIVO \_ \_ DE \_ WLAN
-   SSID DE PERFIL DE CÓDIGO DE MOTIVO DE WLAN \_ \_ NO \_ \_ \_ VÁLIDO

Los códigos de error de seguridad de MSM admitidos en Windows XP con SP3 y en la API de LAN inalámbrica para Windows XP con SP2 son los siguientes:

-   ÍNDICE DE \_ CLAVE NO VÁLIDA DEL PERFIL \_ \_ MSMSEC \_ \_ DEL \_ \_ CÓDIGO DE MOTIVO DE WLAN
-   LONGITUD DE \_ CLAVE \_ DE PERFIL \_ MSMSEC \_ DEL \_ \_ CÓDIGO DE MOTIVO DE WLAN
-   LONGITUD DE PSK DEL \_ \_ PERFIL \_ MSMSEC \_ DEL \_ CÓDIGO \_ DE MOTIVO DE WLAN
-   CIFRADO DE AUTENTICACIÓN NO VÁLIDO \_ DEL PERFIL \_ \_ MSMSEC \_ \_ \_ \_ DEL CÓDIGO DE MOTIVO DE WLAN
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ ONEX \_ DISABLED
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ ONEX \_ ENABLED
-   RED DE \_ \_ FUNCIONALIDAD \_ MSMSEC \_ DEL \_ CÓDIGO DE MOTIVO DE WLAN
-   NIC \_ DE \_ FUNCIONALIDAD \_ MSMSEC \_ \_ DEL CÓDIGO DE MOTIVO DE WLAN
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEYMATERIAL \_ CHAR
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ WRONG \_ KEYTYPE

Los códigos de error 802.1x admitidos en Windows XP con SP3 y en la API de LAN inalámbrica para Windows XP con SP2 son los siguientes:

-   LONGITUD NO \_ VÁLIDA DEL PERFIL \_ DE ONEX \_
-   MARCA O TIPO DE EAP NO VÁLIDO DE PERFIL \_ \_ \_ \_ \_ \_ DE ONEX
-   MODO DE AUTENTICACIÓN NO VÁLIDO DE PERFIL \_ \_ \_ \_ DE ONEX
-   PROPIEDADES DE CONEXIÓN \_ DE \_ EAP NO \_ VÁLIDAS DE \_ \_ PERFIL DE ONEX

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/>                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                  |
| Header<br/>                   | <dl> <dt>Wlanapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
</dt> <dt>

[**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
</dt> </dl>

 

 
