---
title: Códigos de error de Win32
description: En la tabla siguiente se enumeran los mensajes de error LDAP para ADSI.
ms.assetid: b609bd56-770a-4546-8640-26ad6e108d54
ms.tgt_platform: multiple
keywords:
- Códigos de error ADSI de Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d1986b0de2e4afeed0fccdcce62851acfaf104c3f360b7ea462410f4484f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118689895"
---
# <a name="win32-error-codes"></a>Códigos de error de Win32

En la tabla siguiente se enumeran los mensajes de error LDAP para ADSI.



| Valor de error adsi | Mensaje LDAP                           | Mensaje de Win32                               | Descripción                                      |
|------------------|----------------------------------------|---------------------------------------------|--------------------------------------------------|
| 0L               | **LDAP \_ CORRECTO**                      | **NO \_ HAY NINGÚN ERROR**                               | Operación realizada correctamente.                             |
| 0x80070005L      | **DERECHOS \_ INSUFICIENTES DE LDAP \_**         | **ACCESO DE ERROR \_ \_ DENEGADO**                   | El usuario no tiene derechos de acceso suficientes.             |
| 0x80070008L      | **LDAP \_ SIN \_ MEMORIA**                   | **ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**              | El sistema está sin memoria.                         |
| 0x8007001fL      | **LDAP \_ OTHER**                        | **ERROR \_ DE GEN \_**                     | Error desconocido.                                   |
| 0x800700eaL      | **RESULTADOS \_ PARCIALES DE LDAP \_**             | **ERROR \_ MÁS \_ DATOS**                       | Resultados parciales y referencias recibidas.          |
| 0x800700eaL      | **LDAP \_ MORE \_ RESULTS \_ TO \_ RETURN**    | **ERROR \_ MÁS \_ DATOS**                       | Se devolverán más resultados.                 |
| 0x800704c7L      | **USUARIO \_ LDAP \_ CANCELADO**              | **ERROR \_ CANCELADO**                        | El usuario canceló la operación.                     |
| 0x800704c9L      | **\_ERROR DE CONEXIÓN LDAP \_**               | **ERROR \_ DE CONEXIÓN \_ RECHAZADA**              | No se puede establecer la conexión.                 |
| 0x8007052eL      | **CREDENCIALES \_ NO VÁLIDAS DE LDAP \_**         | **ERROR DE \_ INICIO DE \_ SESIÓN**                   | La credencial proporcionada no es válida.                |
| 0x800705b4L      | **TIEMPO DE ESPERA DE LDAP \_**                      | **TIEMPO DE ESPERA \_ DE ERROR**                          | Se ha pasado el tiempo de espera de la búsqueda.                                |
| 0x80071392L      | **LDAP \_ YA \_ EXISTE**              | **EL OBJETO \_ DE ERROR \_ YA \_ EXISTE**          | El objeto ya existe.                           |
| 0x8007200aL      | **LDAP \_ NO ES UN ATRIBUTO DE ESTE \_ \_ TIPO**          | **ERROR \_ DS \_ NO \_ ATTRIBUTE \_ OR \_ VALUE**     | El atributo solicitado no existe.              |
| 0x8007200bL      | **SINTAXIS \_ LDAP NO \_ VÁLIDA**              | **ERROR \_ DS \_ SINTAXIS DE \_ ATRIBUTO NO \_ VÁLIDO**   | La sintaxis no es válida.                             |
| 0x8007200cL      | **TIPO \_ LDAP SIN \_ DEFINIR**              | **ERROR \_ DS \_ ATTRIBUTE \_ TYPE \_ UNDEFINED**   | Tipo no definido.                                |
| 0x8007200dL      | **ATRIBUTO \_ LDAP O VALOR \_ \_ \_ EXISTE** | **ERROR \_ DS \_ ATTRIBUTE \_ OR \_ VALUE \_ EXISTS** | El atributo existe o se ha asignado el valor. |
| 0x8007200eL      | **LDAP \_ OCUPADO**                         | **ERROR \_ DS \_ BUSY**                         | El servidor está ocupado.                                  |
| 0x8007200fL      | **LDAP \_ NO DISPONIBLE**                  | **ERROR \_ DS \_ NO DISPONIBLE**                  | El servidor no está disponible.                         |
| 0x80072014L      | **INFRACCIÓN DE \_ CLASE \_ DE OBJETO \_ LDAP**     | **ERROR \_ DS \_ OBJ \_ CLASS \_ VIOLATION**        | Infracción de clase de objeto.                          |
| 0x80072015L      | **LDAP \_ NO PERMITIDO EN \_ \_ \_ NONLEAF**    | **ERROR \_ DS \_ CANT \_ ON \_ NON \_ LEAF**          | No se permite la operación en un objeto no hoja.  |
| 0x80072016L      | **LDAP \_ NO PERMITIDO EN \_ \_ \_ RDN**        | **ERROR \_ DS \_ CANT \_ ON \_ RDN**                | No se permite la operación en un RDN.              |
| 0x80072017L      | **LDAP \_ SIN \_ \_ MODS DE \_ CLASE DE OBJETO**      | **ERROR \_ DS \_ CANT \_ MOD \_ OBJ \_ (CLASE)**        | No se puede modificar la clase de objeto.                      |
| 0x80072020L      | **ERROR \_ DE OPERACIONES LDAP \_**            | **ERROR \_ DS \_ OPERATIONS \_ ERROR**            | Error de operación.                        |
| 0x80072021L      | **ERROR DEL PROTOCOLO LDAP \_ \_**              | **ERROR \_ DS \_ PROTOCOL \_ ERROR**              | Error de protocolo.                         |
| 0x80072022L      | **LDAP \_ TIMELIMIT \_ EXCEEDED**          | **ERROR \_ DS \_ TIMELIMIT \_ EXCEEDED**          | Se ha superado el límite de tiempo.                             |
| 0x80072023L      | **LDAP \_ SIZELIMIT \_ SUPERADO**          | **ERROR \_ DS \_ SIZELIMIT \_ EXCEEDED**          | Se ha superado el límite de tamaño.                             |
| 0x80072024L      | **SE \_ HA SUPERADO EL LÍMITE DE ADMINISTRADOR \_ \_ LDAP**       | **ERROR \_ DS \_ ADMIN \_ LIMIT \_ EXCEEDED**       | Se superó el límite de administración en el servidor.     |
| 0x80072025L      | **LDAP \_ COMPARE \_ FALSE**               | **ERROR \_ DS \_ COMPARE \_ FALSE**               | Comparar yielded **FALSE**.                       |
| 0x80072026L      | **LDAP \_ COMPARE \_ TRUE**                | **ERROR \_ DS \_ COMPARE \_ TRUE**                | Comparar el valor **TRUE cedido.**                        |
| 0x80072027L      | **NO \_ SE ADMITE EL MÉTODO DE \_ \_ AUTENTICACIÓN \_ LDAP** | **ERROR \_ NO SE ADMITE EL MÉTODO DE \_ \_ AUTENTICACIÓN \_ DE \_ DS** | No se admite el método de autenticación.      |
| 0x80072028L      | **AUTENTICACIÓN \_ SEGURA \_ LDAP \_ REQUERIDA**       | **ERROR \_ DS \_ STRONG \_ AUTH \_ REQUIRED**       | Se requiere autenticación segura.               |
| 0x80072029L      | **AUTENTICACIÓN \_ \_ INAPROPIADA DE LDAP**          | **ERROR \_ DS \_ INAPPROPRIATE \_ AUTH**          | La autenticación no es adecuada.                 |
| 0x8007202aL      | **AUTENTICACIÓN \_ LDAP \_ DESCONOCIDA**                | **ERROR \_ DS \_ AUTH \_ UNKNOWN**                | Error de autenticación desconocido.           |
| 0x8007202bL      | **REFERENCIA \_ LDAP**                     | **REFERENCIA \_ DE DS \_ DE ERROR**                     | No se puede resolver la referencia.                         |
| 0x8007202cL      | **EXTENSIÓN CRIT LDAP \_ NO \_ \_ DISPONIBLE** | **ERROR \_ DS \_ NO DISPONIBLE EXTENSIÓN \_ CRIT \_** | La extensión crítica no está disponible.               |
| 0x8007202dL      | **SE \_ REQUIERE CONFIDENCIALIDAD \_ LDAP**    | **ERROR \_ DS \_ CONFIDENTIALITY \_ REQUIRED**    | Se requiere confidencialidad.                     |
| 0x8007202eL      | **COINCIDENCIA \_ \_ INAPROPIADA DE LDAP**      | **ERROR \_ DS \_ COINCIDENCIA \_ INAPROPIADA**      | Hubo una coincidencia inapropiada.             |
| 0x8007202fL      | **INFRACCIÓN \_ DE RESTRICCIÓN \_ LDAP**        | **ERROR \_ DS \_ CONSTRAINT \_ VIOLATION**        | Hubo una infracción de restricción.                 |
| 0x80072030L      | **LDAP \_ NO ES UN OBJETO DE ESTE \_ \_ TIPO**             | **ERROR \_ DS \_ NO \_ SUCH \_ OBJECT**             | El objeto no existe.                           |
| 0x80072031L      | **PROBLEMA \_ DE ALIAS \_ LDAP**               | **ERROR \_ DS \_ ALIAS \_ PROBLEM**               | El alias no es válido.                              |
| 0x80072032L      | **SINTAXIS \_ \_ DE DN NO VÁLIDA DE LDAP \_**          | **ERROR \_ DS \_ INVALID \_ DN \_ SYNTAX**          | El nombre distintivo tiene una sintaxis que no es válida. |
| 0x80072033L      | **LDAP \_ ES \_ LEAF**                     | **ERROR \_ DS \_ ES \_ LEAF**                     | El objeto es una hoja.                            |
| 0x80072034L      | **PROBLEMA \_ DE \_ DESREFERENCIA DE ALIAS \_ LDAP**        | **ERROR \_ DS \_ ALIAS \_ DEREF \_ PROBLEM**        | No se puede desreferenciar el alias.                    |
| 0x80072035L      | **LDAP \_ NO ESTÁ DISPUESTO A \_ \_ REALIZAR**       | **ERROR \_ DS \_ NO ESTÁ DISPUESTO \_ A \_ REALIZAR**       | El servidor no puede realizar la operación.                 |
| 0x80072036L      | **DETECCIÓN \_ DE BUCLE \_ LDAP**                 | **ERROR \_ DS \_ LOOP \_ DETECT**                 | Se detectó un bucle.                               |
| 0x80072037L      | **INFRACCIÓN \_ DE NOMENCLATURA \_ LDAP**            | **ERROR \_ DS \_ NAMING \_ VIOLATION**            | Hubo una infracción de nomenclatura.                    |
| 0x80072038L      | **RESULTADOS \_ LDAP \_ DEMASIADO \_ GRANDES**          | **ERROR \_ DS \_ OBJECT \_ RESULTS \_ TOO \_ LARGE**  | El conjunto de resultados es demasiado grande.                        |
| 0x80072039L      | **LDAP \_ AFECTA A VARIAS \_ \_ DSAS**      | **EL \_ ERROR DS \_ AFECTA A VARIAS \_ \_ DSAS**      | Varios agentes de servicios de directorio se ven afectados.  |
| 0x8007203aL      | **SERVIDOR LDAP \_ \_ SIN CONEXIÓN**                 | **ERROR \_ DS \_ SERVER \_ DOWN**                 | No se puede ponerse en contacto con el servidor LDAP.                  |
| 0x8007203bL      | **LDAP \_ LOCAL \_ ERROR**                 | **ERROR \_ DS \_ LOCAL \_ ERROR**                 | Error local.                            |
| 0x8007203cL      | **ERROR DE \_ CODIFICACIÓN \_ LDAP**              | **ERROR \_ DS \_ ENCODING \_ ERROR**              | Error de codificación.                         |
| 0x8007203dL      | **\_ERROR DE DESCODING LDAP \_**              | **ERROR \_ DS \_ DECODING \_ ERROR**              | Error de decoding.                         |
| 0x8007203eL      | **\_ERROR DE FILTRO \_ LDAP**                | **ERROR \_ DS \_ FILTER \_ UNKNOWN**              | El filtro de búsqueda es malo.                        |
| 0x8007203fL      | **\_ERROR DE LDAP PARAM \_**                 | **ERROR \_ DS \_ PARAM \_ ERROR**                 | Se pasó un parámetro no válido a una función.        |
| 0x80072040L      | **LDAP \_ NO \_ COMPATIBLE**               | **ERROR \_ DS \_ NO \_ ADMITIDO**               | No se admite la característica.                           |
| 0x80072041L      | **LDAP \_ SIN \_ \_ RESULTADOS DEVUELTOS**        | **ERROR \_ DS \_ NO SE \_ \_ DEVUELVEN RESULTADOS**        | No se devuelven resultados.                        |
| 0x80072042L      | **NO \_ SE ENCONTRÓ EL CONTROL \_ \_ LDAP**          | **ERROR \_ NO SE ENCONTRÓ EL CONTROL DS \_ \_ \_**          | No se encontró el control.                           |
| 0x80072043L      | **BUCLE \_ DE CLIENTE \_ LDAP**                 | **ERROR \_ DS \_ CLIENT \_ LOOP**                 | Se detectó un bucle de cliente.                        |
| 0x80072044L      | **LÍMITE \_ DE REFERENCIAS LDAP \_ \_ SUPERADO**    | **ERROR \_ DS \_ REFERRAL \_ LIMIT \_ EXCEEDED**    | Se ha superado el límite de referencias.                         |



 

 

 




