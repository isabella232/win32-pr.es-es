---
title: Preguntas más frecuentes sobre EAP
description: Encuentre respuestas a las preguntas más frecuentes (p + f) sobre las API de EAP, como "¿Cuál es la duración de una autenticación de EAP?".
ms.assetid: 4e26df7b-3cce-4522-ab39-e24f06b4c4b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08713b17491d4b0bd76540c09b9d4588116256f
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "103995788"
---
# <a name="eap-frequently-asked-questions"></a>Preguntas más frecuentes sobre EAP

En el siguiente tema se proporcionan respuestas a las preguntas más frecuentes sobre las API de EAP.



| Pregunta                                                                                        | Respuesta                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ¿Cuál es la duración de una autenticación de EAP?                                                  | En una situación típica, la autenticación consiste en todo lo que ocurre entre las llamadas a las funciones [**RapEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) y [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) . Cuando un usuario decide configurar un proveedor EAP en el complemento RRAS, una autenticación consta de todo lo que ocurre entre las llamadas a los métodos [**Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize) y [**UnInitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize) .<br/> |
| ¿Qué es "Directiva de grupo"?                                                                         | Para obtener una descripción de la Directiva de grupo, vea [Directiva de grupo colección](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).                                                                                                                                                                                                                                                                                                                                                    |
| ¿Las funciones de EAP pueden invalidar la Directiva de configuración especificada por la Directiva de grupo?                      | No, nunca. Si se usa la Directiva de grupo, la configuración de directiva de grupo siempre invalidará las opciones de configuración de EAP.                                                                                                                                                                                                                                                                                                                                                         |
| Necesito avisar a los usuarios sobre los intentos de PIN no válidos. ¿Es posible capturar un código PIN no válido? | Cuando el usuario escribe un PIN incorrecto, la autenticación extensible Protocol-Transport la seguridad de la capa (EAP-TLS) enviará un código de error al solicitante de la VPN. Una vez que se devuelve un código de error, el solicitante puede implementar su lógica de reintento preferida.                                                                                                                                                                                                                    |
| ¿Qué es la seguridad de nivel de EAP-Transport (EAP-TLS)?                                                 | EAP-TLS es un protocolo cliente-servidor en el que se suelen usar perfiles de certificado distintos para el cliente y el servidor. Para obtener más información, consulte [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el protocolo de autenticación extensible](using-extenstible-authentication-protocol.md)
</dt> </dl>