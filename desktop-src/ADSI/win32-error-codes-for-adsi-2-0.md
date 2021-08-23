---
title: Códigos de error de Win32 para ADSI 2.0
description: En la tabla siguiente se enumeran los mensajes de error LDAP para ADSI 2.0.
ms.assetid: 99d97ea8-1dcc-49f4-a2bf-36ff8076e83a
ms.tgt_platform: multiple
keywords:
- Códigos de error de Win32 para ADSI 2.0 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea81b4d277ad43cb2278d23549e370df1d11b3058be1e9c8b0f8b9329eabe26e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589755"
---
# <a name="win32-error-codes-for-adsi-20"></a>Códigos de error de Win32 para ADSI 2.0

En la tabla siguiente se enumeran los mensajes de error LDAP para ADSI 2.0.



| Valor de error adsi | Mensaje LDAP                           | Mensaje de Win32                        | Descripción                                          |
|------------------|----------------------------------------|--------------------------------------|------------------------------------------------------|
| 0                | **LDAP \_ SUCCESS**                      | **NO \_ ERROR**                        | Operación realizada correctamente.                                 |
| 0x80070002       | **LDAP \_ NO ES UN OBJETO DE ESTE \_ \_ TIPO**             | **ARCHIVO \_ DE ERROR NO \_ \_ ENCONTRADO**          | El objeto no existe.                               |
| 0x80070005       | **NO \_ SE ADMITE EL MÉTODO DE \_ \_ AUTENTICACIÓN \_ LDAP** | **ERROR \_ DE ACCESO \_ DENEGADO**            | No se admite el método de autenticación.                 |
| 0x80070005       | **AUTENTICACIÓN \_ SEGURA \_ LDAP \_ REQUERIDA**       | **ERROR \_ DE ACCESO \_ DENEGADO**            | Requiere autenticación segura.                      |
| 0x80070005       | **AUTENTICACIÓN \_ \_ INAPROPIADA DE LDAP**          | **ERROR \_ DE ACCESO \_ DENEGADO**            | Autenticación inapropiada.                        |
| 0x80070005       | **DERECHOS \_ INSUFICIENTES DE LDAP \_**         | **ERROR \_ DE ACCESO \_ DENEGADO**            | El usuario no tiene derechos de acceso suficientes.                 |
| 0x80070005       | **AUTENTICACIÓN \_ LDAP \_ DESCONOCIDA**                | **ERROR \_ DE ACCESO \_ DENEGADO**            | Error de autenticación desconocido.               |
| 0x80070008       | **LDAP \_ NO \_ MEMORY**                   | **ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**       | El sistema está sin memoria.                             |
| 0x8007001F       | **LDAP \_ OTHER**                        | **ERROR \_ DE GEN \_**              | Error desconocido.                              |
| 0x8007001F       | **LDAP \_ LOCAL \_ ERROR**                 | **ERROR \_ DE GEN \_**              | Error local.                                |
| 0x80070037       | **LDAP \_ NO DISPONIBLE**                  | **ERROR \_ DEV \_ NOT \_ EXIST**           | El servidor no está disponible.                             |
| 0x8007003A       | **SERVIDOR LDAP \_ \_ SIN CONEXIÓN**                 | **ERROR \_ BAD \_ NET \_ RESP**            | No se puede ponerse en contacto con el servidor LDAP.                      |
| 0x8007003B       | **ERROR DE \_ CODIFICACIÓN \_ LDAP**              | **ERROR \_ UNEXP \_ NET \_ ERR**           | Error de codificación.                             |
| 0x8007003B       | **\_ERROR DE DESCODING LDAP \_**              | **ERROR \_ UNEXP \_ NET \_ ERR**           | Error de decoding.                             |
| 0x80070044       | **SE \_ HA SUPERADO EL LÍMITE DE ADMINISTRADOR \_ \_ LDAP**       | **ERROR \_ \_ DEMASIADOS \_ NOMBRES**          | Se superó el límite de administración en el servidor.         |
| 0x80070056       | **CREDENCIALES \_ NO VÁLIDAS DE LDAP \_**         | **ERROR \_ CONTRASEÑA NO \_ VÁLIDA**         | Credencial no válida.                                |
| 0x80070057       | **SINTAXIS \_ \_ DE DN NO VÁLIDA DE LDAP \_**          | **ERROR \_ PARÁMETRO NO \_ VÁLIDO**        | El nombre distintivo tiene una sintaxis que no es válida.     |
| 0x80070057       | **INFRACCIÓN \_ DE NOMENCLATURA \_ LDAP**            | **ERROR \_ PARÁMETRO NO \_ VÁLIDO**        | Infracción de nomenclatura.                                    |
| 0x80070057       | **INFRACCIÓN \_ DE CLASE DE OBJETO \_ \_ LDAP**     | **ERROR \_ PARÁMETRO NO \_ VÁLIDO**        | Infracción de clase de objeto.                              |
| 0x80070057       | **\_ERROR DE FILTRO \_ LDAP**                | **ERROR \_ PARÁMETRO NO \_ VÁLIDO**        | El filtro de búsqueda es malo.                                |
| 0x80070057       | **\_ERROR DE LDAP PARAM \_**                 | **ERROR \_ PARÁMETRO NO \_ VÁLIDO**        | Se pasó un parámetro no válido a una rutina.               |
| 0X8007006E       | **ERROR \_ DE OPERACIONES LDAP \_**            | **ERROR \_ AL ABRIR \_ ERROR**              | Error de operación.                            |
| 0x8007007A       | **RESULTADOS \_ LDAP \_ DEMASIADO \_ GRANDES**          | **ERROR \_ BÚFER \_ INSUFICIENTE**      | El conjunto de resultados es demasiado grande.                            |
| 0x8007007B       | **SINTAXIS \_ LDAP NO \_ VÁLIDA**              | **ERROR \_ NOMBRE NO \_ VÁLIDO**             | Sintaxis no válida.                                    |
| 0x8007007C       | **ERROR DEL PROTOCOLO LDAP \_ \_**              | **ERROR \_ NIVEL NO \_ VÁLIDO**            | Error de protocolo.                                      |
| 0x800700B7       | **LDAP \_ YA \_ EXISTE**              | **EL ERROR \_ YA \_ EXISTE**           | El objeto ya existe.                               |
| 0x800700EA       | **RESULTADOS \_ PARCIALES DE LDAP \_**             | **ERROR \_ MÁS \_ DATOS**                | Resultados parciales y referencias recibidas.              |
| 0x800700EA       | **LDAP \_ OCUPADO**                         | **ERROR \_ OCUPADO**                      | El servidor está ocupado.                                      |
| 0x800703EB       | **LDAP \_ NO ESTÁ DISPUESTO A \_ \_ REALIZAR**       | **ERROR \_ NO SE PUEDE \_ \_ COMPLETAR**        | El servidor no puede realizar la operación.                     |
| 0x8007041D       | **TIEMPO DE ESPERA DE LDAP \_**                      | **TIEMPO DE ESPERA \_ DE SOLICITUD DEL SERVICIO DE \_ \_ ERROR** | Se ha pasado el tiempo de espera de la búsqueda.                                    |
| 0x800704B8       | **LDAP \_ COMPARE \_ FALSE**               | **ERROR \_ EXTENDIDO \_ ERROR**           | Compare yielded **FALSE**.                           |
| 0x800704B8       | **LDAP \_ COMPARE \_ TRUE**                | **ERROR \_ EXTENDIDO \_ ERROR**           | Compare el valor true que se **ha dado.**                            |
| 0x800704B8       | **REFERENCIA \_ LDAP**                     | **ERROR \_ EXTENDIDO \_ ERROR**           | No se puede resolver la referencia.                             |
| 0x800704B8       | **EXTENSIÓN CRIT LDAP \_ NO \_ \_ DISPONIBLE** | **ERROR \_ EXTENDIDO \_ ERROR**           | La extensión crítica no está disponible.                   |
| 0x800704B8       | **LDAP \_ NO ES UN ATRIBUTO DE ESTE \_ \_ TIPO**          | **ERROR \_ EXTENDIDO \_ ERROR**           | El atributo solicitado no existe.                  |
| 0x800704B8       | **TIPO \_ LDAP NO \_ DEFINIDO**              | **ERROR \_ EXTENDIDO \_ ERROR**           | El tipo no está definido.                                 |
| 0x800704B8       | **COINCIDENCIA \_ \_ INAPROPIADA DE LDAP**      | **ERROR \_ EXTENDIDO \_ ERROR**           | Hubo una coincidencia inapropiada.                 |
| 0x800704B8       | **INFRACCIÓN \_ DE RESTRICCIÓN \_ LDAP**        | **ERROR \_ EXTENDIDO \_ ERROR**           | Hubo una infracción de restricción.                     |
| 0x800704B8       | **ATRIBUTO \_ LDAP O VALOR \_ \_ \_ EXISTE** | **ERROR \_ EXTENDIDO \_ ERROR**           | El atributo existe o el valor se ha asignado. |
| 0x800704B8       | **PROBLEMA \_ DE ALIAS \_ LDAP**               | **ERROR \_ EXTENDIDO \_ ERROR**           | El alias no es válido.                                  |
| 0x800704B8       | **LDAP \_ ES \_ HOJA**                     | **ERROR \_ EXTENDIDO \_ ERROR**           | El objeto es una hoja.                                    |
| 0x800704B8       | **PROBLEMA \_ DE DEREF DE ALIAS \_ \_ LDAP**        | **ERROR \_ EXTENDIDO \_ ERROR**           | No se puede desreferenciar el alias.                        |
| 0x800704B8       | **DETECCIÓN \_ DE BUCLE \_ LDAP**                 | **ERROR \_ EXTENDIDO \_ ERROR**           | Se detectó un bucle.                                   |
| 0x800704B8       | **LDAP \_ NO PERMITIDO EN \_ \_ \_ NONLEAF**    | **ERROR \_ EXTENDIDO \_ ERROR**           | No se permite la operación en un objeto no hoja.       |
| 0x800704B8       | **LDAP \_ NO PERMITIDO EN \_ \_ \_ RDN**        | **ERROR \_ EXTENDIDO \_ ERROR**           | No se permite la operación en RDN.                     |
| 0x800704B8       | **LDAP \_ SIN \_ \_ MODS DE \_ CLASE DE OBJETO**      | **ERROR \_ EXTENDIDO \_ ERROR**           | No se puede modificar la clase de objeto.                          |
| 0x800704B8       | **LDAP \_ AFECTA A VARIAS \_ \_ DSAS**      | **ERROR \_ EXTENDIDO \_ ERROR**           | Varios agentes de servicios de directorio se ven afectados.      |
| 0x800704C7       | **USUARIO \_ LDAP \_ CANCELADO**              | **ERROR \_ CANCELADO**                 | El usuario ha cancelado la operación.                     |
| 0x80070718       | **LDAP \_ TIMELIMIT \_ EXCEEDED**          | **ERROR \_ NO HAY SUFICIENTE \_ \_ CUOTA**        | Se ha superado el límite de tiempo.                                 |
| 0x80070718       | **LDAP \_ SIZELIMIT \_ SUPERADO**          | **ERROR \_ NO HAY SUFICIENTE \_ \_ CUOTA**        | Se ha superado el límite de tamaño.                                 |



 

En ADSI 2.0, varios mensajes de error LDAP se asignan a un código de error de Win32 como **ERROR \_ EXTENDED \_ ERROR**. Llame [**a ADsGetLastError para**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) recuperar la cadena de error devuelta por el servidor. Para obtener más información, vea [ADSI Extended Error Messages (Mensajes de error extendidos adsi)](adsi-extended-error-messages.md) a continuación.

 

 




