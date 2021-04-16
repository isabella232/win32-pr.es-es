---
description: Curvas elípticas habilitadas en las versiones 1507 y 1511 de Windows 10.
title: Curvas elípticas de TLS en Windows 10, versión 1507 y 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: c38d1014433e1274d8dff52be09d59761d3b1761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720656"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a><span data-ttu-id="1ba3e-103">Curvas elípticas de TLS en Windows 10, versión 1507 y 1511</span><span class="sxs-lookup"><span data-stu-id="1ba3e-103">TLS Elliptic Curves in Windows 10 version 1507 and 1511</span></span>

<span data-ttu-id="1ba3e-104">En el caso de las versiones 1507 y 1511 de Windows 10, las siguientes curvas elípticas están habilitadas y en este orden de prioridad de forma predeterminada con el proveedor de Microsoft Schannel:</span><span class="sxs-lookup"><span data-stu-id="1ba3e-104">For Windows 10, versions 1507 and 1511, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="1ba3e-105">Cadena de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="1ba3e-105">Elliptic curve string</span></span> | <span data-ttu-id="1ba3e-106">Disponible en modo FIPS</span><span class="sxs-lookup"><span data-stu-id="1ba3e-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="1ba3e-107">NistP256</span><span class="sxs-lookup"><span data-stu-id="1ba3e-107">NistP256</span></span> | <span data-ttu-id="1ba3e-108">Sí</span><span class="sxs-lookup"><span data-stu-id="1ba3e-108">Yes</span></span> |
| <span data-ttu-id="1ba3e-109">NistP384</span><span class="sxs-lookup"><span data-stu-id="1ba3e-109">NistP384</span></span> | <span data-ttu-id="1ba3e-110">Sí</span><span class="sxs-lookup"><span data-stu-id="1ba3e-110">Yes</span></span> |


<span data-ttu-id="1ba3e-111">El proveedor de Microsoft Schannel admite las siguientes curvas elípticas, pero no está habilitada de forma predeterminada:</span><span class="sxs-lookup"><span data-stu-id="1ba3e-111">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="1ba3e-112">Cadena de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="1ba3e-112">Elliptic curve string</span></span> | <span data-ttu-id="1ba3e-113">Disponible en modo FIPS</span><span class="sxs-lookup"><span data-stu-id="1ba3e-113">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="1ba3e-114">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-114">brainpoolP256r1</span></span> | <span data-ttu-id="1ba3e-115">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-115">No</span></span> |
| <span data-ttu-id="1ba3e-116">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-116">brainpoolP384r1</span></span> | <span data-ttu-id="1ba3e-117">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-117">No</span></span> |
| <span data-ttu-id="1ba3e-118">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-118">brainpoolP512r1</span></span> | <span data-ttu-id="1ba3e-119">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-119">No</span></span> |
| <span data-ttu-id="1ba3e-120">nistP192</span><span class="sxs-lookup"><span data-stu-id="1ba3e-120">nistP192</span></span> | <span data-ttu-id="1ba3e-121">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-121">No</span></span> |
| <span data-ttu-id="1ba3e-122">nistP224</span><span class="sxs-lookup"><span data-stu-id="1ba3e-122">nistP224</span></span> | <span data-ttu-id="1ba3e-123">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-123">No</span></span> |
| <span data-ttu-id="1ba3e-124">nistP521</span><span class="sxs-lookup"><span data-stu-id="1ba3e-124">nistP521</span></span> | <span data-ttu-id="1ba3e-125">Sí</span><span class="sxs-lookup"><span data-stu-id="1ba3e-125">Yes</span></span> |
| <span data-ttu-id="1ba3e-126">secP160k1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-126">secP160k1</span></span> | <span data-ttu-id="1ba3e-127">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-127">No</span></span> |
| <span data-ttu-id="1ba3e-128">secP160r1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-128">secP160r1</span></span> | <span data-ttu-id="1ba3e-129">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-129">No</span></span> |
| <span data-ttu-id="1ba3e-130">secP160r2</span><span class="sxs-lookup"><span data-stu-id="1ba3e-130">secP160r2</span></span> | <span data-ttu-id="1ba3e-131">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-131">No</span></span> |
| <span data-ttu-id="1ba3e-132">secP192k1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-132">secP192k1</span></span> | <span data-ttu-id="1ba3e-133">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-133">No</span></span> |
| <span data-ttu-id="1ba3e-134">secP192r1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-134">secP192r1</span></span> | <span data-ttu-id="1ba3e-135">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-135">No</span></span> |
| <span data-ttu-id="1ba3e-136">secP224k1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-136">secP224k1</span></span> | <span data-ttu-id="1ba3e-137">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-137">No</span></span> |
| <span data-ttu-id="1ba3e-138">secP224r1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-138">secP224r1</span></span> | <span data-ttu-id="1ba3e-139">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-139">No</span></span> |
| <span data-ttu-id="1ba3e-140">secP256k1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-140">secP256k1</span></span> | <span data-ttu-id="1ba3e-141">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-141">No</span></span> |
| <span data-ttu-id="1ba3e-142">secP256r1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-142">secP256r1</span></span> | <span data-ttu-id="1ba3e-143">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-143">No</span></span> |
| <span data-ttu-id="1ba3e-144">secP384r1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-144">secP384r1</span></span> | <span data-ttu-id="1ba3e-145">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-145">No</span></span> |
| <span data-ttu-id="1ba3e-146">secP521r1</span><span class="sxs-lookup"><span data-stu-id="1ba3e-146">secP521r1</span></span> | <span data-ttu-id="1ba3e-147">No</span><span class="sxs-lookup"><span data-stu-id="1ba3e-147">No</span></span> |

## <a name="enabling-elliptic-curves"></a><span data-ttu-id="1ba3e-148">Habilitar curvas elípticas</span><span class="sxs-lookup"><span data-stu-id="1ba3e-148">Enabling Elliptic Curves</span></span>

<span data-ttu-id="1ba3e-149">Para agregar curvas elípticas, implemente una directiva de grupo o use los cmdlets de TLS:</span><span class="sxs-lookup"><span data-stu-id="1ba3e-149">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="1ba3e-150">Para usar la Directiva de grupo, [Configure el orden de las curvas ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) en configuración del equipo > plantillas administrativas > de red > configuración de SSL con la lista de prioridades para todas las curvas elípticas que desee habilitar.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-150">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="1ba3e-151">Para usar PowerShell, consulte [cmdlets de TLS](/powershell/module/tls) para obtener una lista completa de la sintaxis y las descripciones de los cmdlets de TLS.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-151">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="1ba3e-152">Antes de Windows 10, las cadenas de conjunto de cifrado se anexaban con la curva elíptica para determinar la prioridad de la curva.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-152">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="1ba3e-153">Windows 10 admite un valor de orden de prioridad de curva elíptica, por lo que el sufijo de curva elíptica no es necesario y se reemplaza por el nuevo orden de prioridad de curva elíptica, cuando se proporciona, para permitir que las organizaciones usen la Directiva de grupo para configurar diferentes versiones de Windows con los mismos conjuntos de cifrado.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-153">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="1ba3e-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1ba3e-154">See Also</span></span>

[<span data-ttu-id="1ba3e-155">Configuración del orden de las curvas ECC de TLS</span><span class="sxs-lookup"><span data-stu-id="1ba3e-155">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="1ba3e-156">Administrar el orden ECC de TLS</span><span class="sxs-lookup"><span data-stu-id="1ba3e-156">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="1ba3e-157">Administrar curvas ECC de Windows mediante directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="1ba3e-157">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="1ba3e-158">Cmdlets de TLS</span><span class="sxs-lookup"><span data-stu-id="1ba3e-158">TLS cmdlets</span></span>](/powershell/module/tls)
