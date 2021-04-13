---
description: Requisitos de Client-Side para la suplantación
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Requisitos de Client-Side para la suplantación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360081"
---
# <a name="client-side-requirements-for-impersonation"></a><span data-ttu-id="94811-103">Requisitos de Client-Side para la suplantación</span><span class="sxs-lookup"><span data-stu-id="94811-103">Client-Side Requirements for Impersonation</span></span>

<span data-ttu-id="94811-104">Se pueden especificar las dos configuraciones siguientes en relación con la suplantación en el lado cliente:</span><span class="sxs-lookup"><span data-stu-id="94811-104">The following two settings can be specified relative to impersonation on the client side:</span></span>

-   <span data-ttu-id="94811-105">Nivel de suplantación, que indica que el cliente está dispuesto a hacer que el servidor use su identidad.</span><span class="sxs-lookup"><span data-stu-id="94811-105">Impersonation level, which indicates the client's willingness to have the server use its identity.</span></span>
-   <span data-ttu-id="94811-106">Una configuración en el servicio Active Directory a través de la cual la cuenta de cliente se puede marcar como "la cuenta es confidencial y no se puede delegar", lo que deshabilitará la delegación.</span><span class="sxs-lookup"><span data-stu-id="94811-106">A setting in the Active Directory Service through which the client account can be marked "Account is sensitive and cannot be delegated," which will disable delegation.</span></span>

<span data-ttu-id="94811-107">El nivel de suplantación se puede establecer de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="94811-107">The impersonation level can be set in a variety of ways.</span></span> <span data-ttu-id="94811-108">Si el cliente no indica un nivel de suplantación, COM utilizará el valor predeterminado para todo el equipo.</span><span class="sxs-lookup"><span data-stu-id="94811-108">If the client does not indicate an impersonation level, the machine-wide default will be used by COM.</span></span> <span data-ttu-id="94811-109">El valor predeterminado para todo el equipo se puede establecer mediante la herramienta administrativa Servicios de componentes o Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="94811-109">The machine-wide default can be set using either the Component Services administrative tool or Dcomcnfg.exe.</span></span> <span data-ttu-id="94811-110">El cliente también puede indicar un nivel de suplantación preferible administrativamente con Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="94811-110">The client can also indicate a preferred impersonation level administratively with Dcomcnfg.exe.</span></span>

<span data-ttu-id="94811-111">El cliente puede indicar el nivel de suplantación mediante programación, mediante [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)(equivalente a [**IClientSecurity:: SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), al que se puede llamar con tanta frecuencia como sea necesario) o a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), al que se puede llamar una vez por cada proceso.</span><span class="sxs-lookup"><span data-stu-id="94811-111">The client can indicate the impersonation level programmatically, using either [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)—equivalent to [**IClientSecurity::SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), which can be called as often as necessary—or [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), which can be called once per process.</span></span>

<span data-ttu-id="94811-112">Si el cliente indica la suplantación de nivel de delegado (la autoridad más amplia que puede conceder al servidor), el cliente debe ejecutarse con una identidad que esté configurada correctamente en el servicio de Active Directory para permitir la delegación de su identidad.</span><span class="sxs-lookup"><span data-stu-id="94811-112">If the client indicates delegate-level impersonation—the broadest authority it can grant to the server—the client should be running under an identity that is properly configured in the Active Directory Service to enable its identity to be delegated.</span></span>

<span data-ttu-id="94811-113">Para obtener más información sobre los niveles de suplantación y los requisitos de delegación, consulte [delegación y suplantación](/windows/desktop/com/delegation-and-impersonation).</span><span class="sxs-lookup"><span data-stu-id="94811-113">For more detail regarding impersonation levels and the requirements for delegation to work, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

<span data-ttu-id="94811-114">Por supuesto, las aplicaciones COM+ siempre pueden actuar como clientes.</span><span class="sxs-lookup"><span data-stu-id="94811-114">COM+ applications can always act as clients, of course.</span></span> <span data-ttu-id="94811-115">Cuando la aplicación COM+ realiza una llamada a otra aplicación o recurso, expresa un nivel de suplantación.</span><span class="sxs-lookup"><span data-stu-id="94811-115">When the COM+ application makes a call to another application or resource, it expresses an impersonation level.</span></span> <span data-ttu-id="94811-116">En el caso de las aplicaciones de servidor COM+, puede establecer un nivel de suplantación de forma administrativa.</span><span class="sxs-lookup"><span data-stu-id="94811-116">For COM+ server applications, you can set an impersonation level administratively.</span></span> <span data-ttu-id="94811-117">Las aplicaciones de biblioteca COM+ no pueden establecer su propio nivel de suplantación; en su lugar, usan el del proceso de host.</span><span class="sxs-lookup"><span data-stu-id="94811-117">COM+ library applications cannot set their own impersonation level; they use that of the host process instead.</span></span> <span data-ttu-id="94811-118">Para obtener información sobre cómo establecer la suplantación para una aplicación COM+, vea [establecer un nivel de suplantación](setting-an-impersonation-level.md).</span><span class="sxs-lookup"><span data-stu-id="94811-118">To learn how to set impersonation for a COM+ application, see [Setting an Impersonation Level](setting-an-impersonation-level.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="94811-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94811-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94811-120">Suplantación y delegación de cliente</span><span class="sxs-lookup"><span data-stu-id="94811-120">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="94811-121">Esconder</span><span class="sxs-lookup"><span data-stu-id="94811-121">Cloaking</span></span>](cloaking.md)
</dt> <dt>

[<span data-ttu-id="94811-122">Requisitos del servidor para la suplantación</span><span class="sxs-lookup"><span data-stu-id="94811-122">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
