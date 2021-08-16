---
description: Explica cómo crear una solicitud de certificado y recibir y almacenar el certificado devuelto en un almacén de certificados.
ms.assetid: 4ca3d6cb-6ce7-4408-9258-6e40c8219dc0
title: Uso del control de inscripción de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d489edb7ed288ffc0b51d039c6c32df90631b833d491567729f075c1cee9cae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971762"
---
# <a name="using-certificate-enrollment-control"></a>Uso del control de inscripción de certificados

El Control de inscripción de certificados es un objeto único con muchas propiedades y varios métodos que se pueden usar para determinar cómo procesa el control de inscripción de certificados la información del usuario, el tipo de certificado que se va a solicitar, cómo se van a generar las claves, dónde se va a almacenar el certificado y los procesos relacionados. Hay dos usos principales del control de [](../secgloss/c-gly.md) inscripción de certificados: para crear una solicitud de certificado (PKCS 10) y para recibir el certificado devuelto y almacenarlo en un almacén \# [*de certificados*](../secgloss/c-gly.md). Para obtener detalles y sintaxis para crear una instancia del objeto Control de inscripción de certificados, establecer sus propiedades y usar sus métodos, vea los temas siguientes.



| Information                                                                                                                                                                                           | Tema                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Creación de una instancia del objeto Control de inscripción de certificados en distintos lenguajes de programación                                                                                                  | [Crear una instancia del objeto de control de inscripción de certificados](creating-an-instance-of-the-certificate-enrollment-control-object.md) |
| Uso de propiedades de Control de inscripción de certificados en distintos lenguajes de programación                                                                                                                    | [Uso de las propiedades del control de inscripción de certificados](using-the-certificate-enrollment-control-properties.md)                             |
| Recopilar la información necesaria y enviar una solicitud [*de certificado*](../secgloss/c-gly.md) en distintos lenguajes de programación. | [Creación de la solicitud de certificado](creating-the-certificate-request.md)                                                                   |
| Extracción y almacenamiento del certificado completado                                                                                                                                                      | [Recepción del certificado devuelto](receiving-the-returned-certificate.md)                                                               |
| Recuperación de información de valores devueltos en distintos idiomas                                                                                                                                      | [Valores devueltos del método](method-return-values.md)                                                                                           |
| Comprobación de errores                                                                                                                                                                                   | [Comprobación de errores](error-checking.md)                                                                                                       |



 

 

 
