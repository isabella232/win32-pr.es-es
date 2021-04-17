---
description: Indica la razón por la que se ha producido un error en una operación de WLAN.
ms.assetid: 7b267f0b-b3f7-4729-bab4-de3bdd0a35a2
title: WLAN_REASON_CODE (wlanapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba0ae705244541063564431809cffa953a0f3fd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546910"
---
# <a name="wlan_reason_code"></a>\_código de motivo de WLAN \_

El tipo de **\_ \_ código de motivo de WLAN** indica la razón por la que se ha producido un error en una operación de WLAN.

Puede usar la función [**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring) para asignar un código de motivo numérico (por ejemplo, 0x00050007) a su significado del texto. También puede usar la tabla de búsqueda para ayudar a interpretar el valor numérico del código de motivo. Para ver la tabla de búsqueda, vea el Apéndice E: asignación de códigos de motivo a mensajes de eventos en el documento [solución de problemas de conexiones inalámbricas de Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10)).


```C++
typedef DWORD WLAN_REASON_CODE, *PWLAN_REASON_CODE;
```



En la tabla siguiente se enumeran los códigos de error generales.



| Código del motivo                 | Significado                            |
|-----------------------------|------------------------------------|
| código de motivo de WLAN \_ \_ \_ correcto | La operación se realiza correctamente.            |
| código de motivo de WLAN \_ \_ \_ desconocido | Se desconoce el motivo del error. |



 

En la tabla siguiente se muestran los códigos de error de configuración automática.



| Código de motivo                                  | Significado                                         |
|----------------------------------------------|-------------------------------------------------|
| red de código de motivo de WLAN \_ \_ \_ \_ no \_ compatible | La red inalámbrica no es compatible.         |
| Perfil de código de motivo de WLAN \_ \_ \_ \_ no \_ compatible | El perfil de red inalámbrica no es compatible. |



 

En la tabla siguiente se enumeran los códigos de error de conexión automática.



| Código de motivo                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| código de motivo de WLAN \_ \_ \_ sin \_ \_ conexión automática                   | El perfil no especifica ninguna conexión automática.                                                                                                                                                                                                                                                                                                                                                                                                               |
| código de motivo de WLAN \_ \_ \_ no \_ visible                           | La red inalámbrica no es visible.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| código de motivo de WLAN \_ \_ \_ \_ denegado                             | La red inalámbrica está bloqueada por la Directiva de grupo.                                                                                                                                                                                                                                                                                                                                                                                                        |
| código de motivo de WLAN \_ \_ \_ \_ denegado                           | La red inalámbrica está bloqueada por el usuario.                                                                                                                                                                                                                                                                                                                                                                                                            |
| código de motivo de WLAN \_ \_ tipo de \_ BSS \_ \_ no \_ permitido                | No se permite el tipo básico de Service Set (BSS) en este adaptador inalámbrico.                                                                                                                                                                                                                                                                                                                                                                               |
| \_ \_ código de motivo \_ de WLAN en \_ lista de errores \_                       | La red inalámbrica está en la lista de errores.                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ código de motivo \_ de WLAN en la \_ lista de bloqueados \_                      | La red inalámbrica está en la lista de bloqueados.                                                                                                                                                                                                                                                                                                                                                                                                            |
| lista de SSID de código de motivo de WLAN \_ \_ \_ \_ \_ demasiado \_ larga                  | El tamaño de la lista de identificadores de conjunto de servicios (SSID) supera el tamaño máximo admitido por el adaptador.                                                                                                                                                                                                                                                                                                                                                  |
| \_error de \_ llamada de conexión de código de motivo de \_ \_ WLAN \_                    | Se produce un error en la llamada de conexión del módulo específico del medio (MSM).                                                                                                                                                                                                                                                                                                                                                                                                     |
| \_error de \_ llamada de examen de código de motivo WLAN \_ \_ \_                       | Se produce un error en la llamada de recorrido de MSM.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| red de código de motivo de WLAN \_ \_ \_ \_ no \_ disponible                | La red especificada no está disponible. Este código de motivo también se usa cuando hay una falta de coincidencia entre las capacidades especificadas en un perfil XML y en las capacidades de interfaz y/o red. Por ejemplo, si un perfil especifica el uso de WPA2 cuando la NIC solo admite WPA, se devuelve este código de error. Además, si un perfil especifica el uso del modo FIPS cuando la NIC no es compatible con el modo FIPS, se devuelve este código de error.<br/> |
| \_ \_ \_ perfil \_ de código de motivo de WLAN cambiado \_ o \_ eliminado          | El perfil se modificó o eliminó antes de establecer la conexión.                                                                                                                                                                                                                                                                                                                                                                               |
| clave de código de motivo de WLAN \_ \_ \_ \_ no coincidente                          | La clave de perfil no coincide con la clave de red.                                                                                                                                                                                                                                                                                                                                                                                                         |
| código de motivo de WLAN \_ \_ \_ \_ no \_ responde                     | El usuario no responde.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ \_ \_ Perfil de AP de código \_ de motivo de WLAN no \_ permitido \_ para el \_ cliente | Una aplicación intentó aplicar un perfil de red hospedada inalámbrica a un adaptador de red inalámbrica físico con la función [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) , en lugar de hacerlo en un dispositivo virtual.                                                                                                                                                                                                                                                    |
| Perfil de PA de código de motivo de WLAN \_ \_ \_ \_ \_ no \_ permitido              | Una aplicación intentó aplicar un perfil de red hospedada inalámbrica a un adaptador de red inalámbrica físico con la función [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) , en lugar de hacerlo en un dispositivo virtual.                                                                                                                                                                                                                                                    |



 

En la tabla siguiente se enumeran los códigos de error de validación de perfil.



| Código de motivo                                                    | Significado                                                                                                                                                                                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| código de motivo de WLAN \_ \_ \_ esquema de perfil no válido \_ \_                   | El perfil no es válido según el esquema.                                                                                                                                                                                                  |
| \_falta el \_ Perfil de código de motivo de WLAN \_ \_                           | Falta el elemento WLANProfile.                                                                                                                                                                                                           |
| código de motivo de WLAN \_ \_ \_ nombre de perfil no válido \_ \_                     | El nombre del perfil no es válido.                                                                                                                                                                                                           |
| código de motivo de WLAN \_ \_ \_ tipo de perfil no válido \_ \_                     | El tipo del perfil no es válido.                                                                                                                                                                                                           |
| código de motivo de WLAN \_ \_ \_ tipo de PHY no válido \_ \_                         | El tipo de PHY no es válido.                                                                                                                                                                                                                      |
| código de motivo de WLAN \_ \_ \_ \_ falta seguridad MSM \_                     | Falta la configuración de seguridad de MSM.                                                                                                                                                                                                        |
| código de motivo de WLAN \_ \_ \_ \_ seguridad IHV \_ no \_ admitida              | Falta la configuración de seguridad del proveedor de hardware independiente (IHV).                                                                                                                                                                          |
| código de motivo de WLAN \_ \_ \_ \_ no coincidente del OUI de IHV \_                         | El OUI del perfil IHV no coincidía con el OUI del adaptador.                                                                                                                                                                                       |
| código de motivo de WLAN \_ \_ \_ \_ falta OUI de IHV \_                          | Falta la configuración del OUI de IHV.                                                                                                                                                                                                             |
| código de motivo de WLAN \_ \_ falta la \_ configuración de IHV \_ \_                     | Falta la configuración de seguridad de IHV.                                                                                                                                                                                                        |
| código de motivo de WLAN \_ \_ \_ \_ \_ no \_ compatible con la conectividad IHV          | Una aplicación intentó aplicar un perfil IHV en un adaptador que no admite la configuración de conectividad IHV.                                                                                                                                   |
| \_seguridad de \_ conflicto de código de motivo de WLAN \_ \_                         | Conflicto en la configuración de seguridad.                                                                                                                                                                                                               |
| \_ \_ falta seguridad del código de motivo de \_ WLAN \_                          | Falta la configuración de seguridad.                                                                                                                                                                                                            |
| código de motivo de WLAN \_ \_ \_ tipo de BSS no válido \_ \_                         | El tipo de BSS no es válido.                                                                                                                                                                                                                    |
| código de motivo de WLAN \_ \_ \_ modo de \_ conexión Adhoc no válido \_ \_           | No se puede establecer la conexión automática para una red ad hoc.                                                                                                                                                                                     |
| \_ \_ código de motivo \_ de WLAN sin \_ difusión \_ establecido \_ para \_ Adhoc            | No se puede establecer la no difusión para una red ad hoc.                                                                                                                                                                                            |
| \_ \_ \_ cambio automático de código \_ \_ de motivo de WLAN establecido \_ para \_ Adhoc              | No se puede establecer el cambio automático para una red ad hoc.                                                                                                                                                                                              |
| \_ \_ \_ cambio automático de código \_ \_ de motivo de WLAN establecido \_ para \_ \_ conexión manual | No se puede establecer el cambio automático para un perfil de conexión manual.                                                                                                                                                                                    |
| código de motivo de WLAN \_ \_ \_ \_ \_ falta Onex de seguridad IHV \_               | Falta la configuración de seguridad 802.1 X de IHV.                                                                                                                                                                                                 |
| SSID de Perfil de código de motivo de WLAN \_ \_ \_ \_ \_ no válido                     | Falta el SSID en el perfil o no es válido.                                                                                                                                                                                                |
| código de motivo de WLAN \_ \_ \_ demasiados \_ \_ SSID                            | Se han especificado demasiados SSID en el perfil.                                                                                                                                                                                                 |
| código de motivo de WLAN \_ \_ \_ \_ \_ no \_ compatible con la conectividad IHV          |                                                                                                                                                                                                                                               |
| \_ \_ código de motivo \_ \_ de WLAN \_ número máximo de clientes incorrectos \_ \_ \_ para \_ AP     | Una aplicación intentó aplicar un perfil de red hospedada inalámbrica a una NIC de adaptador de red físico mediante la función [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) y especificó un valor inaceptable para el número máximo de clientes permitido. |
| código de motivo de WLAN \_ \_ \_ canal no válido \_                           | El canal especificado no es válido.                                                                                                                                                                                                             |
| modo de operación de código de motivo de WLAN \_ \_ \_ \_ \_ no \_ compatible            |                                                                                                                                                                                                                                               |
| \_Perfil de AP automático de código de motivo de WLAN \_ \_ \_ \_ \_ no \_ permitido            | Se produjo un error interno del sistema operativo con la red hospedada inalámbrica.                                                                                                                                                                 |
| \_conexión automática del código de motivo de WLAN \_ \_ \_ \_ no \_ permitida             |                                                                                                                                                                                                                                               |



 

En la tabla siguiente se enumeran los códigos de error de incompatibilidad de red MSM.



| Código de motivo                                            | Significado                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| \_ \_ código de motivo \_ de WLAN seguridad no admitida \_ \_ establecida \_ por el \_ so | El sistema operativo no admite la configuración de seguridad. |
| código de motivo de WLAN \_ \_ \_ conjunto de seguridad no compatible \_ \_         | No se admite la configuración de seguridad.                         |
| código de motivo de WLAN \_ \_ \_ \_ sin coincidencia de tipo de BSS \_                 | El tipo de BSS no coincide.                                     |
| tipo de PHY de código de motivo de WLAN \_ \_ \_ \_ sin \_ coincidencia                 | El tipo de PHY no coincide.                                     |
| la velocidad de los códigos de motivo de WLAN no \_ \_ \_ \_ coincide                  | La velocidad de datos no coincide.                                    |



 

En la tabla siguiente se enumeran los códigos de error de conexión MSM.



| Código de motivo                                       | Significado                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| código de motivo de WLAN \_ \_ \_ \_ cancelado por el usuario               | El usuario ha cancelado la operación.                                                                             |
| \_error de \_ Asociación de código de motivo de WLAN \_ \_          | Controlador desconectado durante la asociación.                                                                       |
| \_tiempo de \_ espera de Asociación de código de motivo de \_ WLAN \_          | Se agotó el tiempo de espera de la asociación.                                                                                       |
| \_error de \_ \_ seguridad previa \_ del código de motivo de \_ WLAN        | Error de seguridad de la asociación anterior.                                                                            |
| \_error de \_ seguridad de código de motivo de WLAN \_ \_ \_      | No se pudo iniciar la seguridad después de la asociación.                                                                  |
| \_error de \_ seguridad de código de motivo de WLAN \_ \_             | La seguridad termina con un error.                                                                               |
| \_tiempo de \_ espera de seguridad de código de motivo de \_ WLAN \_             | Se agota el tiempo de espera de la operación de seguridad.                                                                                |
| \_error de \_ itinerancia de código de motivo de \_ WLAN \_              | Controlador desconectado en itinerancia.                                                                           |
| código de motivo de WLAN \_ \_ error de \_ seguridad de itinerancia \_ \_    | No se pudo iniciar la seguridad de itinerancia.                                                                        |
| \_error de \_ \_ seguridad Adhoc \_ del código de motivo de \_ WLAN      | No se pudo iniciar la seguridad del par ad hoc.                                                                    |
| controlador de código de motivo de WLAN \_ \_ \_ \_ desconectado          | Controlador desconectado.                                                                                         |
| \_error de \_ operación del controlador de código de motivo de \_ \_ WLAN \_    | El controlador no pudo realizar algunas operaciones.                                                                    |
| código de motivo de WLAN \_ \_ \_ IHV \_ no \_ disponible           | El servicio IHV no está disponible.                                                                            |
| código de motivo de WLAN que \_ \_ \_ IHV \_ no \_ responde          | La respuesta del servicio IHV agotó el tiempo de espera.                                                                 |
| \_tiempo de \_ \_ espera de desconexión de código de motivo WLAN \_           | Se agotó el tiempo de espera para que se desconectara el controlador.                                                              |
| \_ \_ error interno del código de motivo de \_ WLAN \_             | Un error interno impidió que la operación se completara.                                              |
| \_tiempo de \_ \_ espera de solicitud de IU de código de \_ motivo WLAN \_          | Se agotó el tiempo de espera de una solicitud de interacción del usuario.                                                                        |
| código de motivo de WLAN \_ \_ \_ demasiados \_ \_ intentos de seguridad \_ | Itinerancia demasiado a menudo. No se completó la seguridad posterior después de 5 intentos.                                         |
| código de motivo de WLAN \_ \_ error de \_ Inicio de AP \_ \_         | Se produjo un error interno del sistema operativo que produjo un error al iniciar la red hospedada inalámbrica. |



 

En la tabla siguiente se muestran los códigos de error de seguridad de MSM.



| Código de motivo                                                             | Significado                                                                                                                                                                                   |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| código de motivo de WLAN \_ \_ \_ Índice de \_ \_ clave no válido de \_ MSMSEC \_                | El índice de clave especificado no es válido.                                                                                                                                                         |
| código de motivo de WLAN \_ \_ MSMSEC de \_ \_ perfil \_ PSK \_ presente                       | Clave requerida, PSK presente.                                                                                                                                                                |
| código de motivo de WLAN \_ \_ longitud de \_ clave de \_ perfil MSMSEC \_ \_                        | Longitud de clave no válida.                                                                                                                                                                       |
| código de motivo de WLAN \_ MSMSEC de longitud de \_ \_ \_ PSK de perfil \_ \_                        | Longitud de PSK no válida.                                                                                                                                                                       |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil \_ sin \_ autenticación \_ \_ especificado        | No se especificaron pares de cifrado/autenticación.                                                                                                                                                           |
| código de motivo de WLAN \_ \_ \_ \_ perfil MSMSEC \_ demasiados \_ \_ \_ cifrado de autenticación \_ especificado | Se han especificado demasiados pares de autenticación/cifrado.                                                                                                                                                     |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ Perfil de \_ \_ cifrado de autenticación duplicado \_            | El perfil contiene un par de cifrado/autenticación duplicado.                                                                                                                                              |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil \_ RAWDATA \_ no válido                   | Los datos sin procesar del perfil no son válidos.                                                                                                                                                              |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ \_ \_ cifrado de autenticación no válido \_              | Combinación de autenticación/cifrado no válida.                                                                                                                                                          |
| código de motivo de WLAN \_ \_ MSMSEC de \_ \_ perfil \_ Onex \_ deshabilitado                     | 802.1 x deshabilitado cuando se requiere que esté habilitado.                                                                                                                                        |
| código de motivo de WLAN \_ \_ MSMSEC de \_ \_ perfil \_ Onex \_ habilitado                      | 802.1 x habilitado cuando es necesario deshabilitarlo.                                                                                                                                        |
| código de motivo de WLAN \_ \_ MSMSEC el \_ \_ \_ \_ modo PMKCACHE no válido \_            | Modo de caché PMK no válido.                                                                                                                                                                   |
| código de motivo de WLAN \_ \_ MSMSEC de \_ \_ \_ tamaño de PMKCACHE no válido \_ \_            | Tamaño de caché PMK no válido.                                                                                                                                                                   |
| código de motivo de WLAN \_ \_ \_ \_ perfil MSMSEC \_ no válido \_ PMKCACHE \_ TTL             | TTL de caché PMK no válido.                                                                                                                                                                    |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ \_ \_ modo de preautenticación no válido \_             | Modo de preautenticación no válido.                                                                                                                                                                     |
| código de motivo de WLAN \_ \_ \_ limitación de \_ \_ \_ autenticación previa no válida \_         | Limitación de autenticación previa no válida.                                                                                                                                                                 |
| código de motivo de WLAN \_ \_ \_ \_ \_ \_ habilitada para la autenticación previa del perfil MSMSEC \_             | La autenticación previa está habilitada cuando la caché de PMK está deshabilitada.                                                                                                                                               |
| código de motivo de WLAN \_ \_ \_ red de \_ funcionalidad MSMSEC \_                         | Error de coincidencia de funcionalidad en la red.                                                                                                                                                    |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ capacidad \_ NIC                             | Error de coincidencia de funcionalidad en la NIC.                                                                                                                                                        |
| código de motivo de WLAN \_ \_ \_ Perfil de \_ capacidad MSMSEC \_                         | Error de coincidencia de funcionalidad en el perfil.                                                                                                                                                    |
| código de motivo de WLAN \_ \_ \_ detección de \_ capacidad MSMSEC \_                       | La red no admite el tipo de capacidad especificado.                                                                                                                                       |
| código de motivo de WLAN \_ \_ carácter de frase de \_ \_ contraseña de perfil MSMSEC \_ \_                   | La frase de contraseña contiene un carácter no válido.                                                                                                                                                    |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil \_ KEYMATERIAL \_ Char                  | El material de clave contiene un carácter no válido.                                                                                                                                                  |
| código de motivo de WLAN \_ \_ MSMSEC de \_ \_ perfil \_ incorrecto \_ KEYTYPE                     | El tipo de clave especificado no coincide con el material de clave.                                                                                                                                   |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ \_ celda mixta                                 | Una celda mixta es sospechosa. El AP no señala que es compatible con un perfil habilitado para la privacidad.                                                                                  |
| código de motivo de WLAN \_ \_ \_ \_ temporizadores de autenticación de perfil MSMSEC \_ \_ \_ no válidos              | El número de temporizadores de autenticación o el número de tiempos de espera especificados en el perfil no es válido.                                                                                        |
| código de motivo de WLAN \_ \_ MSMSEC de \_ \_ perfil \_ no válido \_ GKEY \_ INTV                | El intervalo de actualización de la clave de grupo especificado en el perfil no es válido.                                                                                                                        |
| código de motivo de WLAN \_ \_ \_ red de \_ transición MSMSEC \_                         | Una "red de transición" es sospechosa. La seguridad de 802,11 heredada se usa para el siguiente intento de autenticación.                                                                                  |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ clave de Perfil de \_ carácter no \_ asignado \_                | La clave contiene caracteres que no están en el juego de caracteres ASCII.                                                                                                                      |
| código de motivo de WLAN \_ \_ MSMSEC de Perfil de capacidad de \_ \_ \_ \_ autenticación                   | Error de coincidencia de funcionalidad porque la red no admite el método de autenticación en el perfil.                                                                                 |
| código de motivo de WLAN \_ \_ \_ \_ \_ cifrado de Perfil de capacidad MSMSEC \_                 | Error de coincidencia de funcionalidad porque la red no admite el algoritmo de cifrado en el perfil.                                                                                      |
| código de motivo de WLAN \_ \_ \_ \_ \_ modo seguro de perfil MSMSEC \_                         | El valor del modo FIPS 140-2 en el perfil no es válido.                                                                                                                                          |
| código de motivo de WLAN \_ \_ MSMSEC de \_ \_ \_ \_ \_ modo \_ seguro de Perfil de capacidad        | El perfil requiere el modo FIPS 140-2, que no es compatible con la tarjeta de interfaz de red (NIC).                                                                                                 |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ \_ modo seguro de Perfil de capacidad \_ \_ \_ NW         | El perfil requiere el modo FIPS 140-2, que no es compatible con la red.                                                                                                                      |
| código de motivo de WLAN \_ \_ Perfil de MSMSEC de \_ \_ \_ autenticación no admitido \_                  | Profile especifica un mecanismo de autenticación no compatible.                                                                                                                               |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ \_ cifrado no admitido \_                | Profile especifica un cifrado no admitido.                                                                                                                                                  |
| código de motivo de WLAN \_ \_ error de \_ solicitud de \_ IU MSMSEC \_ \_                        | No se pudo poner en cola la solicitud de interfaz de usuario.                                                                                                                                               |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ funcionalidad de \_ MFP \_ NW \_                    | La LAN inalámbrica requiere la protección de fotogramas de administración (MFP) y la interfaz de red no es compatible con MFP. Para obtener más información, consulte la enmienda IEEE 802.11 w al estándar 802,11. |



 

En la tabla siguiente se enumeran los códigos de error de conexión MSM.



| Código de motivo                                             | Significado                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| código de motivo de WLAN \_ \_ MSMSEC de \_ \_ Inicio de autenticación \_ \_        | la autenticación de 802.1 x no se inició en el tiempo configurado.                                                      |
| código de motivo de WLAN \_ \_ MSMSEC de tiempo de \_ \_ espera de autenticación \_ correcta \_      | la autenticación de 802.1 x no se completó dentro del tiempo configurado.                                                   |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ tiempo de espera de inicio de clave \_ \_         | El intercambio de claves dinámicas no se inició en el tiempo configurado.                                                       |
| código de motivo de WLAN \_ \_ MSMSEC de tiempo de \_ \_ espera de clave \_ correcta \_       | El intercambio de claves dinámicas no se completó dentro del tiempo configurado.                                                    |
| Código de motivo de WLAN \_ \_ \_ MSMSEC \_ \_ \_ datos de clave que faltan \_      | El mensaje 3 del Protocolo de enlace de 4 vías no tiene datos de clave.                                                                    |
| Código de motivo de WLAN \_ \_ \_ MSMSEC \_ m3 \_ Missing \_ IE             | El mensaje 3 del Protocolo de enlace de 4 vías no tiene IE.                                                                          |
| Código de motivo de WLAN \_ \_ MSMSEC, falta la \_ \_ \_ \_ \_ clave GRP       | El mensaje 3 del Protocolo de enlace de 4 vías no tiene ninguna clave GRP.                                                                     |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ búsqueda de \_ \_ coincidencias de IE            | Error en las capacidades de seguridad de búsqueda de coincidencias de IE en m3.                                                               |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ s \_ búsqueda de \_ coincidencias           | Error en las capacidades de seguridad de coincidencia de IE secundario en m3.                                                     |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ no hay \_ clave en pares \_           | Se requiere una clave en pares, pero el punto de acceso (AP) solo configuraba claves de grupo.                                        |
| Código de motivo de WLAN \_ \_ \_ MSMSEC \_ G1 \_ faltan \_ datos de clave \_      | El mensaje 1 del Protocolo de enlace de clave de grupo no tiene datos de clave.                                                                |
| Código de motivo de WLAN \_ \_ \_ MSMSEC \_ G1 \_ falta la \_ \_ clave GRP       | El mensaje 1 del Protocolo de enlace de clave de grupo no tiene ninguna clave de grupo.                                                               |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ del mismo nivel \_ indicado \_ como no seguro   | El bit seguro de restablecimiento de AP después de la conexión se protegió.                                                                |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ sin \_ autenticador           | 802.1 x indica que no hay ningún autenticador, pero el perfil requiere uno.                                   |
| código de motivo de WLAN \_ \_ \_ error de \_ NIC MSMSEC \_                | Error en la configuración de establecimiento de la NIC.                                                                                 |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ cancelado                   | Un llamador canceló la operación.                                                                              |
| código de motivo de WLAN \_ \_ \_ formato de \_ clave MSMSEC \_                 | El formato de clave especificado no tiene un formato válido.                                                                     |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ degradación \_ detectada         | Se detectó una degradación de seguridad.                                                                               |
| código de motivo de WLAN MSMSEC error de \_ \_ \_ coincidencia de \_ PSK \_ \_    | Se sospecha que la falta de coincidencia de PSK.                                                                                     |
| código de motivo de WLAN \_ \_ MSMSEC de \_ \_ \_ error forzado             | Se produjo un error forzado porque el método de conexión no era seguro.                                         |
| Código de motivo de WLAN \_ \_ \_ MSMSEC \_ m3 \_ demasiados \_ \_ RSNIE        | El mensaje 3 del Protocolo de enlace de 4 vías contiene demasiados RSN (RSN).                                                     |
| Código de motivo de WLAN \_ \_ \_ MSMSEC \_ \_ datos de clave que faltan m2 \_ \_      | El mensaje 2 del Protocolo de enlace de 4 vías no tiene datos clave (RSN Adhoc).                                                        |
| Código de motivo de WLAN \_ \_ \_ MSMSEC \_ m2 \_ falta \_ IE             | El mensaje 2 del Protocolo de enlace de 4 vías no tiene IE (RSN Adhoc).                                                              |
| código de motivo de WLAN \_ \_ MSMSEC de \_ \_ autenticación \_ WCN \_ completado        |                                                                                                                  |
| código de motivo de WLAN \_ \_ error de \_ UI de \_ seguridad MSMSEC \_ \_       | Error en la solicitud de IU de seguridad porque la solicitud no se pudo poner en cola o porque el usuario canceló la solicitud. |
| Código de motivo de WLAN \_ \_ \_ MSMSEC \_ m3 \_ falta la \_ \_ clave GRP de administración \_ | El mensaje 3 del Protocolo de enlace de 4 vías no tiene ninguna clave de grupo de administración (RSN).                                                        |
| Código de motivo de WLAN \_ \_ \_ MSMSEC \_ G1 \_ falta la \_ \_ clave GRP de administración \_ | El mensaje 1 del Protocolo de enlace de clave de grupo no tiene ninguna clave de administración de grupo.                                                    |



 

En la tabla siguiente se enumeran los códigos de motivo de 802.1 X. Los elementos de esquema que se mencionan a continuación se definen en el esquema OneX y se especifican en el perfil de WLAN.



| Código de motivo                                         | Significado                                                                                                                                                                            |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ONEX \_ no se puede \_ \_ identificar al \_ usuario                    | Ningún usuario está disponible para la autenticación de 802.1 X. Este error puede producirse si la autenticación de la máquina está deshabilitada y ningún usuario ha iniciado sesión en la máquina.                              |
| \_identidad Onex \_ no \_ encontrada                          | No se encontró la identidad de 802.1 X.                                                                                                                                            |
| interfaz de usuario de ONEX \_ \_ deshabilitada                                  | Solo se puede completar la autenticación a través de la interfaz de usuario y no se puede mostrar esta interfaz.                                                                       |
| ONEX \_ - \_ error de EAP \_ recibido                        | Error de autenticación de EAP.                                                                                                                                                     |
| el \_ autenticador Onex ya \_ no \_ \_ está presente            | El autenticador de 802.1 X salió de la red.                                                                                                                               |
| \_versión de perfil Onex \_ \_ no \_ compatible              | No se admite la versión del perfil OneX proporcionado.                                                                                                                         |
| \_ \_ longitud no válida del perfil Onex \_                      | El perfil OneX tiene una longitud no válida.                                                                                                                                            |
| Perfil ONEX no \_ \_ permitido \_ tipo de EAP \_                | El tipo de EAP especificado en el perfil OneX (posiblemente proporcionado por el elemento EAPType) no está permitido.                                                                               |
| \_ \_ \_ \_ tipo \_ o marca de EAP \_ no válido del perfil Onex         | El tipo de EAP especificado en el perfil OneX (posiblemente proporcionado por el elemento EAPType) no es válido, o una de las marcas EAP (posiblemente proporcionado en el elemento EAPConfig) no es válida. |
| \_ \_ indicadores Onex no válidos del perfil Onex \_ \_                 | Las marcas de suplicante (posiblemente proporcionadas en el elemento EAPConfig) en el perfil OneX no son válidas.                                                                                 |
| \_valor de \_ temporizador no válido \_ del perfil Onex \_                | Un temporizador especificado en el perfil OneX (posiblemente proporcionado por el elemento heldPeriod, authPeriod o startPeriod) no es válido.                                                        |
| \_ \_ \_ modo suplicante no válido del perfil Onex \_            | El modo suplicante especificado en el perfil OneX (posiblemente proporcionado por el elemento supplicantMode) no es válido.                                                                    |
| \_modo de \_ autenticación no válido del perfil \_ Onex \_                  | El modo de autenticación especificado en el perfil OneX (posiblemente proporcionado por el elemento authMode) no es válido.                                                                      |
| \_propiedades de \_ \_ conexión EAP \_ no VÁLIDAs del perfil Onex \_ | Las propiedades de conexión especificadas en el perfil OneX (posiblemente proporcionado por el elemento EAPConfig) no son válidas.                                                                  |



 

## <a name="remarks"></a>Observaciones

En Windows XP con Service Pack 3 (SP3) y en la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2) se admite un conjunto limitado de códigos de motivo. Los códigos de error de validación de perfiles que se admiten en Windows XP con SP3 y en la API de LAN inalámbrica para Windows XP con SP2 son los siguientes:

-   código de motivo de WLAN \_ \_ \_ esquema de perfil no válido \_ \_
-   \_falta el \_ Perfil de código de motivo de WLAN \_ \_
-   SSID de Perfil de código de motivo de WLAN \_ \_ \_ \_ \_ no válido

Los códigos de error de seguridad de MSM admitidos en Windows XP con SP3 y en la API de LAN inalámbrica para Windows XP con SP2 son los siguientes:

-   código de motivo de WLAN \_ \_ \_ Índice de \_ \_ clave no válido de \_ MSMSEC \_
-   código de motivo de WLAN \_ \_ longitud de \_ clave de \_ perfil MSMSEC \_ \_
-   código de motivo de WLAN \_ MSMSEC de longitud de \_ \_ \_ PSK de perfil \_ \_
-   código de motivo de WLAN \_ \_ \_ MSMSEC \_ \_ \_ cifrado de autenticación no válido \_
-   código de motivo de WLAN \_ \_ MSMSEC de \_ \_ perfil \_ Onex \_ deshabilitado
-   código de motivo de WLAN \_ \_ MSMSEC de \_ \_ perfil \_ Onex \_ habilitado
-   código de motivo de WLAN \_ \_ \_ red de \_ funcionalidad MSMSEC \_
-   código de motivo de WLAN \_ \_ \_ MSMSEC \_ capacidad \_ NIC
-   código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil \_ KEYMATERIAL \_ Char
-   código de motivo de WLAN \_ \_ MSMSEC de \_ \_ perfil \_ incorrecto \_ KEYTYPE

Los códigos de error de 802.1 x que se admiten en Windows XP con SP3 y en la API de LAN inalámbrica para Windows XP con SP2 son los siguientes:

-   \_ \_ longitud no válida del perfil Onex \_
-   \_ \_ \_ \_ tipo \_ o marca de EAP \_ no válido del perfil Onex
-   \_modo de \_ autenticación no válido del perfil \_ Onex \_
-   \_propiedades de \_ \_ conexión EAP \_ no VÁLIDAs del perfil Onex \_

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/>                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Wlanapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
</dt> <dt>

[**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
</dt> </dl>

 

 
