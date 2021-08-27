---
description: A veces, un mensaje firmado requiere una contrafirma.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Contrasignatures de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d95f9d082a2814501bdb948d1bfebdc5c2699012446c5189c5c3fc18612c1ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080645"
---
# <a name="message-countersignatures"></a>Contrasignatures de mensajes

A veces, un mensaje firmado requiere [*una contrafirma*](../secgloss/c-gly.md). Por ejemplo, el usuario A puede enviar un mensaje de datos firmados al usuario B, esperando que B confirme el acuerdo con los términos contenidos en el documento. El usuario B descodifica el mensaje, lee los términos y, si está de acuerdo, contrarreste el mensaje. A continuación, el mensaje con contrascargo se envía de vuelta al usuario A. El usuario A ahora sabe y puede demostrar que el usuario B aceptó los términos.

En la tabla siguiente se enumeran las secciones que contienen descripciones de procedimientos o ejemplos de programa de C de contrasignación de mensajes.



| Sección                                                                                                                                 | Contenido                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Funciones de mensajes](cryptography-functions.md)                                                                       | Enumera las funciones de firma de contador.                             |
| [Contrasignar un mensaje](countersigning-a-message.md)                                                                                | Detalla el proceso de firma de un mensaje en el contador.                  |
| [Comprobación de una contrasignación](verifying-a-countersignature.md)                                                                        | Detalla el procedimiento para comprobar una firma de contador.           |
| [Comprobar un mensaje firmado](verifying-a-signed-message.md)                                                                            | Detalla un proceso para comprobar la firma en un mensaje firmado. |
| [Programa C de ejemplo: codificación y codificación de un mensaje counterSigned](example-c-program-encoding-and-decoding-a-countersigned-message.md) | Programa de C de ejemplo que codifica y descodifica un mensaje con contrasignación. |



 

 

 
