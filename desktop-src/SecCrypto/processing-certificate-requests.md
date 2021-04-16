---
description: Explica cómo los servicios de Certificate Server procesan las solicitudes de certificados.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Procesar solicitudes de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70a25d9ca633247c3995677825dc011b2b38d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557039"
---
# <a name="processing-certificate-requests"></a><span data-ttu-id="b7779-103">Procesar solicitudes de certificado</span><span class="sxs-lookup"><span data-stu-id="b7779-103">Processing Certificate Requests</span></span>

<span data-ttu-id="b7779-104">Servicios de Certificate Server realiza los siguientes pasos al procesar una [*solicitud de certificado*](../secgloss/c-gly.md):</span><span class="sxs-lookup"><span data-stu-id="b7779-104">Certificate Services performs the following steps when processing a [*certificate request*](../secgloss/c-gly.md):</span></span>

1.  <span data-ttu-id="b7779-105">Solicitar recepción.</span><span class="sxs-lookup"><span data-stu-id="b7779-105">Request reception.</span></span>

    <span data-ttu-id="b7779-106">El cliente envía la [*solicitud de certificado*](../secgloss/c-gly.md) a una aplicación intermediario, que la da formato a una solicitud de \# formato PKCS 10 y la envía al motor del servidor.</span><span class="sxs-lookup"><span data-stu-id="b7779-106">The [*certificate request*](../secgloss/c-gly.md) is sent by the client to an intermediary application, which formats it into a PKCS \#10 format request and submits it to the server engine.</span></span>

2.  <span data-ttu-id="b7779-107">Solicitar aprobación.</span><span class="sxs-lookup"><span data-stu-id="b7779-107">Request approval.</span></span>

    <span data-ttu-id="b7779-108">El motor del servidor llama al [módulo de directivas](policy-modules.md)de, que consulta las propiedades de la solicitud, decide si la solicitud está autorizada o no, y establece las propiedades opcionales del certificado.</span><span class="sxs-lookup"><span data-stu-id="b7779-108">The server engine calls the [Policy Module](policy-modules.md), which queries request properties, decides whether the request is authorized or not, and sets optional certificate properties.</span></span>

3.  <span data-ttu-id="b7779-109">Formación de certificados.</span><span class="sxs-lookup"><span data-stu-id="b7779-109">Certificate formation.</span></span>

    <span data-ttu-id="b7779-110">Si se aprueba la solicitud, el motor del servidor toma la solicitud y todas las propiedades solicitadas por el módulo de directivas, y crea un certificado completo.</span><span class="sxs-lookup"><span data-stu-id="b7779-110">If the request is approved, the server engine takes the request, and any properties requested by the Policy Module, and builds a complete certificate.</span></span>

4.  <span data-ttu-id="b7779-111">Publicación de certificado.</span><span class="sxs-lookup"><span data-stu-id="b7779-111">Certificate publication.</span></span>

    <span data-ttu-id="b7779-112">El motor del servidor almacena el certificado completado en la base de datos de servicios de certificados y notifica a la aplicación intermediario el estado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7779-112">The server engine stores the completed certificate in the Certificate Services database and notifies the intermediary application of the request status.</span></span> <span data-ttu-id="b7779-113">Si el [módulo de salida](exit-modules.md) lo ha solicitado, el motor del servidor le notificará un evento de emisión de certificado.</span><span class="sxs-lookup"><span data-stu-id="b7779-113">If the [exit module](exit-modules.md) has so requested, the server engine will notify it of a certificate issuance event.</span></span> <span data-ttu-id="b7779-114">Esto permite que el módulo de salida realice otras operaciones, como publicar el certificado en un repositorio de certificados externos (por ejemplo, un servicio de directorio).</span><span class="sxs-lookup"><span data-stu-id="b7779-114">This allows the exit module to perform further operations such as publishing the certificate to an external certificate repository (for example, a directory service).</span></span> <span data-ttu-id="b7779-115">Mientras tanto, el intermediario obtiene el certificado publicado de los servicios de servidor de certificados y lo devuelve al cliente.</span><span class="sxs-lookup"><span data-stu-id="b7779-115">Meanwhile, the intermediary gets the published certificate from Certificate Services and passes it back to the client.</span></span>

<span data-ttu-id="b7779-116">La siguiente ilustración muestra el modo en que los servicios de Certificate Server procesan una [*solicitud de certificado*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b7779-116">The following illustration shows how a [*certificate request*](../secgloss/c-gly.md) is processed by Certificate Services.</span></span>

![procesar una solicitud de certificado](images/certflow.png)

 

 
