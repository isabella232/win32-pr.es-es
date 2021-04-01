---
description: Componentes SID
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: Componentes SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082221"
---
# <a name="sid-components"></a><span data-ttu-id="69247-103">Componentes SID</span><span class="sxs-lookup"><span data-stu-id="69247-103">SID Components</span></span>

<span data-ttu-id="69247-104">Un valor de SID incluye componentes que proporcionan información sobre la estructura de [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) y los componentes que identifican de forma única a un administrador de confianza.</span><span class="sxs-lookup"><span data-stu-id="69247-104">A SID value includes components that provide information about the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure and components that uniquely identify a trustee.</span></span> <span data-ttu-id="69247-105">Un SID consta de los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="69247-105">A SID consists of the following components:</span></span>

-   <span data-ttu-id="69247-106">El nivel de revisión de la estructura de [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)</span><span class="sxs-lookup"><span data-stu-id="69247-106">The revision level of the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure</span></span>
-   <span data-ttu-id="69247-107">Un valor de autoridad de identificador de 48 bits que identifica la autoridad que emitió el SID.</span><span class="sxs-lookup"><span data-stu-id="69247-107">A 48-bit identifier authority value that identifies the authority that issued the SID</span></span>
-   <span data-ttu-id="69247-108">Un número variable de valores de subautoridad o de [*identificador relativo*](/windows/desktop/SecGloss/r-gly) (RID) que identifican de forma única el administrador de confianza con respecto a la autoridad que emitió el SID.</span><span class="sxs-lookup"><span data-stu-id="69247-108">A variable number of subauthority or [*relative identifier*](/windows/desktop/SecGloss/r-gly) (RID) values that uniquely identify the trustee relative to the authority that issued the SID</span></span>

<span data-ttu-id="69247-109">La combinación del valor de autoridad de identificador y los valores de subautor garantiza que no habrá dos SID serán el mismo, incluso si dos entidades emisoras de SID diferentes emiten la misma combinación de valores de RID.</span><span class="sxs-lookup"><span data-stu-id="69247-109">The combination of the identifier authority value and the subauthority values ensures that no two SIDs will be the same, even if two different SID-issuing authorities issue the same combination of RID values.</span></span> <span data-ttu-id="69247-110">Cada autoridad emisora de SID emite un RID determinado solo una vez.</span><span class="sxs-lookup"><span data-stu-id="69247-110">Each SID-issuing authority issues a given RID only once.</span></span>

<span data-ttu-id="69247-111">Los SID se almacenan en formato binario en una estructura de [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) .</span><span class="sxs-lookup"><span data-stu-id="69247-111">SIDs are stored in binary format in a [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure.</span></span> <span data-ttu-id="69247-112">Para mostrar un SID, puede llamar a la función [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) para convertir un SID binario en formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="69247-112">To display a SID, you can call the [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) function to convert a binary SID to string format.</span></span> <span data-ttu-id="69247-113">Para volver a convertir una cadena SID en un SID funcional válido, llame a la función [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) .</span><span class="sxs-lookup"><span data-stu-id="69247-113">To convert a SID string back to a valid, functional SID, call the [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) function.</span></span>

<span data-ttu-id="69247-114">Estas funciones utilizan la siguiente notación de cadena normalizada para SID, lo que facilita la visualización de sus componentes:</span><span class="sxs-lookup"><span data-stu-id="69247-114">These functions use the following standardized string notation for SIDs, which makes it simpler to visualize their components:</span></span>

<span data-ttu-id="69247-115">s-*R* - *I* - ...</span><span class="sxs-lookup"><span data-stu-id="69247-115">S-*R*-*I*-*S*…</span></span>

<span data-ttu-id="69247-116">En esta notación, el carácter literal "S" identifica la serie de dígitos como un SID, *R* es el nivel de revisión, *I* es el valor de la autoridad de identificador y *S*...</span><span class="sxs-lookup"><span data-stu-id="69247-116">In this notation, the literal character "S" identifies the series of digits as a SID, *R* is the revision level, *I* is the identifier-authority value, and *S*…</span></span> <span data-ttu-id="69247-117">es uno o varios valores de subautoridad.</span><span class="sxs-lookup"><span data-stu-id="69247-117">is one or more subauthority values.</span></span>

<span data-ttu-id="69247-118">En el ejemplo siguiente se usa esta notación para mostrar el SID relativo al dominio conocido del grupo de administradores locales:</span><span class="sxs-lookup"><span data-stu-id="69247-118">The following example uses this notation to display the well-known domain-relative SID of the local Administrators group:</span></span>

<span data-ttu-id="69247-119">S-1-5-32-544</span><span class="sxs-lookup"><span data-stu-id="69247-119">S-1-5-32-544</span></span>

<span data-ttu-id="69247-120">En este ejemplo, el SID tiene los siguientes componentes.</span><span class="sxs-lookup"><span data-stu-id="69247-120">In this example, the SID has the following components.</span></span> <span data-ttu-id="69247-121">Las constantes entre paréntesis son los valores conocidos de autoridad de identificador conocido y [*RID*](/windows/desktop/SecGloss/r-gly) definidos en Winnt. h:</span><span class="sxs-lookup"><span data-stu-id="69247-121">The constants in parentheses are well-known identifier authority and [*RID*](/windows/desktop/SecGloss/r-gly) values defined in Winnt.h:</span></span>

-   <span data-ttu-id="69247-122">Un nivel de revisión de 1</span><span class="sxs-lookup"><span data-stu-id="69247-122">A revision level of 1</span></span>
-   <span data-ttu-id="69247-123">Un valor de autoridad de identificador de 5 (entidad de seguridad de \_ NT \_ )</span><span class="sxs-lookup"><span data-stu-id="69247-123">An identifier-authority value of 5 (SECURITY\_NT\_AUTHORITY)</span></span>
-   <span data-ttu-id="69247-124">Primer valor de subautoridad de 32 (seguridad, \_ \_ RID de dominio \_ )</span><span class="sxs-lookup"><span data-stu-id="69247-124">A first subauthority value of 32 (SECURITY\_BUILTIN\_DOMAIN\_RID)</span></span>
-   <span data-ttu-id="69247-125">Un segundo valor de subautoridad de 544 ( \_ administradores de RID de alias de dominio \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="69247-125">A second subauthority value of 544 (DOMAIN\_ALIAS\_RID\_ADMINS)</span></span>

 

 
