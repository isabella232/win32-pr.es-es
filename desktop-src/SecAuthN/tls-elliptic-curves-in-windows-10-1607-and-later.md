---
description: Curvas elípticas habilitadas en la versión 1607 de Windows 10 y versiones posteriores.
title: Curvas elípticas de TLS en la versión 1607 de Windows 10 y versiones posteriores
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 813a7c117f5f1e3fc1c6484fc57d1c9f14cf9567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278255"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a><span data-ttu-id="7e402-103">Curvas elípticas de TLS en la versión 1607 de Windows 10 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="7e402-103">TLS Elliptic Curves in Windows 10 version 1607 and later</span></span>

<span data-ttu-id="7e402-104">En Windows 10, versiones 1607 y posteriores, las siguientes curvas elípticas están habilitadas y en este orden de prioridad de forma predeterminada con el proveedor de Microsoft Schannel:</span><span class="sxs-lookup"><span data-stu-id="7e402-104">For Windows 10, versions 1607 and later, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="7e402-105">Cadena de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="7e402-105">Elliptic curve string</span></span> | <span data-ttu-id="7e402-106">Disponible en modo FIPS</span><span class="sxs-lookup"><span data-stu-id="7e402-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="7e402-107">curve25519</span><span class="sxs-lookup"><span data-stu-id="7e402-107">curve25519</span></span> | <span data-ttu-id="7e402-108">No</span><span class="sxs-lookup"><span data-stu-id="7e402-108">No</span></span> |
| <span data-ttu-id="7e402-109">NistP256</span><span class="sxs-lookup"><span data-stu-id="7e402-109">NistP256</span></span> | <span data-ttu-id="7e402-110">Sí</span><span class="sxs-lookup"><span data-stu-id="7e402-110">Yes</span></span> |
| <span data-ttu-id="7e402-111">NistP384</span><span class="sxs-lookup"><span data-stu-id="7e402-111">NistP384</span></span> | <span data-ttu-id="7e402-112">Sí</span><span class="sxs-lookup"><span data-stu-id="7e402-112">Yes</span></span> |


<span data-ttu-id="7e402-113">El proveedor de Microsoft Schannel admite las siguientes curvas elípticas, pero no está habilitada de forma predeterminada:</span><span class="sxs-lookup"><span data-stu-id="7e402-113">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="7e402-114">Cadena de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="7e402-114">Elliptic curve string</span></span> | <span data-ttu-id="7e402-115">Disponible en modo FIPS</span><span class="sxs-lookup"><span data-stu-id="7e402-115">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="7e402-116">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="7e402-116">brainpoolP256r1</span></span> | <span data-ttu-id="7e402-117">No</span><span class="sxs-lookup"><span data-stu-id="7e402-117">No</span></span> |
| <span data-ttu-id="7e402-118">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="7e402-118">brainpoolP384r1</span></span> | <span data-ttu-id="7e402-119">No</span><span class="sxs-lookup"><span data-stu-id="7e402-119">No</span></span> |
| <span data-ttu-id="7e402-120">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="7e402-120">brainpoolP512r1</span></span> | <span data-ttu-id="7e402-121">No</span><span class="sxs-lookup"><span data-stu-id="7e402-121">No</span></span> |
| <span data-ttu-id="7e402-122">nistP192</span><span class="sxs-lookup"><span data-stu-id="7e402-122">nistP192</span></span> | <span data-ttu-id="7e402-123">No</span><span class="sxs-lookup"><span data-stu-id="7e402-123">No</span></span> |
| <span data-ttu-id="7e402-124">nistP224</span><span class="sxs-lookup"><span data-stu-id="7e402-124">nistP224</span></span> | <span data-ttu-id="7e402-125">No</span><span class="sxs-lookup"><span data-stu-id="7e402-125">No</span></span> |
| <span data-ttu-id="7e402-126">nistP521</span><span class="sxs-lookup"><span data-stu-id="7e402-126">nistP521</span></span> | <span data-ttu-id="7e402-127">Sí</span><span class="sxs-lookup"><span data-stu-id="7e402-127">Yes</span></span> |
| <span data-ttu-id="7e402-128">secP160k1</span><span class="sxs-lookup"><span data-stu-id="7e402-128">secP160k1</span></span> | <span data-ttu-id="7e402-129">No</span><span class="sxs-lookup"><span data-stu-id="7e402-129">No</span></span> |
| <span data-ttu-id="7e402-130">secP160r1</span><span class="sxs-lookup"><span data-stu-id="7e402-130">secP160r1</span></span> | <span data-ttu-id="7e402-131">No</span><span class="sxs-lookup"><span data-stu-id="7e402-131">No</span></span> |
| <span data-ttu-id="7e402-132">secP160r2</span><span class="sxs-lookup"><span data-stu-id="7e402-132">secP160r2</span></span> | <span data-ttu-id="7e402-133">No</span><span class="sxs-lookup"><span data-stu-id="7e402-133">No</span></span> |
| <span data-ttu-id="7e402-134">secP192k1</span><span class="sxs-lookup"><span data-stu-id="7e402-134">secP192k1</span></span> | <span data-ttu-id="7e402-135">No</span><span class="sxs-lookup"><span data-stu-id="7e402-135">No</span></span> |
| <span data-ttu-id="7e402-136">secP192r1</span><span class="sxs-lookup"><span data-stu-id="7e402-136">secP192r1</span></span> | <span data-ttu-id="7e402-137">No</span><span class="sxs-lookup"><span data-stu-id="7e402-137">No</span></span> |
| <span data-ttu-id="7e402-138">secP224k1</span><span class="sxs-lookup"><span data-stu-id="7e402-138">secP224k1</span></span> | <span data-ttu-id="7e402-139">No</span><span class="sxs-lookup"><span data-stu-id="7e402-139">No</span></span> |
| <span data-ttu-id="7e402-140">secP224r1</span><span class="sxs-lookup"><span data-stu-id="7e402-140">secP224r1</span></span> | <span data-ttu-id="7e402-141">No</span><span class="sxs-lookup"><span data-stu-id="7e402-141">No</span></span> |
| <span data-ttu-id="7e402-142">secP256k1</span><span class="sxs-lookup"><span data-stu-id="7e402-142">secP256k1</span></span> | <span data-ttu-id="7e402-143">No</span><span class="sxs-lookup"><span data-stu-id="7e402-143">No</span></span> |
| <span data-ttu-id="7e402-144">secP256r1</span><span class="sxs-lookup"><span data-stu-id="7e402-144">secP256r1</span></span> | <span data-ttu-id="7e402-145">No</span><span class="sxs-lookup"><span data-stu-id="7e402-145">No</span></span> |
| <span data-ttu-id="7e402-146">secP384r1</span><span class="sxs-lookup"><span data-stu-id="7e402-146">secP384r1</span></span> | <span data-ttu-id="7e402-147">No</span><span class="sxs-lookup"><span data-stu-id="7e402-147">No</span></span> |
| <span data-ttu-id="7e402-148">secP521r1</span><span class="sxs-lookup"><span data-stu-id="7e402-148">secP521r1</span></span> | <span data-ttu-id="7e402-149">No</span><span class="sxs-lookup"><span data-stu-id="7e402-149">No</span></span> |



## <a name="enabling-elliptic-curves"></a><span data-ttu-id="7e402-150">Habilitar curvas elípticas</span><span class="sxs-lookup"><span data-stu-id="7e402-150">Enabling Elliptic Curves</span></span>

<span data-ttu-id="7e402-151">Para agregar curvas elípticas, implemente una directiva de grupo o use los cmdlets de TLS:</span><span class="sxs-lookup"><span data-stu-id="7e402-151">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="7e402-152">Para usar la Directiva de grupo, [Configure el orden de las curvas ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) en configuración del equipo > plantillas administrativas > de red > configuración de SSL con la lista de prioridades para todas las curvas elípticas que desee habilitar.</span><span class="sxs-lookup"><span data-stu-id="7e402-152">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="7e402-153">Para usar PowerShell, consulte [cmdlets de TLS](/powershell/module/tls) para obtener una lista completa de la sintaxis y las descripciones de los cmdlets de TLS.</span><span class="sxs-lookup"><span data-stu-id="7e402-153">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="7e402-154">Antes de Windows 10, las cadenas de conjunto de cifrado se anexaban con la curva elíptica para determinar la prioridad de la curva.</span><span class="sxs-lookup"><span data-stu-id="7e402-154">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="7e402-155">Windows 10 admite un valor de orden de prioridad de curva elíptica, por lo que el sufijo de curva elíptica no es necesario y se reemplaza por el nuevo orden de prioridad de curva elíptica, cuando se proporciona, para permitir que las organizaciones usen la Directiva de grupo para configurar diferentes versiones de Windows con los mismos conjuntos de cifrado.</span><span class="sxs-lookup"><span data-stu-id="7e402-155">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="7e402-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7e402-156">See Also</span></span>

[<span data-ttu-id="7e402-157">Configuración del orden de las curvas ECC de TLS</span><span class="sxs-lookup"><span data-stu-id="7e402-157">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="7e402-158">Administrar el orden ECC de TLS</span><span class="sxs-lookup"><span data-stu-id="7e402-158">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="7e402-159">Administrar curvas ECC de Windows mediante directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="7e402-159">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="7e402-160">Cmdlets de TLS</span><span class="sxs-lookup"><span data-stu-id="7e402-160">TLS cmdlets</span></span>](/powershell/module/tls)
