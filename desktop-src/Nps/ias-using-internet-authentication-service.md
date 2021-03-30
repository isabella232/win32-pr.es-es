---
title: Uso de extensiones de NPS
description: Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) al servidor de directivas de redes (NPS).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Servicio de autenticación de Internet IAS, tareas
- Servicio de autenticación de Internet IAS, usar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cc9f10c810ec9fe16618144db11686a1e2132
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104533064"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="7ec73-105">Uso de extensiones de NPS</span><span class="sxs-lookup"><span data-stu-id="7ec73-105">Using NPS Extensions</span></span>

<span data-ttu-id="7ec73-106">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) al servidor de directivas de redes (NPS).</span><span class="sxs-lookup"><span data-stu-id="7ec73-106">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="7ec73-107">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="7ec73-107">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="7ec73-108">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="7ec73-108">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="7ec73-109">\* \* Windows Server 2008 R2 y Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="7ec73-109">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="7ec73-110">Los ejemplos de acceso telefónico y Nombredemapa amplían la funcionalidad de NPS.</span><span class="sxs-lookup"><span data-stu-id="7ec73-110">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="7ec73-111">Muestra</span><span class="sxs-lookup"><span data-stu-id="7ec73-111">Sample</span></span>             | <span data-ttu-id="7ec73-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ec73-112">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec73-113">Omiten</span><span class="sxs-lookup"><span data-stu-id="7ec73-113">DialIn</span></span><br/>  | <span data-ttu-id="7ec73-114">En este ejemplo se implementa un archivo DLL de extensión RADIUS que comprueba el bit de marcado del usuario.</span><span class="sxs-lookup"><span data-stu-id="7ec73-114">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="7ec73-115">nombreDeMapa</span><span class="sxs-lookup"><span data-stu-id="7ec73-115">MapName</span></span><br/> | <span data-ttu-id="7ec73-116">Este archivo DLL de extensión de ejemplo busca la cuenta designada en todos los dominios de confianza.</span><span class="sxs-lookup"><span data-stu-id="7ec73-116">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="7ec73-117">Esto permite autenticar a los usuarios de varios dominios sin que los usuarios tengan que proporcionar su nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="7ec73-117">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="7ec73-118">Puede encontrar el código fuente de las aplicaciones de ejemplo Nombredemapa y Dialen en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="7ec73-118">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="7ec73-119">*Ubicación*,% install Path%, designa el directorio de instalación base para equipos x64.</span><span class="sxs-lookup"><span data-stu-id="7ec73-119">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="7ec73-120">Vea también [Kit de desarrollo de software (SDK) de Windows para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), kit de desarrollo de software (SDK) de Microsoft Windows y [descargas para el desarrollo de aplicaciones de la tienda Windows](https://msdn.microsoft.com/windows/apps/br229516).</span><span class="sxs-lookup"><span data-stu-id="7ec73-120">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="7ec73-121">Windows SDK para Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ec73-121">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="7ec73-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ec73-122">Windows Server 2012</span></span>

<span data-ttu-id="7ec73-123">Vínculo de descarga: N/A</span><span class="sxs-lookup"><span data-stu-id="7ec73-123">Download link: N/A</span></span>

<span data-ttu-id="7ec73-124">Nombredemapa: no</span><span class="sxs-lookup"><span data-stu-id="7ec73-124">MapName: No</span></span>

<span data-ttu-id="7ec73-125">Marcado: no</span><span class="sxs-lookup"><span data-stu-id="7ec73-125">DialIn: No</span></span>

<span data-ttu-id="7ec73-126">Ubicación: N/A</span><span class="sxs-lookup"><span data-stu-id="7ec73-126">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="7ec73-127">Kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7 y .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="7ec73-127">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="7ec73-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ec73-128">Windows Server 2008 R2</span></span>

<span data-ttu-id="7ec73-129">Vínculo de descarga: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="7ec73-129">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="7ec73-130">Nombredemapa: sí</span><span class="sxs-lookup"><span data-stu-id="7ec73-130">MapName: Yes</span></span>

<span data-ttu-id="7ec73-131">Marcado: no</span><span class="sxs-lookup"><span data-stu-id="7ec73-131">DialIn: No</span></span>

<span data-ttu-id="7ec73-132">Ubicación:% install path% \\ Microsoft SDKs \\ Windows \\ v 7.1 \\ Samples \\ netds \\ IAS</span><span class="sxs-lookup"><span data-stu-id="7ec73-132">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="7ec73-133">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7ec73-133">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="7ec73-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ec73-134">Windows Server 2008</span></span>

<span data-ttu-id="7ec73-135">Vínculo de descarga: <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="7ec73-135">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="7ec73-136">Nombredemapa: sí</span><span class="sxs-lookup"><span data-stu-id="7ec73-136">MapName: Yes</span></span>

<span data-ttu-id="7ec73-137">Marcado: no</span><span class="sxs-lookup"><span data-stu-id="7ec73-137">DialIn: No</span></span>

<span data-ttu-id="7ec73-138">Ubicación:% install path% \\ Microsoft SDKs \\ Windows \\ v 6.1 \\ Samples \\ NetDs \\ IAS</span><span class="sxs-lookup"><span data-stu-id="7ec73-138">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="7ec73-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7ec73-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ec73-140">Descargas para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="7ec73-140">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="7ec73-141">Windows SDK para Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ec73-141">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





