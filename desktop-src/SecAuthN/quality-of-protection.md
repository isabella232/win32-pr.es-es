---
description: La calidad de protección, identificada por la Directiva qop, la especifica primero el servidor en el desafío de síntesis y, a continuación, la confirma el cliente en la respuesta de desafío.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Calidad de protección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4643c9e2de77647a3adf2cbf0441e31bcf5be5de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083188"
---
# <a name="quality-of-protection"></a>Calidad de protección

La calidad de protección, identificada por la Directiva qop, la especifica primero el servidor en el desafío de síntesis y, a continuación, la confirma el cliente en la respuesta de desafío. Si el cliente requiere una calidad de protección que el servidor no admite, el cliente debe finalizar la autenticación.

Los valores posibles de la Directiva qop se describen en la tabla siguiente.



| Value                   | Descripción                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| autenticación                  | Sólo autenticación.                                                                                                                         |
| "auth-int"              | Autenticación y comprobación de la [*integridad*](../secgloss/i-gly.md) mediante firmas.                  |
| (Solo SASL) "auth-conf" | Autenticación, integridad y comprobación de confidencialidad mediante firmas y cifrado. Para obtener más información, vea [cifrado](ciphers.md). |



 

La calidad de la protección viene determinada por las marcas de requisitos de contexto que se pasan al Microsoft Digest SSP. En la tabla siguiente se enumeran las marcas relacionadas con la calidad de la protección y el valor resultante de la Directiva qop.



| Marca                         | valor qop               |
|------------------------------|-------------------------|
| *XXX* \_ \_confidencialidad de REQ  | "auth-conf" (solo SASL) |
| *XXX* \_ detección de la reproducción de REQ \_ \_   | "auth-int"              |
| *XXX* \_ \_detección de secuencia de REQ \_ | "auth-int"              |
| *XXX* \_ integridad de REQ \_        | "auth-int"              |
| (ninguno)                       | autenticación                  |



 

> [!Note]  
> Las marcas de requisitos de contexto especificadas por las aplicaciones de servidor tienen un prefijo de ASC y las especificadas por los clientes tienen el prefijo ISC. Para determinar los valores de marca usados por la aplicación, sustituya uno de estos prefijos por *XXX*.

 

Para obtener información adicional relacionada con el servidor, consulte [generación del desafío de síntesis](generating-the-digest-challenge.md).

Para obtener información adicional relacionada con el cliente, consulte [generación de la respuesta de desafío de síntesis](generating-the-digest-challenge-response.md).

 

 
