---
description: Un contexto de seguridad es el conjunto de atributos y reglas de seguridad en vigor durante una sesión de comunicación.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Semántica de contexto de SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddadd2c8a76f1fdc151273dca2027b8cb55776a50b78a7c08343c22410ae90e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916984"
---
# <a name="sspi-context-semantics"></a>Semántica de contexto de SSPI

Un [*contexto de seguridad*](../secgloss/s-gly.md) es el conjunto de atributos y reglas de seguridad en vigor durante una sesión de comunicación. Esto incluye información como las identidades de la entidad de seguridad y la información sobre las claves, los cifrados y los algoritmos que se usan. Para [*security support provider interface*](../secgloss/s-gly.md) (SSPI), un contexto de seguridad es una estructura opaca que se crea a través de un intercambio que implica la función [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) y la [**función AcceptSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)

Para obtener más información sobre los atributos de contexto, vea [Requisitos de contexto.](context-requirements.md)

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
<td>Un contexto orientado a la <a href="/windows/desktop/SecGloss/c-gly"><em>conexión</em></a> es el contexto de seguridad más común y el más sencillo de usar. El autor de la llamada es responsable del formato general del mensaje y de la ubicación de los datos en el mensaje. El autor de la llamada también es responsable de la ubicación de los campos pertinentes para la seguridad dentro de un mensaje, como la ubicación de los datos de firma.<br/></td>
</tr>
<tr class="even">
<td><a href="datagram-contexts.md">Datagrama</a></td>
<td>Un <a href="/windows/desktop/SecGloss/d-gly"><em>contexto orientado a</em></a>datagramas tiene compatibilidad adicional con la comunicación de datagramas de estilo DCE. También se puede usar genéricamente para una aplicación de transporte orientada a datagramas.<br/>
<blockquote>
<p>[!Important]</p>
<p>El <a href="microsoft-kerberos.md">paquete kerberos</a> de Microsoft no admite contextos de datagramas en modo de usuario a usuario.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="stream-contexts.md">Stream</a></td>
<td>Un contexto orientado a secuencias es responsable del bloqueo y el formato de los mensajes dentro del paquete de seguridad. El autor de la llamada no está interesado en dar formato, sino en un flujo de datos sin procesar.<br/></td>
</tr>
</tbody>
</table>



 

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

 

 
