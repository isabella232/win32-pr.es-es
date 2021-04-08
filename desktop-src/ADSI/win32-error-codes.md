---
title: Códigos de error de Win32
description: En la tabla siguiente se enumeran los mensajes de error LDAP para ADSI.
ms.assetid: b609bd56-770a-4546-8640-26ad6e108d54
ms.tgt_platform: multiple
keywords:
- Códigos de error de Win32 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d8151c07fb6470d395f15e088ae5e50f3e43bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993832"
---
# <a name="win32-error-codes"></a>Códigos de error de Win32

En la tabla siguiente se enumeran los mensajes de error LDAP para ADSI.



| Valor de error ADSI | Mensaje LDAP                           | Mensaje Win32                               | Descripción                                      |
|------------------|----------------------------------------|---------------------------------------------|--------------------------------------------------|
| 0L               | **LDAP \_ correcto**                      | **SIN \_ errores**                               | Operación realizada correctamente.                             |
| 0x80070005L      | **\_derechos insuficientes LDAP \_**         | **ERROR de \_ acceso \_ denegado**                   | El usuario no tiene derechos de acceso suficientes.             |
| 0x80070008L      | **LDAP \_ sin \_ memoria**                   | **ERROR \_ de \_ memoria insuficiente \_**              | El sistema no tiene memoria suficiente.                         |
| 0x8007001fL      | **\_otro LDAP**                        | **ERROR de \_ gen. \_**                     | Error desconocido.                                   |
| 0x800700eaL      | **\_resultados parciales de LDAP \_**             | **ERROR \_ más \_ datos**                       | Resultados parciales y referencias recibidas.          |
| 0x800700eaL      | **\_más \_ resultados de LDAP \_ para \_ devolver**    | **ERROR \_ más \_ datos**                       | Se devolverán más resultados.                 |
| 0x800704c7L      | **\_usuario LDAP \_ cancelado**              | **ERROR \_ cancelado**                        | El usuario canceló la operación.                     |
| 0x800704c9L      | **\_error de conexión LDAP \_**               | **ERROR de \_ conexión \_ rechazada**              | No se puede establecer la conexión.                 |
| 0x8007052eL      | **\_credenciales no válidas de LDAP \_**         | **ERROR de \_ Inicio de sesión \_**                   | La credencial proporcionada no es válida.                |
| 0x800705b4L      | **\_tiempo de espera LDAP**                      | **tiempo de espera de ERROR \_**                          | Se agotó el tiempo de espera de la búsqueda.                                |
| 0x80071392L      | **LDAP \_ ya \_ existe**              | **el \_ objeto de error \_ ya \_ existe**          | El objeto ya existe.                           |
| 0x8007200aL      | **\_atributo no \_ tal de LDAP \_**          | **ERROR \_ DS \_ ningún \_ atributo \_ o \_ valor**     | El atributo solicitado no existe.              |
| 0x8007200bL      | **\_Sintaxis LDAP no válida \_**              | **ERROR \_ de \_ \_ Sintaxis de atributo no válida de DS \_**   | La sintaxis no es válida.                             |
| 0x8007200cL      | **tipo no definido de LDAP \_ \_**              | **ERROR \_ de \_ tipo de atributo DS no \_ \_ definido**   | Tipo no definido.                                |
| 0x8007200dL      | **el \_ atributo \_ o \_ valor LDAP \_ existe** | **ERROR \_ el \_ atributo \_ o \_ valor de DS \_ existe** | El atributo existe o se ha asignado el valor. |
| 0x8007200eL      | **LDAP \_ ocupado**                         | **ERROR de \_ DS \_ ocupado**                         | El servidor está ocupado.                                  |
| 0x8007200fL      | **LDAP \_ no disponible**                  | **ERROR \_ DS \_ no disponible**                  | El servidor no está disponible.                         |
| 0x80072014L      | **infracción de \_ clase de objeto LDAP \_ \_**     | **ERROR \_ de \_ \_ infracción de clase obj DS \_**        | Infracción de clase de objeto.                          |
| 0x80072015L      | **LDAP \_ no \_ permitido \_ en \_ Nonleaf**    | **ERROR \_ \_ de la peralte \_ de DS en \_ no \_ hoja**          | No se permite la operación en un objeto no hoja.  |
| 0x80072016L      | **LDAP \_ no \_ permitido \_ en \_ RDN**        | **ERROR \_ de DS no se pudo \_ \_ en \_ RDN**                | La operación no se permite en un RDN.              |
| 0x80072017L      | **\_no se \_ mods la clase de objeto \_ \_ LDAP**      | **ERROR DS no se pudo \_ \_ mod ( \_ \_ \_ clase)**        | No se puede modificar la clase de objeto.                      |
| 0x80072020L      | **\_error de operaciones LDAP \_**            | **error \_ de \_ operaciones de DS \_ error**            | Error de operación.                        |
| 0x80072021L      | **\_error de protocolo LDAP \_**              | **error \_ de \_ Protocolo de DS \_ error**              | Error de protocolo.                         |
| 0x80072022L      | **\_TIMELIMIT LDAP \_ superado**          | **ERROR de \_ DS \_ TIMELIMIT \_ superado**          | Se superó el límite de tiempo.                             |
| 0x80072023L      | **\_SIZELIMIT LDAP \_ superado**          | **ERROR de \_ DS \_ SIZELIMIT \_ superado**          | Se superó el límite de tamaño.                             |
| 0x80072024L      | **\_límite de administración LDAP \_ \_ superado**       | **se \_ \_ \_ superó el límite de administración de DS de error \_**       | Se superó el límite de administración en el servidor.     |
| 0x80072025L      | **\_comparación LDAP \_ false**               | **ERROR \_ de \_ comparación de DS \_ false**               | La comparación da como resultado **false**.                       |
| 0x80072026L      | **\_comparación LDAP \_ true**                | **ERROR \_ de \_ comparación de DS \_ true**                | La comparación da como resultado **true**.                        |
| 0x80072027L      | **\_método de autenticación LDAP \_ \_ no \_ compatible** | **\_no se \_ admite el \_ método de autenticación DS \_ de error \_** | No se admite el método de autenticación.      |
| 0x80072028L      | **se \_ \_ requiere la autenticación segura LDAP \_**       | **ERROR \_ de \_ DS \_ autenticación segura \_ requerida**       | Se requiere autenticación sólida.               |
| 0x80072029L      | **\_autenticación no adecuada de LDAP \_**          | **ERROR \_ de \_ autenticación no adecuada de DS \_**          | La autenticación no es adecuada.                 |
| 0x8007202aL      | **\_autenticación LDAP \_ desconocida**                | **ERROR \_ de \_ autenticación DS \_ desconocida**                | Se produjo un error de autenticación desconocido.           |
| 0x8007202bL      | **\_referencia LDAP**                     | **\_referencia de DS de error \_**                     | No se puede resolver la referencia.                         |
| 0x8007202cL      | **\_extensión crít no disponible LDAP \_ \_** | **ERROR \_ DS \_ \_ extensión de crít no disponible \_** | La extensión crítica no está disponible.               |
| 0x8007202dL      | **\_confidencialidad LDAP \_ requerida**    | **ERROR \_ de \_ confidencialidad de DS \_ requerido**    | La confidencialidad es obligatoria.                     |
| 0x8007202eL      | **\_coincidencia inadecuada de LDAP \_**      | **ERROR \_ de \_ coincidencia incorrecta de DS \_**      | Hubo una coincidencia inadecuada.             |
| 0x8007202fL      | **infracción de \_ restricción LDAP \_**        | **ERROR \_ de \_ infracción de restricción de DS \_**        | Se ha producido una infracción de restricción.                 |
| 0x80072030L      | **\_objeto LDAP no \_ tal \_**             | **ERROR \_ DS \_ no \_ tal \_ objeto**             | El objeto no existe.                           |
| 0x80072031L      | **\_problema de alias LDAP \_**               | **\_problema de \_ alias de DS de error \_**               | El alias no es válido.                              |
| 0x80072032L      | **\_Sintaxis DN no válida de LDAP \_ \_**          | **ERROR \_ DS \_ \_ Sintaxis DN no válida \_**          | El nombre distintivo tiene una sintaxis no válida. |
| 0x80072033L      | **LDAP \_ es \_ hoja**                     | **el ERROR de \_ DS \_ es \_ hoja**                     | El objeto es una hoja.                            |
| 0x80072034L      | **problema en el alias de LDAP \_ \_ deref \_**        | **problema de alias de DS de ERROR \_ \_ \_ deref \_**        | No se puede desreferenciar el alias.                    |
| 0x80072035L      | **LDAP \_ que no va \_ a \_ realizar**       | **ERROR \_ \_ de DS que no \_ se \_ realizará**       | El servidor no puede realizar la operación.                 |
| 0x80072036L      | **\_detección de bucle LDAP \_**                 | **ERROR \_ de \_ detección de bucle DS \_**                 | Se detectó un bucle.                               |
| 0x80072037L      | **infracción de \_ nomenclatura LDAP \_**            | **ERROR \_ de \_ infracción de nomenclatura de DS \_**            | Se produjo una infracción de nomenclatura.                    |
| 0x80072038L      | **resultados de LDAP \_ \_ demasiado \_ grandes**          | **\_los resultados del objeto DS de error son \_ \_ \_ demasiado \_ grandes**  | El conjunto de resultados es demasiado grande.                        |
| 0x80072039L      | **LDAP \_ afecta a \_ varios \_ DSA**      | **el ERROR de \_ DS \_ afecta a \_ varios \_ DSA**      | Varios agentes de servicios de directorio se ven afectados.  |
| 0x8007203aL      | **\_servidor LDAP \_ inactivo**                 | **ERROR en el \_ servidor de DS \_ \_**                 | No se puede establecer contacto con el servidor LDAP.                  |
| 0x8007203bL      | **\_error local de LDAP \_**                 | **error de \_ DS \_ local \_ error**                 | Se produjo un error local.                            |
| 0x8007203cL      | **\_error de codificación \_ LDAP**              | **error de \_ codificación de DS de error \_ \_**              | Error de codificación.                         |
| 0x8007203dL      | **\_error de descodificación LDAP \_**              | **error \_ de \_ descodificación de DS \_**              | Error de descodificación.                         |
| 0x8007203eL      | **\_error de filtro LDAP \_**                | **ERROR \_ de \_ filtro de DS \_ desconocido**              | El filtro de búsqueda es incorrecto.                        |
| 0x8007203fL      | **\_error de parámetro LDAP \_**                 | **error \_ de \_ parámetro DS de error \_**                 | Se pasó un parámetro no válido a una función.        |
| 0x80072040L      | **LDAP \_ no \_ compatible**               | **ERROR \_ DS \_ no \_ compatible**               | Característica no admitida.                           |
| 0x80072041L      | **\_no se \_ \_ DEvolvieron resultados LDAP**        | **ERROR \_ DS \_ no \_ se \_ devolvió ningún resultado**        | No se devuelven resultados.                        |
| 0x80072042L      | **\_ \_ no \_ se encontró el control LDAP**          | **\_ \_ \_ no \_ se encontró el control DS de error**          | No se encontró el control.                           |
| 0x80072043L      | **\_bucle de cliente LDAP \_**                 | **ERROR \_ de \_ bucle de cliente DS \_**                 | Se detectó un bucle de cliente.                        |
| 0x80072044L      | **se \_ \_ superó el límite de referencia LDAP \_**    | **se \_ \_ \_ superó el límite de referencia de DS \_**    | Se superó el límite de referencias.                         |



 

 

 




