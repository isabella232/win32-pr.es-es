---
description: Los requisitos de seguridad de nivel C2 especifican que los administradores del sistema deben poder auditar los eventos relacionados con la seguridad y que el acceso a estos datos de auditoría debe limitarse a los administradores autorizados.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Generación de auditoría
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d00be8b6d94b29a42436fdabc63be8d2c05789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653021"
---
# <a name="audit-generation"></a><span data-ttu-id="a5082-103">Generación de auditoría</span><span class="sxs-lookup"><span data-stu-id="a5082-103">Audit Generation</span></span>

<span data-ttu-id="a5082-104">Los requisitos de seguridad de nivel C2 especifican que los administradores del sistema deben poder auditar los eventos relacionados con la seguridad y que el acceso a estos datos de auditoría debe limitarse a los administradores autorizados.</span><span class="sxs-lookup"><span data-stu-id="a5082-104">C2-level security requirements specify that system administrators must be able to audit security-related events and that access to this audit data must be limited to authorized administrators.</span></span> <span data-ttu-id="a5082-105">La API de Windows proporciona funciones que permiten a un administrador supervisar los eventos relacionados con la seguridad.</span><span class="sxs-lookup"><span data-stu-id="a5082-105">The Windows API provides functions enabling an administrator to monitor security-related events.</span></span>

<span data-ttu-id="a5082-106">El descriptor de seguridad de un objeto protegible puede tener una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="a5082-106">The security descriptor for a securable object can have a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="a5082-107">Una SACL contiene [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) que especifican los tipos de intentos de acceso que generan informes de auditoría.</span><span class="sxs-lookup"><span data-stu-id="a5082-107">A SACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) that specify the types of access attempts that generate audit reports.</span></span> <span data-ttu-id="a5082-108">Cada ACE identifica un administrador de confianza, un conjunto de derechos de acceso y un conjunto de marcas que indican si el sistema genera mensajes de auditoría para intentos de acceso erróneos, intentos de acceso correctos o ambos.</span><span class="sxs-lookup"><span data-stu-id="a5082-108">Each ACE identifies a trustee, a set of access rights, and a set of flags that indicate whether the system generates audit messages for failed access attempts, successful access attempts, or both.</span></span>

<span data-ttu-id="a5082-109">El sistema escribe mensajes de auditoría en el registro de eventos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a5082-109">The system writes audit messages to the security event log.</span></span> <span data-ttu-id="a5082-110">Para obtener información sobre cómo obtener acceso a los registros de un registro de eventos de seguridad, vea [registro de eventos](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="a5082-110">For information about accessing the records in a security event log, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

<span data-ttu-id="a5082-111">Para leer o escribir la SACL de un objeto, un subproceso debe habilitar primero el privilegio de nombre de seguridad de SE \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a5082-111">To read or write an object's SACL, a thread must first enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="a5082-112">Para obtener más información, consulte [derechos de acceso de SACL](sacl-access-right.md).</span><span class="sxs-lookup"><span data-stu-id="a5082-112">For more information, see [SACL Access Right](sacl-access-right.md).</span></span>

<span data-ttu-id="a5082-113">La API de Windows también proporciona compatibilidad para que las aplicaciones de servidor generen mensajes de auditoría cuando un cliente intenta obtener acceso a un objeto privado.</span><span class="sxs-lookup"><span data-stu-id="a5082-113">The Windows API also provides support for server applications to generate audit messages when a client tries to access a private object.</span></span> <span data-ttu-id="a5082-114">Para obtener más información, consulte [auditar el acceso a objetos privados](auditing-access-to-private-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a5082-114">For more information, see [Auditing Access To Private Objects](auditing-access-to-private-objects.md).</span></span>

 

 
