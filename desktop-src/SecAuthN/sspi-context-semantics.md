---
description: Un contexto de seguridad es el conjunto de reglas y atributos de seguridad en vigor durante una sesión de comunicación.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Semántica de contexto SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcb604e09b1a2458ef05204aefbe754af26b210
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652931"
---
# <a name="sspi-context-semantics"></a>Semántica de contexto SSPI

Un [*contexto de seguridad*](../secgloss/s-gly.md) es el conjunto de reglas y atributos de seguridad en vigor durante una sesión de comunicación. Esto incluye información como las identidades de la entidad de seguridad e información sobre las claves, los cifrados y los algoritmos que se usan. Para la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI), un contexto de seguridad es una estructura opaca que se crea a través de un intercambio que implica la función [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) y la función [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .

Para obtener más información sobre los atributos de contexto, vea [requisitos de contexto](context-requirements.md).

El modelo SSPI admite tres tipos de contextos de seguridad.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="connection-oriented-contexts.md">Connection</a></td>
<td>Un <a href="/windows/desktop/SecGloss/c-gly"><em>contexto</em></a> orientado a la conexión es el contexto de seguridad más común y el más sencillo de usar. El autor de la llamada es responsable del formato de mensaje general y de la ubicación de los datos en el mensaje. El autor de la llamada también es responsable de la ubicación de los campos relevantes para la seguridad dentro de un mensaje, como la ubicación de los datos de la firma.<br/></td>
</tr>
<tr class="even">
<td><a href="datagram-contexts.md">Datagrama</a></td>
<td>Un contexto orientado a <a href="/windows/desktop/SecGloss/d-gly"><em>datagramas</em></a>tiene compatibilidad adicional para la comunicación de datagramas de estilo DCE. También se puede utilizar de forma genérica para una aplicación de transporte orientada a datagramas.<br/>
<blockquote>
<p>[!Important]</p>
<p>El paquete de <a href="microsoft-kerberos.md">Microsoft Kerberos</a> no admite contextos de datagramas en modo de usuario a usuario.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="stream-contexts.md">Stream</a></td>
<td>Un contexto orientado a secuencias es responsable del bloqueo y el formato de los mensajes en el paquete de seguridad. El autor de la llamada no está interesado en dar formato, sino en una secuencia de datos sin formato.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Requisitos de contexto](context-requirements.md)
</dt> <dt>

[Contextos orientados a conexiones](connection-oriented-contexts.md)
</dt> <dt>

[Contextos de datagramas](datagram-contexts.md)
</dt> <dt>

[Contextos de secuencia](stream-contexts.md)
</dt> </dl>

 

 
