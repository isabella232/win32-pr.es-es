---
title: Preguntas más frecuentes sobre EAP
description: Encuentre respuestas a las preguntas más frecuentes (P+F) sobre las API de EAP, como "¿Cuál es la duración de una autenticación EAP?".
ms.assetid: 4e26df7b-3cce-4522-ab39-e24f06b4c4b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a8b424ed195d30621c67007fc8e7d1a0882bae6ce676c70a1ca0dc93e8b846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978535"
---
# <a name="eap-frequently-asked-questions"></a>Preguntas más frecuentes sobre EAP

En el tema siguiente se proporcionan respuestas a las preguntas más frecuentes sobre las API de EAP.



| Pregunta                                                                                        | Respuesta                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ¿Cuál es la duración de una autenticación EAP?                                                  | En una situación típica, la autenticación consta de todo lo que ocurre entre llamar a las [**funciones RapEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) y [**RasEapEnd.**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) Cuando un usuario decide configurar un proveedor de EAP en el complemento RRAS, una autenticación consta de todo lo que ocurre entre llamar a los métodos [**Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize) y [**Uninitialize.**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize)<br/> |
| ¿Qué es la "directiva de grupo"?                                                                         | Para obtener una descripción de la directiva de grupo, [vea directiva de grupo Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).                                                                                                                                                                                                                                                                                                                                                    |
| ¿Pueden las funciones de EAP invalidar la directiva de configuración especificada por la directiva de grupo?                      | No, nunca. Si la directiva de grupo está en uso, la configuración de directiva de grupo siempre invalidará las opciones de configuración de EAP.                                                                                                                                                                                                                                                                                                                                                         |
| Necesito advertir a los usuarios sobre intentos de PIN no válidos. ¿Es posible capturar un código pin no válido? | Cuando el usuario escribe el PIN incorrecto, la autenticación extensible Protocol-Transport Layer Security (EAP-TLS) enviará códigos de error al proveedor de VPN. Una vez que se devuelve un código de error, el suplicante puede implementar su lógica de reintento preferida.                                                                                                                                                                                                                    |
| ¿Qué es EAP-Transport seguridad de nivel de usuario (EAP-TLS)?                                                 | EAP-TLS es un protocolo cliente-servidor en el que normalmente se usan perfiles de certificado distintos para el cliente y el servidor. Para obtener más información, [vea IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del protocolo de autenticación extensible](using-extenstible-authentication-protocol.md)
</dt> </dl>