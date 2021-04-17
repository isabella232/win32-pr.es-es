---
description: No puede utilizar las funciones de copia de seguridad y restauración del Certadm.dll para realizar copias de seguridad de las claves privadas de los servicios de Certificate Server.
ms.assetid: 27ee8caa-8f5e-46dc-b55d-afde5471507e
title: Copia de seguridad y restauración de la clave privada de servicios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 891794f36e87b2aa4b6a5d5c8dde55304da20601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666537"
---
# <a name="backing-up-and-restoring-the-certificate-services-private-key"></a>Copia de seguridad y restauración de la clave privada de servicios de certificados

No puede utilizar las funciones de copia de seguridad y restauración del Certadm.dll para realizar copias de seguridad de las [*claves privadas*](../secgloss/p-gly.md)de los servicios de Certificate Server. Estas funciones no pueden realizar copias de seguridad de las claves privadas porque estas funciones están pensadas para realizar copias de seguridad y restaurar la base de datos de servicios de certificados (y los archivos relacionados), y esta base de datos no contiene ninguna clave privada (incluso para los certificados emitidos automáticamente).

Para realizar una copia de seguridad de una clave privada de servicios de servidor de certificados, use el complemento MMC entidad de certificación o el comando certutil (con-backup o-backupkey especificado). La copia de seguridad de la clave privada con el complemento MMC de la entidad de certificación o certutil hace que la clave privada se escriba en un \# archivo PKCS 12. Aunque este archivo PKCS \# 12 está protegido por contraseña, debe considerarse extremadamente sensible y debe almacenarse de forma segura; la contraseña del \# archivo PKCS 12 también debe estar protegida contra personas no autorizadas.

Del mismo modo, las funciones de copia de seguridad y restauración de servicios de Certificate Server no pueden restaurar las claves privadas. Una clave de copia de seguridad de servicios de certificado contenida en un \# archivo PKCS 12 puede ser restaurada por el complemento MMC de la entidad de certificación, o por el comando certutil (especificando los verbos-restore o-restorekey). tenga en cuenta que la persona que realiza la operación de restauración deberá conocer la contraseña del \# archivo PKCS 12.

Solo hay dos casos en los que se debe hacer una copia de seguridad de una clave privada de servicios de servidor de certificados. El primer caso es después de la instalación de servicios de Certificate Server. El segundo caso es después de cualquier operación de renovación del certificado de servicios de Certificate Server.

 

 
