---
title: Requisitos de firma de la característica de arranque seguro para los controladores en modo kernel
description: Requisitos de firma de la característica de arranque seguro para los controladores en modo kernel
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105705052"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a><span data-ttu-id="c6715-103">Requisitos de firma de la característica de arranque seguro para los controladores en modo kernel</span><span class="sxs-lookup"><span data-stu-id="c6715-103">Secure boot feature signing requirements for kernel-mode drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="c6715-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="c6715-104">Platforms</span></span>

<span data-ttu-id="c6715-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="c6715-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="c6715-106">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c6715-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="c6715-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6715-107">Description</span></span>

<span data-ttu-id="c6715-108">En Windows 8 y Windows Server 2012, incluido WinPE, el kernel se ha bloqueado para evitar que el malware introducido por los kits de arranque o raíz eluda los requisitos de seguridad del sistema operativo Windows para los controladores firmados.</span><span class="sxs-lookup"><span data-stu-id="c6715-108">In Windows 8 and Windows Server 2012, including WinPE, the kernel has been locked down to prevent malware introduced by boot or root kits from circumventing Windows operating system security requirements for signed drivers.</span></span>

<span data-ttu-id="c6715-109">Este cambio afecta a todos los controladores en modo kernel para dispositivos que admiten el arranque seguro de Unified extensible firmware Interface (UEFI). El arranque seguro UEFI es necesario para la certificación de Windows 8 para equipos cliente y es opcional para los servidores.</span><span class="sxs-lookup"><span data-stu-id="c6715-109">This change affects all kernel-mode drivers for devices that support unified extensible firmware interface (UEFI) Secure Boot; UEFI Secure Boot is required for Windows 8 certification for client machines, and optional for servers.</span></span> <span data-ttu-id="c6715-110">No afecta a los controladores de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="c6715-110">It does not affect user-mode drivers.</span></span>

<span data-ttu-id="c6715-111">El desarrollo estándar para los controladores en modo kernel implica el uso de la configuración de la depuración en modo kernel o de datos de configuración de arranque (BCD) <testsigning> .</span><span class="sxs-lookup"><span data-stu-id="c6715-111">Standard development for kernel-mode drivers involves either the use of kernel mode debugging or the boot configuration data (BCD) <testsigning> setting.</span></span> <span data-ttu-id="c6715-112">Ambos están deshabilitados cuando el arranque protegido está activado.</span><span class="sxs-lookup"><span data-stu-id="c6715-112">Both of these are disabled when Secured Boot is on.</span></span>

## <a name="manifestation"></a><span data-ttu-id="c6715-113">Manifestación</span><span class="sxs-lookup"><span data-stu-id="c6715-113">Manifestation</span></span>

<span data-ttu-id="c6715-114">Los controladores en modo kernel no se ejecutarán si no están firmados correctamente por una entidad de certificación (CA) de confianza.</span><span class="sxs-lookup"><span data-stu-id="c6715-114">Kernel-mode drivers will not run if they are not properly signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="c6715-115">El sistema operativo no permitirá la ejecución de controladores que no sean de confianza y no se permitirán mecanismos estándar como la depuración de kernel y testsigning.</span><span class="sxs-lookup"><span data-stu-id="c6715-115">The operating system will not allow untrusted drivers to run and standard mechanisms like kernel debugging and testsigning will not be permitted.</span></span>

## <a name="mitigation"></a><span data-ttu-id="c6715-116">Mitigación</span><span class="sxs-lookup"><span data-stu-id="c6715-116">Mitigation</span></span>

<span data-ttu-id="c6715-117">Para probar los controladores, debe deshabilitar el arranque seguro en BIOS y cumplir los otros requisitos de firma de prueba (consulte a continuación).</span><span class="sxs-lookup"><span data-stu-id="c6715-117">To test drivers, you must disable Secure Boot in BIOS as well as meet the other test-signing requirements (see below).</span></span>

<span data-ttu-id="c6715-118">Al distribuir controladores más ampliamente, deben estar firmados correctamente por una CA de confianza.</span><span class="sxs-lookup"><span data-stu-id="c6715-118">When distributing drivers more widely they must be properly signed by a trusted CA.</span></span>

## <a name="resources"></a><span data-ttu-id="c6715-119">Recursos</span><span class="sxs-lookup"><span data-stu-id="c6715-119">Resources</span></span>

-   <span data-ttu-id="c6715-120">[Controladores de firma](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6715-120">[Signing Drivers](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span></span>

 

 