---
description: Servicios de Certificate Server admite solicitudes de certificados basadas en el \# formato PKCS 10 y en el formato keygen (Netscape). Los servicios de Certificate Server también admiten \# solicitudes de renovación de PKCS 7 y solicitudes de sintaxis de mensajes de cifrado (CMS).
ms.assetid: 6321ce99-f5d1-4d72-a062-99cffb543731
title: Requests
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7870e09d930fb06d50f0cc8acfff1270db1c92f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687910"
---
# <a name="requests"></a><span data-ttu-id="1a2b4-104">Requests</span><span class="sxs-lookup"><span data-stu-id="1a2b4-104">Requests</span></span>

<span data-ttu-id="1a2b4-105">Servicios de Certificate Server admite [*solicitudes de certificados*](../secgloss/c-gly.md) basadas en el \# formato PKCS 10 y en el formato keygen (Netscape).</span><span class="sxs-lookup"><span data-stu-id="1a2b4-105">Certificate Services supports [*certificate requests*](../secgloss/c-gly.md) based on the PKCS \#10 format and the Keygen (Netscape) format.</span></span> <span data-ttu-id="1a2b4-106">Los servicios de Certificate Server también admiten \# solicitudes de renovación de PKCS 7 y solicitudes de sintaxis de mensajes de cifrado (CMS).</span><span class="sxs-lookup"><span data-stu-id="1a2b4-106">Certificate Services also supports PKCS \#7 renewal requests and Cryptographic Message Syntax (CMS) requests.</span></span>

<span data-ttu-id="1a2b4-107">Los servicios de Certificate Server también proporcionan una interfaz [ICertRequest](/windows/desktop/api/Certcli/nn-certcli-icertrequest) , que contiene métodos para enviar una solicitud de certificado y (si se aprueba la solicitud) para recibir el certificado emitido resultante.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-107">Certificate Services also provides an [ICertRequest](/windows/desktop/api/Certcli/nn-certcli-icertrequest) interface, which contains methods for submitting a certificate request and (if the request is approved) for receiving the resulting issued certificate.</span></span>

<span data-ttu-id="1a2b4-108">Hay interfaces adicionales relacionadas con la seguridad disponibles en el [control de inscripción de certificados](certificate-enrollment-control.md).</span><span class="sxs-lookup"><span data-stu-id="1a2b4-108">Additional security-related interfaces are available in the [Certificate Enrollment Control](certificate-enrollment-control.md).</span></span>

 

 
