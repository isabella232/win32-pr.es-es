---
description: No puede usar las funciones de copia Certadm.dll copia de seguridad y restauración de la base de datos para realizar una copia de seguridad de las claves privadas de Servicios de certificados.
ms.assetid: 27ee8caa-8f5e-46dc-b55d-afde5471507e
title: Copia de seguridad y restauración de la clave privada de Servicios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65b8c25e627e516d92b8dc8219db9c7933bd8d9902b1f75bea204d723edd61f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879785"
---
# <a name="backing-up-and-restoring-the-certificate-services-private-key"></a>Copia de seguridad y restauración de la clave privada de Servicios de certificados

No puede usar las funciones de copia Certadm.dll y restauración de la base de datos para realizar una copia de seguridad de las claves [*privadas de*](../secgloss/p-gly.md)Servicios de certificados . Estas funciones no pueden hacer una copia de seguridad de las claves privadas porque están diseñadas para realizar copias de seguridad y restaurar la base de datos de servicios de certificados (y los archivos relacionados), y esta base de datos no contiene ninguna clave privada (incluso para los certificados autoefirmados).

Para realizar una copia de seguridad de una clave privada de Servicios de certificado, use el complemento MMC de la entidad de certificación o el comando certutil (con -backup o -backupkey especificados). Al hacer una copia de seguridad de la clave privada con el complemento MMC de la entidad de certificación o certutil, la clave privada se escribe en el archivo PKCS \# 12. Aunque este archivo PKCS 12 está protegido con contraseña, debe considerarse extremadamente confidencial y debe almacenarse de forma segura; la contraseña del archivo PKCS 12 también debe protegerse de personas no \# \# autorizadas.

Del mismo modo, las funciones de copia de seguridad y restauración de Servicios de certificados no pueden restaurar las claves privadas. Una clave de copia de seguridad de Servicios de certificado contenida en un archivo PKCS 12 se puede restaurar mediante el complemento MMC de la entidad de certificación o mediante el comando certutil (especificando los verbos -restore o -restorekey); tenga en cuenta que la persona que realiza la operación de restauración deberá conocer la contraseña del archivo \# PKCS \# 12.

Solo hay dos casos en los que se debe realizar una copia de seguridad de una clave privada de Servicios de certificados. El primer caso es después de la instalación de Servicios de certificados. El segundo caso es después de cualquier operación de renovación del certificado de Servicios de certificados.

 

 
