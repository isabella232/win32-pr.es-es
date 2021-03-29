---
description: El cliente debe enviar al servidor una respuesta de desafío de síntesis cuando recibe un desafío de síntesis en respuesta a una solicitud de un recurso.
ms.assetid: a9a30255-a78a-41aa-9dfd-340902f4c550
title: Contenido de una respuesta de desafío de síntesis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7168a7e6a468ecc7d573ef0bd853ec6db255b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277345"
---
# <a name="contents-of-a-digest-challenge-response"></a>Contenido de una respuesta de desafío de síntesis

El cliente debe enviar al servidor una respuesta de desafío de síntesis cuando recibe un desafío de síntesis en respuesta a una solicitud de un recurso. El cliente debe volver a enviar la solicitud, proporcionando un encabezado de autorización con la respuesta de desafío. En la tabla siguiente se describen las directivas que componen una respuesta de desafío de síntesis.



| Directiva          | Descripción                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| username           | El nombre de la cuenta de la [*entidad de seguridad*](/windows/desktop/SecGloss/s-gly) que solicita el recurso.                                                                  |
| Dominio              | Nombre del dominio que contiene la cuenta indicada por el nombre de usuario.                                                                                                                                                    |
| valor de seguridad              | El nonce recibido en el desafío de síntesis.                                                                                                                                                                                |
| uri                | Identificador de recursos universal (URI) del recurso solicitado.                                                                                                                                                         |
| qop                | [Calidad de la protección](quality-of-protection.md).                                                                                                                                                                    |
| NC                 | Recuento de nonce. Número de veces que el cliente ha enviado una respuesta de desafío mediante el valor de seguridad (nonce). Para obtener más información, vea la Directiva nonce.                                                                              |
| cnonce             | Valor codificado único generado por el cliente para cada respuesta de desafío.                                                                                                                                                |
| respuesta           | Un valor calculado según la especificación de acceso implícita ([RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)). Una respuesta precisa es una prueba concluyente de que la contraseña del usuario se conoce en el lado del cliente. |
| algoritmo          | Algoritmo recibido en el desafío de síntesis.                                                                                                                                                                            |
| opaco             | Valor opaco recibido en el desafío de síntesis.                                                                                                                                                                         |
| Cifrado (solo SASL) | Uno de los valores de cifrado recibidos en el desafío de síntesis. Para obtener información detallada sobre el cifrado, consulte [calidad de protección y cifrado](quality-of-protection-and-ciphers.md).                                                             |



 

Microsoft Digest admite los siguientes formatos de nombre de usuario y dominio Kerberos:

-   Dominio de nombre de usuario
-   Dominio AccountName (plano)
-   UPN "" (en blanco)
-   NetBIOS "" (en blanco)

Aunque se admiten caracteres en mayúsculas, para obtener el mejor rendimiento que coincida con los valores hash de Resumen precalculados del servidor, se recomienda el uso de caracteres en minúsculas.

El uso de hashes precalculados es una nueva característica que permite a los operadores del sistema omitir el uso de contraseñas cifradas reversibles en el controlador de dominio. Un hash precalculado está formado por un usuario cuando se cambia la contraseña del usuario.

Microsoft Digest genera la cadena de respuesta de desafío de síntesis para las aplicaciones cliente. Para obtener más información, consulte [generación de la respuesta de desafío de síntesis](generating-the-digest-challenge-response.md).

 

 
