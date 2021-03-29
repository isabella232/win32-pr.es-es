---
description: A veces, un mensaje firmado requiere una contrafirma.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Contrafirmas de mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8dff2920217dd9a79f917f7b625da3919747d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810244"
---
# <a name="message-countersignatures"></a>Contrafirmas de mensaje

A veces, un mensaje firmado requiere una [*contrafirma*](../secgloss/c-gly.md). Por ejemplo, el usuario A puede enviar un mensaje de datos firmados al usuario B, esperando que B confirme el acuerdo con los términos contenidos en el documento. El usuario B descodifica el mensaje, Lee los términos y, si está en acuerdo, contrafirma el mensaje. A continuación, el mensaje con firma se devuelve al usuario a. el usuario A ahora sabe y puede demostrar que el usuario B aceptó los términos.

En la tabla siguiente se muestran las secciones que contienen descripciones de procedimientos o ejemplos de programas de C de contrafirma de mensajes.



| Sección                                                                                                                                 | Contenido                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Funciones de mensajes](cryptography-functions.md)                                                                       | Enumera las funciones de firma de contadores.                             |
| [Contrafirmar un mensaje](countersigning-a-message.md)                                                                                | Detalla el proceso de firma de un mensaje.                  |
| [Comprobar una contrafirma](verifying-a-countersignature.md)                                                                        | Detalla el procedimiento para comprobar una firma de contador.           |
| [Comprobación de un mensaje firmado](verifying-a-signed-message.md)                                                                            | Detalla un proceso para comprobar la firma de un mensaje firmado. |
| [Programa C de ejemplo: codificar y descodificar un mensaje con signo](example-c-program-encoding-and-decoding-a-countersigned-message.md) | Programa de ejemplo C que codifica y descodifica un mensaje con signo. |



 

 

 
