---
description: Los certificados se conceden según las directivas que definen los criterios que los solicitantes deben cumplir para recibir un certificado.
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: Independencia de la Directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0d99b5babeced0fb87d9e603038e23a40859b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360906"
---
# <a name="policy-independence"></a><span data-ttu-id="469a1-103">Independencia de la Directiva</span><span class="sxs-lookup"><span data-stu-id="469a1-103">Policy Independence</span></span>

<span data-ttu-id="469a1-104">Los certificados se conceden según las directivas que definen los criterios que los solicitantes deben cumplir para recibir un certificado.</span><span class="sxs-lookup"><span data-stu-id="469a1-104">Certificates are granted according to policies that define criteria that requesters must meet to receive a certificate.</span></span> <span data-ttu-id="469a1-105">Por ejemplo, una Directiva puede ser conceder certificados comerciales solo si los solicitantes presentan su identificación en persona.</span><span class="sxs-lookup"><span data-stu-id="469a1-105">For example, one policy may be to grant commercial certificates only if applicants present their identification in person.</span></span> <span data-ttu-id="469a1-106">Otra directiva puede conceder [*credenciales*](../secgloss/c-gly.md) basadas en solicitudes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="469a1-106">Another policy may grant [*credentials*](../secgloss/c-gly.md) based on email requests.</span></span> <span data-ttu-id="469a1-107">Una agencia que emite tarjetas de crédito puede optar por consultar una base de datos y realizar consultas telefónicas antes de emitir una tarjeta.</span><span class="sxs-lookup"><span data-stu-id="469a1-107">An agency that issues credit cards may choose to consult a database and make phone inquiries before issuing a card.</span></span>

<span data-ttu-id="469a1-108">Las directivas se implementan en módulos de directivas escritos en C++, C o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="469a1-108">Policies are implemented in policy modules written in C++, C, or Visual Basic.</span></span> <span data-ttu-id="469a1-109">Las funciones de servicios de Certificate Server están aisladas de los cambios de la Directiva que puede implementar una agencia.</span><span class="sxs-lookup"><span data-stu-id="469a1-109">Certificate Services functions are isolated from any changes in policy that an agency might implement.</span></span> <span data-ttu-id="469a1-110">Los cambios en la Directiva se pueden implementar completamente en el código del módulo de directivas del servidor.</span><span class="sxs-lookup"><span data-stu-id="469a1-110">Changes in policy can be fully implemented in the server policy module code.</span></span> <span data-ttu-id="469a1-111">Una [*entidad de certificación*](../secgloss/c-gly.md) (CA) empresarial solo debe usar el módulo de directivas empresariales proporcionado por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="469a1-111">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

 

 
