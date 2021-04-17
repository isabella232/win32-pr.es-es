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
# <a name="sspi-context-semantics"></a><span data-ttu-id="a4021-103">Semántica de contexto SSPI</span><span class="sxs-lookup"><span data-stu-id="a4021-103">SSPI Context Semantics</span></span>

<span data-ttu-id="a4021-104">Un [*contexto de seguridad*](../secgloss/s-gly.md) es el conjunto de reglas y atributos de seguridad en vigor durante una sesión de comunicación.</span><span class="sxs-lookup"><span data-stu-id="a4021-104">A [*security context*](../secgloss/s-gly.md) is the set of security attributes and rules in effect during a communication session.</span></span> <span data-ttu-id="a4021-105">Esto incluye información como las identidades de la entidad de seguridad e información sobre las claves, los cifrados y los algoritmos que se usan.</span><span class="sxs-lookup"><span data-stu-id="a4021-105">This includes such information as the identities of the principal and information on the keys, ciphers, and algorithms being used.</span></span> <span data-ttu-id="a4021-106">Para la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI), un contexto de seguridad es una estructura opaca que se crea a través de un intercambio que implica la función [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) y la función [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .</span><span class="sxs-lookup"><span data-stu-id="a4021-106">For [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI), a security context is an opaque structure that is created through an exchange involving the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function and the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span>

<span data-ttu-id="a4021-107">Para obtener más información sobre los atributos de contexto, vea [requisitos de contexto](context-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a4021-107">For more information about the context attributes, see [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="a4021-108">El modelo SSPI admite tres tipos de contextos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a4021-108">The SSPI model supports three types of security contexts.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4021-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4021-109">Type</span></span></th>
<th><span data-ttu-id="a4021-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4021-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4021-111"><a href="connection-oriented-contexts.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="a4021-111"><a href="connection-oriented-contexts.md">Connection</a></span></span></td>
<td><span data-ttu-id="a4021-112">Un <a href="/windows/desktop/SecGloss/c-gly"><em>contexto</em></a> orientado a la conexión es el contexto de seguridad más común y el más sencillo de usar.</span><span class="sxs-lookup"><span data-stu-id="a4021-112">A connection-oriented <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> is the most common security context, and the simplest to use.</span></span> <span data-ttu-id="a4021-113">El autor de la llamada es responsable del formato de mensaje general y de la ubicación de los datos en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a4021-113">The caller is responsible for the overall message format and for the location of the data in the message.</span></span> <span data-ttu-id="a4021-114">El autor de la llamada también es responsable de la ubicación de los campos relevantes para la seguridad dentro de un mensaje, como la ubicación de los datos de la firma.</span><span class="sxs-lookup"><span data-stu-id="a4021-114">The caller is also responsible for the location of the security-relevant fields within a message, such as the location of the signature data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4021-115"><a href="datagram-contexts.md">Datagrama</a></span><span class="sxs-lookup"><span data-stu-id="a4021-115"><a href="datagram-contexts.md">Datagram</a></span></span></td>
<td><span data-ttu-id="a4021-116">Un contexto orientado a <a href="/windows/desktop/SecGloss/d-gly"><em>datagramas</em></a>tiene compatibilidad adicional para la comunicación de datagramas de estilo DCE.</span><span class="sxs-lookup"><span data-stu-id="a4021-116">A <a href="/windows/desktop/SecGloss/d-gly"><em>datagram</em></a>-oriented context has extra support for DCE-style datagram communication.</span></span> <span data-ttu-id="a4021-117">También se puede utilizar de forma genérica para una aplicación de transporte orientada a datagramas.</span><span class="sxs-lookup"><span data-stu-id="a4021-117">It can also be used generically for a datagram-oriented transport application.</span></span><br/>
<blockquote>
<p>[!Important]</p>
<p><span data-ttu-id="a4021-118">El paquete de <a href="microsoft-kerberos.md">Microsoft Kerberos</a> no admite contextos de datagramas en modo de usuario a usuario.</span><span class="sxs-lookup"><span data-stu-id="a4021-118">The <a href="microsoft-kerberos.md">Microsoft Kerberos</a> package does not support datagram contexts in user-to-user mode.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4021-119"><a href="stream-contexts.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="a4021-119"><a href="stream-contexts.md">Stream</a></span></span></td>
<td><span data-ttu-id="a4021-120">Un contexto orientado a secuencias es responsable del bloqueo y el formato de los mensajes en el paquete de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a4021-120">A stream-oriented context is responsible for the blocking and message formatting within the security package.</span></span> <span data-ttu-id="a4021-121">El autor de la llamada no está interesado en dar formato, sino en una secuencia de datos sin formato.</span><span class="sxs-lookup"><span data-stu-id="a4021-121">The caller is not interested in formatting, but rather a raw stream of data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a4021-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a4021-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4021-123">Requisitos de contexto</span><span class="sxs-lookup"><span data-stu-id="a4021-123">Context Requirements</span></span>](context-requirements.md)
</dt> <dt>

[<span data-ttu-id="a4021-124">Contextos orientados a conexiones</span><span class="sxs-lookup"><span data-stu-id="a4021-124">Connection-Oriented Contexts</span></span>](connection-oriented-contexts.md)
</dt> <dt>

[<span data-ttu-id="a4021-125">Contextos de datagramas</span><span class="sxs-lookup"><span data-stu-id="a4021-125">Datagram Contexts</span></span>](datagram-contexts.md)
</dt> <dt>

[<span data-ttu-id="a4021-126">Contextos de secuencia</span><span class="sxs-lookup"><span data-stu-id="a4021-126">Stream Contexts</span></span>](stream-contexts.md)
</dt> </dl>

 

 
