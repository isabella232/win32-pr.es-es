---
description: Un contexto de seguridad es el conjunto de atributos y reglas de seguridad en vigor durante una sesión de comunicación.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Semántica de contexto de SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423ce097d1ab71cf50983285f3ca8731497ed5a9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482541"
---
# <a name="sspi-context-semantics"></a>Semántica de contexto de SSPI

Un [*contexto de seguridad*](../secgloss/s-gly.md) es el conjunto de atributos y reglas de seguridad en vigor durante una sesión de comunicación. Esto incluye información como las identidades de la entidad de seguridad e información sobre las claves, cifrados y algoritmos que se usan. Para [*la*](../secgloss/s-gly.md) interfaz del proveedor de compatibilidad de seguridad (SSPI), un contexto de seguridad es una estructura opaca que se crea a través de un intercambio que implica la función [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) y la [**función AcceptSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)

Para obtener más información sobre los atributos de contexto, vea [Requisitos de contexto](context-requirements.md).

El modelo SSPI admite tres tipos de contextos de seguridad.




| Tipo | Descripción | 
|------|-------------|
| <a href="connection-oriented-contexts.md">Connection</a> | Un contexto orientado a la <a href="/windows/desktop/SecGloss/c-gly"><em>conexión</em></a> es el contexto de seguridad más común y el más sencillo de usar. El autor de la llamada es responsable del formato general del mensaje y de la ubicación de los datos del mensaje. El autor de la llamada también es responsable de la ubicación de los campos pertinentes para la seguridad dentro de un mensaje, como la ubicación de los datos de firma.<br /> | 
| <a href="datagram-contexts.md">Datagrama</a> | Un <a href="/windows/desktop/SecGloss/d-gly"><em>contexto orientado a</em></a>datagramas tiene compatibilidad adicional para la comunicación de datagramas de estilo DCE. También se puede usar genéricamente para una aplicación de transporte orientada a datagramas.<br /><blockquote><p>[!Important]</p><p>El <a href="microsoft-kerberos.md">paquete de Microsoft Kerberos</a> no admite contextos de datagramas en modo de usuario a usuario.<br /></p></blockquote><br /> | 
| <a href="stream-contexts.md">Stream</a> | Un contexto orientado a secuencias es responsable del bloqueo y el formato de los mensajes dentro del paquete de seguridad. El autor de la llamada no está interesado en el formato, sino en un flujo de datos sin procesar.<br /> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Requisitos de contexto](context-requirements.md)
</dt> <dt>

[Contextos orientados a la conexión](connection-oriented-contexts.md)
</dt> <dt>

[Contextos de datagrama](datagram-contexts.md)
</dt> <dt>

[Contextos de secuencia](stream-contexts.md)
</dt> </dl>

 

 
