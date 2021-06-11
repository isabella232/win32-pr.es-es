---
title: Uso de extensiones NPS
description: Obtenga información sobre el uso de extensiones NPS. El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- IAS del servicio de autenticación de Internet, tareas
- Internet Authentication Service IAS , mediante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f422c005d6810a4035450e24de1324b28361f1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989081"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="e3076-106">Uso de extensiones NPS</span><span class="sxs-lookup"><span data-stu-id="e3076-106">Using NPS Extensions</span></span>

<span data-ttu-id="e3076-107">El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS).</span><span class="sxs-lookup"><span data-stu-id="e3076-107">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="e3076-108">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="e3076-108">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="e3076-109">A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="e3076-109">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="e3076-110">\*\*Windows Server 2008 R2 y Windows Server 2008: \*\*</span><span class="sxs-lookup"><span data-stu-id="e3076-110">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="e3076-111">Los ejemplos de DialIn y MapName amplían la funcionalidad nps.</span><span class="sxs-lookup"><span data-stu-id="e3076-111">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="e3076-112">Muestra</span><span class="sxs-lookup"><span data-stu-id="e3076-112">Sample</span></span>             | <span data-ttu-id="e3076-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3076-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3076-114">DialIn</span><span class="sxs-lookup"><span data-stu-id="e3076-114">DialIn</span></span><br/>  | <span data-ttu-id="e3076-115">En este ejemplo se implementa un archivo DLL de extensión RADIUS que comprueba el bit de acceso telefónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="e3076-115">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="e3076-116">nombreDeMapa</span><span class="sxs-lookup"><span data-stu-id="e3076-116">MapName</span></span><br/> | <span data-ttu-id="e3076-117">Este archivo DLL de extensión de ejemplo busca en todos los dominios de confianza la cuenta designada.</span><span class="sxs-lookup"><span data-stu-id="e3076-117">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="e3076-118">Esto permite que los usuarios de varios dominios se autentiquen sin que los usuarios tengan que proporcionar su nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="e3076-118">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="e3076-119">Puede encontrar el código fuente de las aplicaciones de ejemplo MapName y DialIn en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="e3076-119">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="e3076-120">*Ubicación*, %Ruta de instalación%, designa el directorio de instalación base para equipos x64.</span><span class="sxs-lookup"><span data-stu-id="e3076-120">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="e3076-121">Consulte también [Kit de desarrollo de software de Windows (SDK)](https://developer.microsoft.com/windows/downloads/windows-8-sdk)para Windows 8 , Microsoft Kit de desarrollo de software de Windows (SDK) y Descargas para el desarrollo de [aplicaciones de la Tienda Windows.](https://msdn.microsoft.com/windows/apps/br229516)</span><span class="sxs-lookup"><span data-stu-id="e3076-121">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="e3076-122">Windows SDK para Windows 8</span><span class="sxs-lookup"><span data-stu-id="e3076-122">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="e3076-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3076-123">Windows Server 2012</span></span>

<span data-ttu-id="e3076-124">Vínculo de descarga: N/A</span><span class="sxs-lookup"><span data-stu-id="e3076-124">Download link: N/A</span></span>

<span data-ttu-id="e3076-125">MapName: No</span><span class="sxs-lookup"><span data-stu-id="e3076-125">MapName: No</span></span>

<span data-ttu-id="e3076-126">DialIn: No</span><span class="sxs-lookup"><span data-stu-id="e3076-126">DialIn: No</span></span>

<span data-ttu-id="e3076-127">Ubicación: N/A</span><span class="sxs-lookup"><span data-stu-id="e3076-127">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="e3076-128">Microsoft Kit de desarrollo de software de Windows (SDK) para Windows 7 y .NET Framework 4.0</span><span class="sxs-lookup"><span data-stu-id="e3076-128">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="e3076-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e3076-129">Windows Server 2008 R2</span></span>

<span data-ttu-id="e3076-130">Vínculo de descarga: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="e3076-130">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="e3076-131">MapName: Sí</span><span class="sxs-lookup"><span data-stu-id="e3076-131">MapName: Yes</span></span>

<span data-ttu-id="e3076-132">DialIn: No</span><span class="sxs-lookup"><span data-stu-id="e3076-132">DialIn: No</span></span>

<span data-ttu-id="e3076-133">Ubicación: %Ruta de instalación% \\ SDK de Microsoft Windows \\ \\ v7.1 \\ Ejemplos \\ netds \\ ias</span><span class="sxs-lookup"><span data-stu-id="e3076-133">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="e3076-134">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e3076-134">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="e3076-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3076-135">Windows Server 2008</span></span>

<span data-ttu-id="e3076-136">Vínculo de descarga: <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="e3076-136">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="e3076-137">MapName: Sí</span><span class="sxs-lookup"><span data-stu-id="e3076-137">MapName: Yes</span></span>

<span data-ttu-id="e3076-138">DialIn: No</span><span class="sxs-lookup"><span data-stu-id="e3076-138">DialIn: No</span></span>

<span data-ttu-id="e3076-139">Ubicación: %Install Path% \\ Microsoft SDKs \\ Windows \\ v6.1 \\ Samples \\ NetDs \\ IAS</span><span class="sxs-lookup"><span data-stu-id="e3076-139">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="e3076-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3076-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3076-141">Descargas para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="e3076-141">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="e3076-142">Windows SDK para Windows 8</span><span class="sxs-lookup"><span data-stu-id="e3076-142">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





