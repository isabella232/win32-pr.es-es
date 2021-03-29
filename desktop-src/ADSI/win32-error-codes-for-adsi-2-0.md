---
title: Códigos de error de Win32 para ADSI 2,0
description: En la tabla siguiente se enumeran los mensajes de error LDAP para ADSI 2,0.
ms.assetid: 99d97ea8-1dcc-49f4-a2bf-36ff8076e83a
ms.tgt_platform: multiple
keywords:
- Códigos de error de Win32 para ADSI 2,0 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e079fa6a98df28625f6307f774ce194712a52a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903015"
---
# <a name="win32-error-codes-for-adsi-20"></a>Códigos de error de Win32 para ADSI 2,0

En la tabla siguiente se enumeran los mensajes de error LDAP para ADSI 2,0.



| Valor de error ADSI | Mensaje LDAP                           | Mensaje Win32                        | Descripción                                          |
|------------------|----------------------------------------|--------------------------------------|------------------------------------------------------|
| 0                | **LDAP \_ correcto**                      | **SIN \_ errores**                        | Operación realizada correctamente.                                 |
| 0x80070002       | **\_objeto LDAP no \_ tal \_**             | **\_ \_ no \_ se encontró el archivo de error**          | El objeto no existe.                               |
| 0x80070005       | **\_método de autenticación LDAP \_ \_ no \_ compatible** | **ERROR de \_ acceso \_ denegado**            | Método de autenticación no admitido.                 |
| 0x80070005       | **se \_ \_ requiere la autenticación segura LDAP \_**       | **ERROR de \_ acceso \_ denegado**            | Requiere autenticación sólida.                      |
| 0x80070005       | **\_autenticación no adecuada de LDAP \_**          | **ERROR de \_ acceso \_ denegado**            | Autenticación inadecuada.                        |
| 0x80070005       | **\_derechos insuficientes LDAP \_**         | **ERROR de \_ acceso \_ denegado**            | El usuario no tiene derechos de acceso suficientes.                 |
| 0x80070005       | **\_autenticación LDAP \_ desconocida**                | **ERROR de \_ acceso \_ denegado**            | Se produjo un error de autenticación desconocido.               |
| 0x80070008       | **LDAP \_ sin \_ memoria**                   | **ERROR \_ de \_ memoria insuficiente \_**       | El sistema no tiene memoria suficiente.                             |
| 0x8007001F       | **\_otro LDAP**                        | **ERROR de \_ gen. \_**              | Error desconocido.                              |
| 0x8007001F       | **\_error local de LDAP \_**                 | **ERROR de \_ gen. \_**              | Se produjo un error local.                                |
| 0x80070037       | **LDAP \_ no disponible**                  | **\_ \_ no existe el desarrollador de errores \_**           | El servidor no está disponible.                             |
| 0x8007003A       | **\_servidor LDAP \_ inactivo**                 | **ERROR \_ de \_ net \_ resp**            | No se puede establecer contacto con el servidor LDAP.                      |
| 0x8007003B       | **\_error de codificación \_ LDAP**              | **ERROR \_ UNEXP \_ net \_ Err**           | Error de codificación.                             |
| 0x8007003B       | **\_error de descodificación LDAP \_**              | **ERROR \_ UNEXP \_ net \_ Err**           | Error de descodificación.                             |
| 0x80070044       | **\_límite de administración LDAP \_ \_ superado**       | **ERROR \_ demasiados \_ \_ nombres**          | Se superó el límite de administración en el servidor.         |
| 0x80070056       | **\_credenciales no válidas de LDAP \_**         | **ERROR \_ de \_ contraseña no válida**         | Credencial no válida.                                |
| 0x80070057       | **\_Sintaxis DN no válida de LDAP \_ \_**          | **ERROR \_ de \_ parámetro no válido**        | El nombre distintivo tiene una sintaxis no válida.     |
| 0x80070057       | **infracción de \_ nomenclatura LDAP \_**            | **ERROR \_ de \_ parámetro no válido**        | Infracción de nomenclatura.                                    |
| 0x80070057       | **infracción de \_ clase de objeto LDAP \_ \_**     | **ERROR \_ de \_ parámetro no válido**        | Infracción de clase de objeto.                              |
| 0x80070057       | **\_error de filtro LDAP \_**                | **ERROR \_ de \_ parámetro no válido**        | El filtro de búsqueda no es válido.                                |
| 0x80070057       | **\_error de parámetro LDAP \_**                 | **ERROR \_ de \_ parámetro no válido**        | Se pasó un parámetro incorrecto a una rutina.               |
| 0X8007006E       | **\_error de operaciones LDAP \_**            | **ERROR \_ al abrir el error \_**              | Error de operación.                            |
| 0x8007007A       | **resultados de LDAP \_ \_ demasiado \_ grandes**          | **ERROR \_ de \_ búfer insuficiente**      | El conjunto de resultados es demasiado grande.                            |
| 0x8007007B       | **\_Sintaxis LDAP no válida \_**              | **ERROR \_ de \_ nombre no válido**             | Sintaxis no válida.                                    |
| 0x8007007C       | **\_error de protocolo LDAP \_**              | **ERROR \_ de \_ nivel no válido**            | Error de protocolo.                                      |
| 0x800700B7       | **LDAP \_ ya \_ existe**              | **el ERROR \_ ya \_ existe**           | El objeto ya existe.                               |
| 0x800700EA       | **\_resultados parciales de LDAP \_**             | **ERROR \_ más \_ datos**                | Resultados parciales y referencias recibidas.              |
| 0x800700EA       | **LDAP \_ ocupado**                         | **ERROR \_ ocupado**                      | El servidor está ocupado.                                      |
| 0x800703EB       | **LDAP \_ que no va \_ a \_ realizar**       | **\_no se \_ puede \_ completar el error**        | El servidor no puede realizar la operación.                     |
| 0x8007041D       | **\_tiempo de espera LDAP**                      | **\_tiempo de \_ espera de solicitud de servicio de error \_** | Se agotó el tiempo de espera de la búsqueda.                                    |
| 0x800704B8       | **\_comparación LDAP \_ false**               | **error de ERROR \_ extendido \_**           | La comparación da como resultado **false**.                           |
| 0x800704B8       | **\_comparación LDAP \_ true**                | **error de ERROR \_ extendido \_**           | La comparación da como resultado **true**.                            |
| 0x800704B8       | **\_referencia LDAP**                     | **error de ERROR \_ extendido \_**           | No se puede resolver la referencia.                             |
| 0x800704B8       | **\_extensión crít no disponible LDAP \_ \_** | **error de ERROR \_ extendido \_**           | La extensión crítica no está disponible.                   |
| 0x800704B8       | **\_atributo no \_ tal de LDAP \_**          | **error de ERROR \_ extendido \_**           | El atributo solicitado no existe.                  |
| 0x800704B8       | **tipo no definido de LDAP \_ \_**              | **error de ERROR \_ extendido \_**           | El tipo no está definido.                                 |
| 0x800704B8       | **\_coincidencia inadecuada de LDAP \_**      | **error de ERROR \_ extendido \_**           | Hubo una coincidencia inadecuada.                 |
| 0x800704B8       | **infracción de \_ restricción LDAP \_**        | **error de ERROR \_ extendido \_**           | Se ha producido una infracción de restricción.                     |
| 0x800704B8       | **el \_ atributo \_ o \_ valor LDAP \_ existe** | **error de ERROR \_ extendido \_**           | El atributo existe o el valor se ha asignado. |
| 0x800704B8       | **\_problema de alias LDAP \_**               | **error de ERROR \_ extendido \_**           | El alias no es válido.                                  |
| 0x800704B8       | **LDAP \_ es \_ hoja**                     | **error de ERROR \_ extendido \_**           | El objeto es una hoja.                                    |
| 0x800704B8       | **problema en el alias de LDAP \_ \_ deref \_**        | **error de ERROR \_ extendido \_**           | No se puede desreferenciar el alias.                        |
| 0x800704B8       | **\_detección de bucle LDAP \_**                 | **error de ERROR \_ extendido \_**           | Se detectó un bucle.                                   |
| 0x800704B8       | **LDAP \_ no \_ permitido \_ en \_ Nonleaf**    | **error de ERROR \_ extendido \_**           | No se permite la operación en un objeto no hoja.       |
| 0x800704B8       | **LDAP \_ no \_ permitido \_ en \_ RDN**        | **error de ERROR \_ extendido \_**           | No se permite la operación en RDN.                     |
| 0x800704B8       | **\_no se \_ mods la clase de objeto \_ \_ LDAP**      | **error de ERROR \_ extendido \_**           | No se puede modificar la clase de objeto.                          |
| 0x800704B8       | **LDAP \_ afecta a \_ varios \_ DSA**      | **error de ERROR \_ extendido \_**           | Varios agentes de servicios de directorio se ven afectados.      |
| 0x800704C7       | **\_usuario LDAP \_ cancelado**              | **ERROR \_ cancelado**                 | El usuario ha cancelado la operación.                     |
| 0x80070718       | **\_TIMELIMIT LDAP \_ superado**          | **ERROR: \_ no \_ hay \_ cuota suficiente**        | Se superó el límite de tiempo.                                 |
| 0x80070718       | **\_SIZELIMIT LDAP \_ superado**          | **ERROR: \_ no \_ hay \_ cuota suficiente**        | Se superó el límite de tamaño.                                 |



 

En ADSI 2,0, se asignan varios mensajes de error LDAP a un código de error de Win32 como **\_ \_ error extendido de error**. Llame a [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) para recuperar la cadena de error devuelta por el servidor. Para obtener más información, consulte [los mensajes de error extendidos de ADSI](adsi-extended-error-messages.md) .

 

 




