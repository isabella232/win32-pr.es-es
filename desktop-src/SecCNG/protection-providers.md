---
description: A partir de Windows 8, Microsoft comenzó a distribuir los proveedores que le permiten compartir de forma segura secretos y mensajes cifrados entre equipos.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Proveedores de protección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001648"
---
# <a name="protection-providers"></a><span data-ttu-id="d9ee7-103">Proveedores de protección</span><span class="sxs-lookup"><span data-stu-id="d9ee7-103">Protection Providers</span></span>

<span data-ttu-id="d9ee7-104">A partir de Windows 8, Microsoft comenzó a distribuir los proveedores que le permiten compartir de forma segura secretos y mensajes cifrados entre equipos.</span><span class="sxs-lookup"><span data-stu-id="d9ee7-104">Beginning with Windows 8, Microsoft began distributing the providers that enable you to securely share encrypted secrets and messages across computers.</span></span> <span data-ttu-id="d9ee7-105">Actualmente hay dos proveedores de protección de claves.</span><span class="sxs-lookup"><span data-stu-id="d9ee7-105">There are currently two key protection providers.</span></span> <span data-ttu-id="d9ee7-106">El proveedor de protección de claves de Microsoft permite proteger el contenido en un grupo de un bosque de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d9ee7-106">The Microsoft Key Protection provider allows you to protect content to a group in an Active Directory forest.</span></span> <span data-ttu-id="d9ee7-107">El proveedor de protección de claves de cliente de Microsoft permite proteger el contenido en un conjunto de credenciales Web.</span><span class="sxs-lookup"><span data-stu-id="d9ee7-107">The Microsoft Client Key Protection provider allows you to protect content to a set of web credentials.</span></span>

<span data-ttu-id="d9ee7-108">El protector correcto que se va a usar se elige automáticamente cuando la función [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) analiza la cadena de la regla del descriptor de protección que proporciona como entrada.</span><span class="sxs-lookup"><span data-stu-id="d9ee7-108">The correct protector to use is automatically chosen for you when the [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) function parses the protection descriptor rule string your provide as input.</span></span> <span data-ttu-id="d9ee7-109">Se elige el proveedor de protección de claves de Microsoft para las cadenas de reglas que comienzan por SID, SDDL y LOCAL.</span><span class="sxs-lookup"><span data-stu-id="d9ee7-109">The Microsoft Key Protection provider is chosen for rule strings that begin with SID, SDDL, and LOCAL.</span></span> <span data-ttu-id="d9ee7-110">El proveedor de protección de claves de cliente de Microsoft analiza las cadenas de reglas que comienzan con las credenciales webcredentials.</span><span class="sxs-lookup"><span data-stu-id="d9ee7-110">The Microsoft Client Key Protection provider parses rule strings that begin with WEBCREDENTIALS.</span></span> <span data-ttu-id="d9ee7-111">Para obtener más información sobre las cadenas de reglas, consulte [descriptores de protección](protection-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="d9ee7-111">For more information about rule strings, see [Protection Descriptors](protection-descriptors.md).</span></span>

> [!Note]  
> <span data-ttu-id="d9ee7-112">Los proveedores personalizados no están permitidos actualmente. [DPAPI de CNG](cng-dpapi.md)</span><span class="sxs-lookup"><span data-stu-id="d9ee7-112">Custom providers are not currently allowed.[CNG DPAPI](cng-dpapi.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d9ee7-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9ee7-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9ee7-114">DPAPI DE CNG</span><span class="sxs-lookup"><span data-stu-id="d9ee7-114">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="d9ee7-115">**NCryptCreateProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d9ee7-115">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[<span data-ttu-id="d9ee7-116">Descriptores de protección</span><span class="sxs-lookup"><span data-stu-id="d9ee7-116">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> </dl>

 

 



