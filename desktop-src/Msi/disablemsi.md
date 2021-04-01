---
description: Si el valor de esta Directiva del sistema por equipo se establece en &\# 0034; 2&\# 0034; el instalador está siempre deshabilitado para todas las aplicaciones. Si este valor de Directiva se establece en &\# 0034; 1&\# 0034;, el instalador está deshabilitado para las aplicaciones no administradas, pero aún está habilitado para las aplicaciones administradas.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf8a784f5e8090bf6ba2007091c22cf4bc070c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082785"
---
# <a name="disablemsi"></a><span data-ttu-id="6ba15-104">DisableMSI</span><span class="sxs-lookup"><span data-stu-id="6ba15-104">DisableMSI</span></span>

<span data-ttu-id="6ba15-105">Si el valor de esta [Directiva del sistema](system-policy.md) por equipo se establece en "2", el instalador está siempre deshabilitado para todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6ba15-105">If the value of this per-machine [system policy](system-policy.md) is set to "2" the installer is always disabled for all applications.</span></span> <span data-ttu-id="6ba15-106">Si este valor de Directiva se establece en "1", el instalador está deshabilitado para las aplicaciones no administradas, pero todavía está habilitado para las aplicaciones administradas.</span><span class="sxs-lookup"><span data-stu-id="6ba15-106">If this policy value is set to "1", the installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span>

<span data-ttu-id="6ba15-107">En la tabla siguiente se enumeran las posibles configuraciones.</span><span class="sxs-lookup"><span data-stu-id="6ba15-107">The following table lists the possible configurations.</span></span>



| <span data-ttu-id="6ba15-108">DisableMSI</span><span class="sxs-lookup"><span data-stu-id="6ba15-108">DisableMSI</span></span> | <span data-ttu-id="6ba15-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ba15-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba15-110">*Valor predeterminado*</span><span class="sxs-lookup"><span data-stu-id="6ba15-110">*Default*</span></span>  | <span data-ttu-id="6ba15-111">En Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 y Windows Server 2008 R2, si el valor de la Directiva es null, está ausente o cualquier número distinto de 1 o 2, el Windows Installer está habilitado para las aplicaciones administradas.</span><span class="sxs-lookup"><span data-stu-id="6ba15-111">On Windows Server 2003, Windows Server 2003 R2, Windows Server 2008, and Windows Server 2008 R2, if the policy value is Null, absent, or any number other than 1 or 2, the Windows Installer is enabled for managed applications.</span></span> <span data-ttu-id="6ba15-112">Las instalaciones de aplicaciones no administradas están bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="6ba15-112">Unmanaged application installs are blocked.</span></span><br/> <span data-ttu-id="6ba15-113">En Windows XP, Windows Vista y Windows 7, la Windows Installer está habilitada para todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6ba15-113">On Windows XP, Windows Vista, and Windows 7, the Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="6ba15-114">Se permiten todas las operaciones de instalación.</span><span class="sxs-lookup"><span data-stu-id="6ba15-114">All install operations are allowed.</span></span><br/> |
| <span data-ttu-id="6ba15-115">0</span><span class="sxs-lookup"><span data-stu-id="6ba15-115">0</span></span>          | <span data-ttu-id="6ba15-116">Windows Installer está habilitada para todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6ba15-116">Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="6ba15-117">Se permiten todas las operaciones de instalación.</span><span class="sxs-lookup"><span data-stu-id="6ba15-117">All install operations are allowed.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6ba15-118">1</span><span class="sxs-lookup"><span data-stu-id="6ba15-118">1</span></span>          | <span data-ttu-id="6ba15-119">El Windows Installer está deshabilitado para las aplicaciones no administradas, pero todavía está habilitado para las aplicaciones administradas.</span><span class="sxs-lookup"><span data-stu-id="6ba15-119">The Windows Installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span> <span data-ttu-id="6ba15-120">Las instalaciones por usuario no elevadas están bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="6ba15-120">Non-elevated per-user installations are blocked.</span></span> <span data-ttu-id="6ba15-121">Se permiten las instalaciones con privilegios elevados por usuario y por equipo.</span><span class="sxs-lookup"><span data-stu-id="6ba15-121">Per-user elevated and per-machine installs are allowed.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="6ba15-122">2</span><span class="sxs-lookup"><span data-stu-id="6ba15-122">2</span></span>          | <span data-ttu-id="6ba15-123">Windows Installer está siempre deshabilitada para todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6ba15-123">Windows Installer is always disabled for all applications.</span></span> <span data-ttu-id="6ba15-124">No se permite ninguna instalación, como reparaciones, reinstalaciones o instalaciones a petición.</span><span class="sxs-lookup"><span data-stu-id="6ba15-124">No installs are allowed including repairs, reinstalls, or on-demand installations.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a><span data-ttu-id="6ba15-125">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="6ba15-125">Registry Key</span></span>

<span data-ttu-id="6ba15-126">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="6ba15-126">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="6ba15-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6ba15-127">Data Type</span></span>

<span data-ttu-id="6ba15-128">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="6ba15-128">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ba15-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ba15-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ba15-130">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="6ba15-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




