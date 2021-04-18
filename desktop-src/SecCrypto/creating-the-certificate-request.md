---
description: El proceso de creación de una solicitud de certificado implica la recopilación de cierta información del solicitante.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Crear la solicitud de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666420"
---
# <a name="creating-the-certificate-request"></a><span data-ttu-id="41167-103">Crear la solicitud de certificado</span><span class="sxs-lookup"><span data-stu-id="41167-103">Creating the Certificate Request</span></span>

<span data-ttu-id="41167-104">El proceso de creación de una solicitud de certificado implica la recopilación de cierta información del solicitante.</span><span class="sxs-lookup"><span data-stu-id="41167-104">The process of creating a certificate request involves collecting certain information from the requester.</span></span> <span data-ttu-id="41167-105">Normalmente, esto se realiza a través de algún tipo de interfaz de usuario, aunque la información podría tomarse directamente desde una base de datos sin necesidad de una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="41167-105">Usually, this is done through some sort of user interface (UI), although the information could be taken directly from a database without the need for a UI.</span></span> <span data-ttu-id="41167-106">El nivel de la información requerida se establece mediante la Directiva de la entidad de [*certificación*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="41167-106">The level of information required is set by the policy of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="41167-107">A continuación se muestra un ejemplo de la información necesaria:</span><span class="sxs-lookup"><span data-stu-id="41167-107">An example of the required information might be as follows:</span></span>

-   <span data-ttu-id="41167-108">Nombre común</span><span class="sxs-lookup"><span data-stu-id="41167-108">Common Name</span></span>
-   <span data-ttu-id="41167-109">Nombre de unidad</span><span class="sxs-lookup"><span data-stu-id="41167-109">Unit Name</span></span>
-   <span data-ttu-id="41167-110">Nombre de la empresa</span><span class="sxs-lookup"><span data-stu-id="41167-110">Company Name</span></span>
-   <span data-ttu-id="41167-111">City (Ciudad)</span><span class="sxs-lookup"><span data-stu-id="41167-111">City</span></span>
-   <span data-ttu-id="41167-112">Estado</span><span class="sxs-lookup"><span data-stu-id="41167-112">State</span></span>
-   <span data-ttu-id="41167-113">País/región</span><span class="sxs-lookup"><span data-stu-id="41167-113">Country/Region</span></span>

> [!Note]  
> <span data-ttu-id="41167-114">La interfaz está diseñada para hacer una solicitud única para cada instancia de XENROLL.</span><span class="sxs-lookup"><span data-stu-id="41167-114">The interface is designed to make a single request for each xenroll instance.</span></span> <span data-ttu-id="41167-115">Se debe crear una instancia de XENROLL independiente para crear cada [*solicitud de certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="41167-115">A separate xenroll instance must be created to create each [*certificate request*](../secgloss/c-gly.md).</span></span>

 

<span data-ttu-id="41167-116">Para obtener información sobre cómo usar el control de inscripción de certificados para solicitar un certificado en lenguajes de programación específicos, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="41167-116">For information about how to use the Certificate Enrollment Control to request a certificate in specific programming languages, see the following topics:</span></span>

-   [<span data-ttu-id="41167-117">Ejemplo de solicitud en C++</span><span class="sxs-lookup"><span data-stu-id="41167-117">Request Sample in C++</span></span>](request-sample-in-c-.md)
-   [<span data-ttu-id="41167-118">Ejemplo de solicitud en VBScript</span><span class="sxs-lookup"><span data-stu-id="41167-118">Request Sample in VBScript</span></span>](request-sample-in-vbscript.md)

 

 
