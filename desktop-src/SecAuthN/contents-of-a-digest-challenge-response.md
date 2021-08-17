---
description: El cliente debe enviar al servidor una respuesta de desafío de resumen cuando recibe un desafío de resumen en respuesta a una solicitud de un recurso.
ms.assetid: a9a30255-a78a-41aa-9dfd-340902f4c550
title: Contenido de una respuesta de desafío de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af2a4fd199dfe9e97d69628adb0e6012bc4941929b9c1e96e00de8c42d53eba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141158"
---
# <a name="contents-of-a-digest-challenge-response"></a>Contenido de una respuesta de desafío de resumen

El cliente debe enviar al servidor una respuesta de desafío de resumen cuando recibe un desafío de resumen en respuesta a una solicitud de un recurso. El cliente debe enviar la solicitud de nuevo y proporcionar un encabezado de autorización con la respuesta de desafío. En la tabla siguiente se describen las directivas que son una respuesta de desafío implícita.



| Directiva          | Descripción                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| username           | Nombre de cuenta de la entidad [*de seguridad*](/windows/desktop/SecGloss/s-gly) que solicita el recurso.                                                                  |
| Dominio              | Nombre del dominio que contiene la cuenta indicada por nombre de usuario.                                                                                                                                                    |
| valor de seguridad              | Nonce recibido en el desafío Digest.                                                                                                                                                                                |
| uri                | Identificador de recurso universal (URI) del recurso solicitado.                                                                                                                                                         |
| qop                | Calidad [de protección](quality-of-protection.md).                                                                                                                                                                    |
| Nc                 | Recuento de nonce. Número de veces que el cliente ha enviado una respuesta de desafío mediante el nonce. Para obtener más información, vea la directiva nonce.                                                                              |
| cnonce             | Valor codificado único generado por el cliente para cada respuesta de desafío.                                                                                                                                                |
| respuesta           | Valor calculado según la especificación de acceso implícita[(RFC 2617).](https://www.ietf.org/rfc/rfc2617.txt) Una respuesta precisa es una prueba concluyente de que la contraseña del usuario se conoce en el lado cliente. |
| algoritmo          | Algoritmo recibido en el desafío Digest.                                                                                                                                                                            |
| Opaco             | Valor opaco recibido en el desafío Digest.                                                                                                                                                                         |
| Cifrado (solo SASL) | Uno de los valores de cifrado recibidos en el desafío Digest. Para obtener más información sobre el cifrado, vea [Calidad de protección y cifrado.](quality-of-protection-and-ciphers.md)                                                             |



 

Microsoft Digest admite los siguientes formularios de nombre de usuario o dominio:

-   Dominio de nombre de usuario
-   AccountName Domain (flat)
-   UPN "" (en blanco)
-   NetBIOS "" (en blanco)

Aunque se admiten caracteres en mayúsculas, para obtener un mejor rendimiento que coincida con los valores hash de digest precalculados del servidor, se recomienda el uso de caracteres en minúsculas.

El uso de hashes precalculados es una nueva característica que permite a los operadores del sistema omitir el uso de contraseñas cifradas reversibles en el controlador de dominio. Se forma un hash precalculado para un usuario cuando se cambia la contraseña del usuario.

Microsoft Digest genera la cadena de respuesta de desafío implícita para las aplicaciones cliente. Para obtener más información, consulte [Generación de la respuesta del desafío de resumen.](generating-the-digest-challenge-response.md)

 

 
