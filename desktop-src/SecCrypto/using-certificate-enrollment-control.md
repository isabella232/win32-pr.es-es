---
description: Explica cómo crear una solicitud de certificado y recibir y almacenar el certificado devuelto en un almacén de certificados.
ms.assetid: 4ca3d6cb-6ce7-4408-9258-6e40c8219dc0
title: Usar el control de inscripción de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac3da319571b164fe66eb5bb3ac647c2978fff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666725"
---
# <a name="using-certificate-enrollment-control"></a>Usar el control de inscripción de certificados

El control de inscripción de certificados es un objeto único con muchas propiedades y varios métodos que se pueden usar para determinar cómo el control de inscripción de certificados procesa la información del usuario, el tipo de certificado que se va a solicitar, cómo se deben generar las claves, dónde se almacenará el certificado y los procesos relacionados. Hay dos usos principales del control de inscripción de certificados: para crear una [*solicitud de certificado*](../secgloss/c-gly.md) (PKCS \# 10) y para recibir el certificado devuelto y almacenarlo en un [*almacén de certificados*](../secgloss/c-gly.md). Para obtener información detallada y la sintaxis para crear una instancia del objeto de control de inscripción de certificados, establecer sus propiedades y usar sus métodos, vea los temas siguientes.



| Información                                                                                                                                                                                           | Tema                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Crear una instancia del objeto de control de inscripción de certificados en diferentes lenguajes de programación                                                                                                  | [Crear una instancia del objeto de control de inscripción de certificados](creating-an-instance-of-the-certificate-enrollment-control-object.md) |
| Usar las propiedades de control de inscripción de certificados en diferentes lenguajes de programación                                                                                                                    | [Uso de las propiedades de control de inscripción de certificados](using-the-certificate-enrollment-control-properties.md)                             |
| Recopilar la información necesaria y enviar una [*solicitud de certificado*](../secgloss/c-gly.md) en diferentes lenguajes de programación. | [Crear la solicitud de certificado](creating-the-certificate-request.md)                                                                   |
| Extracción y almacenamiento del certificado completado                                                                                                                                                      | [Recibir el certificado devuelto](receiving-the-returned-certificate.md)                                                               |
| Recuperar información de valores devueltos en diferentes idiomas                                                                                                                                      | [Valores devueltos del método](method-return-values.md)                                                                                           |
| Comprobar errores                                                                                                                                                                                   | [Comprobación de errores](error-checking.md)                                                                                                       |



 

 

 
