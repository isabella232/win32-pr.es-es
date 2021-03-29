---
title: Objeto agente de revocación de licencias
description: Objeto agente de revocación de licencias
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- SDK de Windows Media Format, objetos de agente de revocación de licencias
- Advanced Systems Format (ASF), objetos de agente de revocación de licencias
- ASF (formato de sistemas avanzados), objetos de agente de revocación de licencias
- objetos, objetos del agente de revocación de licencias
- revocación de licencias, objetos de agente de revocación de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420237"
---
# <a name="license-revocation-agent-object"></a><span data-ttu-id="f28eb-108">Objeto agente de revocación de licencias</span><span class="sxs-lookup"><span data-stu-id="f28eb-108">License Revocation Agent Object</span></span>

<span data-ttu-id="f28eb-109">El objeto agente de revocación de licencias administra el lado cliente de la revocación de licencia.</span><span class="sxs-lookup"><span data-stu-id="f28eb-109">The license revocation agent object manages the client side of license revocation.</span></span> <span data-ttu-id="f28eb-110">La revocación de licencias es el proceso por el que un servidor de licencias puede quitar licencias del almacén de licencias en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="f28eb-110">License revocation is the process by which a license server can remove licenses from the license store on the client computer.</span></span> <span data-ttu-id="f28eb-111">El proceso implica pasar varios mensajes entre la aplicación cliente y el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="f28eb-111">The process involves passing several messages between the client application and the license server.</span></span> <span data-ttu-id="f28eb-112">Los métodos expuestos en este objeto procesan y generan esos mensajes.</span><span class="sxs-lookup"><span data-stu-id="f28eb-112">The methods exposed on this object process and generate those messages.</span></span>

<span data-ttu-id="f28eb-113">El objeto agente de revocación de licencias se crea mediante la función [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) , que establece un puntero a una interfaz [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .</span><span class="sxs-lookup"><span data-stu-id="f28eb-113">The license revocation agent object is created by the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function, which sets a pointer to an [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span> <span data-ttu-id="f28eb-114">**IUnknown** y **IWMLicenseRevocationAgent** son las únicas interfaces que admite este objeto.</span><span class="sxs-lookup"><span data-stu-id="f28eb-114">**IUnknown** and **IWMLicenseRevocationAgent** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f28eb-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f28eb-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f28eb-116">**Objects**</span><span class="sxs-lookup"><span data-stu-id="f28eb-116">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




