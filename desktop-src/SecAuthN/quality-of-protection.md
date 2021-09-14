---
description: La calidad de protección, identificada por la directiva qop, la especifica primero el servidor en el desafío Digest y, a continuación, la confirma el cliente en la respuesta del desafío.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Calidad de protección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4643c9e2de77647a3adf2cbf0441e31bcf5be5de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253671"
---
# <a name="quality-of-protection"></a>Calidad de protección

La calidad de protección, identificada por la directiva qop, la especifica primero el servidor en el desafío Digest y, a continuación, la confirma el cliente en la respuesta del desafío. Si el cliente requiere una calidad de protección que el servidor no admite, el cliente debe finalizar la autenticación.

Los valores posibles de la directiva qop se describen en la tabla siguiente.



| Value                   | Descripción                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| "auth"                  | Sólo autenticación.                                                                                                                         |
| "auth-int"              | Comprobación de [*la autenticación y*](../secgloss/i-gly.md) la integridad mediante firmas.                  |
| (solo SASL) "auth-conf" | Comprobación de autenticación, integridad y confidencialidad mediante firmas y cifrado. Para obtener más información, vea [Ciphers](ciphers.md). |



 

La calidad de protección viene determinada por las marcas de requisitos de contexto que se pasan al Microsoft Digest SSP. En la tabla siguiente se enumeran las marcas relacionadas con la calidad de protección y el valor resultante de la directiva qop.



| Marca                         | Valor de qop               |
|------------------------------|-------------------------|
| *XXX* \_ CONFIDENCIALIDAD DE REQ \_  | "auth-conf" (solo SASL) |
| *XXX* \_ REQ \_ REPLAY \_ DETECT   | "auth-int"              |
| *XXX* \_ REQ \_ SEQUENCE \_ DETECT | "auth-int"              |
| *XXX* \_ INTEGRIDAD \_ DE REQ        | "auth-int"              |
| (ninguno)                       | "auth"                  |



 

> [!Note]  
> Las marcas de requisitos de contexto especificadas por las aplicaciones de servidor tienen un prefijo de ASC y las especificadas por los clientes tienen el prefijo ISC. Para determinar los valores de marca utilizados por la aplicación, sustituya uno de estos prefijos por *XXX.*

 

Para obtener información adicional relacionada con el servidor, vea [Generating the Digest Challenge](generating-the-digest-challenge.md).

Para obtener información adicional relacionada con el cliente, vea [Generating the Digest Challenge Response](generating-the-digest-challenge-response.md).

 

 
