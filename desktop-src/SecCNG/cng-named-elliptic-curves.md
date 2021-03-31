---
description: A partir de Windows 10, CNG proporciona compatibilidad para las siguientes curvas elípticas con nombre (ANSI X 9.62, X 9.63, FIPS 186-2).
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: Curvas elípticas con nombre de CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35092d463e6f83917d231a87659e690ffeb59fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907652"
---
# <a name="cng-named-elliptic-curves"></a><span data-ttu-id="612bb-103">Curvas elípticas con nombre CNG</span><span class="sxs-lookup"><span data-stu-id="612bb-103">CNG Named Elliptic Curves</span></span>

<span data-ttu-id="612bb-104">A partir de Windows 10, CNG proporciona compatibilidad para las siguientes curvas elípticas con nombre (ANSI X 9.62, X 9.63, FIPS 186-2).</span><span class="sxs-lookup"><span data-stu-id="612bb-104">Beginning in Windows 10, CNG provides support for the following named elliptic curves (ANSI X9.62, X9.63, FIPS 186-2).</span></span>

<dl> <span data-ttu-id="612bb-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**La \_ curva de ECC BCRYPT \_ \_ 25519**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT\_ECC\_CURVE\_25519**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-106">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-106">Requirement</span></span> | <span data-ttu-id="612bb-107">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-107">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="612bb-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-108">Name</span></span>              | <span data-ttu-id="612bb-109">curve25519</span><span class="sxs-lookup"><span data-stu-id="612bb-109">curve25519</span></span>                                                  |
| <span data-ttu-id="612bb-110">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-110">Standard</span></span>          | [<span data-ttu-id="612bb-111">Curva 25519</span><span class="sxs-lookup"><span data-stu-id="612bb-111">Curve 25519</span></span>](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| <span data-ttu-id="612bb-112">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-112">Key size (bits)</span></span>   | <span data-ttu-id="612bb-113">255</span><span class="sxs-lookup"><span data-stu-id="612bb-113">255</span></span>                                                         |
| <span data-ttu-id="612bb-114">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-114">TLS capable</span></span>       |                                                             |
| <span data-ttu-id="612bb-115">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-115">Object identifier</span></span> | <span data-ttu-id="612bb-116">None</span><span class="sxs-lookup"><span data-stu-id="612bb-116">None</span></span>                                                        |



 

<span data-ttu-id="612bb-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**\_BRAINPOOLP160R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-118">Requirement</span></span> | <span data-ttu-id="612bb-119">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-120">Name</span></span>              | <span data-ttu-id="612bb-121">brainpoolP160r1</span><span class="sxs-lookup"><span data-stu-id="612bb-121">brainpoolP160r1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-122">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-122">Standard</span></span>          | [<span data-ttu-id="612bb-123">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-123">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-124">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-124">Key size (bits)</span></span>   | <span data-ttu-id="612bb-125">160</span><span class="sxs-lookup"><span data-stu-id="612bb-125">160</span></span>                                                                                                               |
| <span data-ttu-id="612bb-126">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-126">TLS capable</span></span>       | <span data-ttu-id="612bb-127">No</span><span class="sxs-lookup"><span data-stu-id="612bb-127">No</span></span>                                                                                                                |
| <span data-ttu-id="612bb-128">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-128">Object identifier</span></span> | <span data-ttu-id="612bb-129">1.3.36.3.3.2.8.1.1.1</span><span class="sxs-lookup"><span data-stu-id="612bb-129">1.3.36.3.3.2.8.1.1.1</span></span>                                                                                              |



 

<span data-ttu-id="612bb-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP160T1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-131">Requirement</span></span> | <span data-ttu-id="612bb-132">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-133">Name</span></span>              | <span data-ttu-id="612bb-134">brainpoolP160t1</span><span class="sxs-lookup"><span data-stu-id="612bb-134">brainpoolP160t1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-135">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-135">Standard</span></span>          | [<span data-ttu-id="612bb-136">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-136">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-137">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-137">Key size (bits)</span></span>   | <span data-ttu-id="612bb-138">160</span><span class="sxs-lookup"><span data-stu-id="612bb-138">160</span></span>                                                                                                               |
| <span data-ttu-id="612bb-139">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-139">TLS capable</span></span>       | <span data-ttu-id="612bb-140">No</span><span class="sxs-lookup"><span data-stu-id="612bb-140">No</span></span>                                                                                                                |
| <span data-ttu-id="612bb-141">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-141">Object identifier</span></span> | <span data-ttu-id="612bb-142">1.3.36.3.3.2.8.1.1.2</span><span class="sxs-lookup"><span data-stu-id="612bb-142">1.3.36.3.3.2.8.1.1.2</span></span>                                                                                              |



 

<span data-ttu-id="612bb-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**\_BRAINPOOLP192R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-144">Requirement</span></span> | <span data-ttu-id="612bb-145">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-145">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-146">Name</span></span>              | <span data-ttu-id="612bb-147">brainpoolP192r1</span><span class="sxs-lookup"><span data-stu-id="612bb-147">brainpoolP192r1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-148">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-148">Standard</span></span>          | [<span data-ttu-id="612bb-149">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-149">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-150">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-150">Key size (bits)</span></span>   | <span data-ttu-id="612bb-151">192</span><span class="sxs-lookup"><span data-stu-id="612bb-151">192</span></span>                                                                                                               |
| <span data-ttu-id="612bb-152">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-152">TLS capable</span></span>       | <span data-ttu-id="612bb-153">No</span><span class="sxs-lookup"><span data-stu-id="612bb-153">No</span></span>                                                                                                                |
| <span data-ttu-id="612bb-154">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-154">Object identifier</span></span> | <span data-ttu-id="612bb-155">1.3.36.3.3.2.8.1.1.3</span><span class="sxs-lookup"><span data-stu-id="612bb-155">1.3.36.3.3.2.8.1.1.3</span></span>                                                                                              |



 

<span data-ttu-id="612bb-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**\_BRAINPOOLP192T1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-157">Requirement</span></span> | <span data-ttu-id="612bb-158">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-159">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-159">Name</span></span>              | <span data-ttu-id="612bb-160">brainpoolP192t1</span><span class="sxs-lookup"><span data-stu-id="612bb-160">brainpoolP192t1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-161">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-161">Standard</span></span>          | [<span data-ttu-id="612bb-162">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-162">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-163">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-163">Key size (bits)</span></span>   | <span data-ttu-id="612bb-164">192</span><span class="sxs-lookup"><span data-stu-id="612bb-164">192</span></span>                                                                                                               |
| <span data-ttu-id="612bb-165">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-165">TLS capable</span></span>       | <span data-ttu-id="612bb-166">No</span><span class="sxs-lookup"><span data-stu-id="612bb-166">No</span></span>                                                                                                                |
| <span data-ttu-id="612bb-167">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-167">Object identifier</span></span> | <span data-ttu-id="612bb-168">1.3.36.3.3.2.8.1.1.4</span><span class="sxs-lookup"><span data-stu-id="612bb-168">1.3.36.3.3.2.8.1.1.4</span></span>                                                                                              |



 

<span data-ttu-id="612bb-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**\_BRAINPOOLP224R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-170">Requirement</span></span> | <span data-ttu-id="612bb-171">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-172">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-172">Name</span></span>              | <span data-ttu-id="612bb-173">brainpoolP224r1</span><span class="sxs-lookup"><span data-stu-id="612bb-173">brainpoolP224r1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-174">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-174">Standard</span></span>          | [<span data-ttu-id="612bb-175">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-175">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-176">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-176">Key size (bits)</span></span>   | <span data-ttu-id="612bb-177">224</span><span class="sxs-lookup"><span data-stu-id="612bb-177">224</span></span>                                                                                                               |
| <span data-ttu-id="612bb-178">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-178">TLS capable</span></span>       | <span data-ttu-id="612bb-179">No</span><span class="sxs-lookup"><span data-stu-id="612bb-179">No</span></span>                                                                                                                |
| <span data-ttu-id="612bb-180">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-180">Object identifier</span></span> | <span data-ttu-id="612bb-181">1.3.36.3.3.2.8.1.1.5</span><span class="sxs-lookup"><span data-stu-id="612bb-181">1.3.36.3.3.2.8.1.1.5</span></span>                                                                                              |



 

<span data-ttu-id="612bb-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**\_BRAINPOOLP224T1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-183">Requirement</span></span> | <span data-ttu-id="612bb-184">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-184">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-185">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-185">Name</span></span>              | <span data-ttu-id="612bb-186">brainpoolP224t1</span><span class="sxs-lookup"><span data-stu-id="612bb-186">brainpoolP224t1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-187">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-187">Standard</span></span>          | [<span data-ttu-id="612bb-188">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-188">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-189">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-189">Key size (bits)</span></span>   | <span data-ttu-id="612bb-190">224</span><span class="sxs-lookup"><span data-stu-id="612bb-190">224</span></span>                                                                                                               |
| <span data-ttu-id="612bb-191">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-191">TLS capable</span></span>       | <span data-ttu-id="612bb-192">No</span><span class="sxs-lookup"><span data-stu-id="612bb-192">No</span></span>                                                                                                                |
| <span data-ttu-id="612bb-193">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-193">Object identifier</span></span> | <span data-ttu-id="612bb-194">1.3.36.3.3.2.8.1.1.6</span><span class="sxs-lookup"><span data-stu-id="612bb-194">1.3.36.3.3.2.8.1.1.6</span></span>                                                                                              |



 

<span data-ttu-id="612bb-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**\_BRAINPOOLP256R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-196">Requirement</span></span> | <span data-ttu-id="612bb-197">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-197">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-198">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-198">Name</span></span>              | <span data-ttu-id="612bb-199">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="612bb-199">brainpoolP256r1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-200">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-200">Standard</span></span>          | [<span data-ttu-id="612bb-201">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-201">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-202">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-202">Key size (bits)</span></span>   | <span data-ttu-id="612bb-203">256</span><span class="sxs-lookup"><span data-stu-id="612bb-203">256</span></span>                                                                                                               |
| <span data-ttu-id="612bb-204">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-204">TLS capable</span></span>       | <span data-ttu-id="612bb-205">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-205">Yes</span></span>                                                                                                               |
| <span data-ttu-id="612bb-206">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-206">Object identifier</span></span> | <span data-ttu-id="612bb-207">1.3.36.3.3.2.8.1.1.7</span><span class="sxs-lookup"><span data-stu-id="612bb-207">1.3.36.3.3.2.8.1.1.7</span></span>                                                                                              |



 

<span data-ttu-id="612bb-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**\_BRAINPOOLP256T1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-209">Requirement</span></span> | <span data-ttu-id="612bb-210">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-210">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-211">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-211">Name</span></span>              | <span data-ttu-id="612bb-212">brainpoolP256t1</span><span class="sxs-lookup"><span data-stu-id="612bb-212">brainpoolP256t1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-213">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-213">Standard</span></span>          | [<span data-ttu-id="612bb-214">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-214">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-215">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-215">Key size (bits)</span></span>   | <span data-ttu-id="612bb-216">256</span><span class="sxs-lookup"><span data-stu-id="612bb-216">256</span></span>                                                                                                               |
| <span data-ttu-id="612bb-217">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-217">TLS capable</span></span>       | <span data-ttu-id="612bb-218">No</span><span class="sxs-lookup"><span data-stu-id="612bb-218">No</span></span>                                                                                                                |
| <span data-ttu-id="612bb-219">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-219">Object identifier</span></span> | <span data-ttu-id="612bb-220">1.3.36.3.3.2.8.1.1.8</span><span class="sxs-lookup"><span data-stu-id="612bb-220">1.3.36.3.3.2.8.1.1.8</span></span>                                                                                              |



 

<span data-ttu-id="612bb-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**\_BRAINPOOLP320R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP320R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-222">Requirement</span></span> | <span data-ttu-id="612bb-223">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-223">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-224">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-224">Name</span></span>              | <span data-ttu-id="612bb-225">brainpoolP320r1</span><span class="sxs-lookup"><span data-stu-id="612bb-225">brainpoolP320r1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-226">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-226">Standard</span></span>          | [<span data-ttu-id="612bb-227">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-227">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-228">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-228">Key size (bits)</span></span>   | <span data-ttu-id="612bb-229">320</span><span class="sxs-lookup"><span data-stu-id="612bb-229">320</span></span>                                                                                                               |
| <span data-ttu-id="612bb-230">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-230">TLS capable</span></span>       | <span data-ttu-id="612bb-231">No</span><span class="sxs-lookup"><span data-stu-id="612bb-231">No</span></span>                                                                                                                |
| <span data-ttu-id="612bb-232">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-232">Object identifier</span></span> | <span data-ttu-id="612bb-233">1.3.36.3.3.2.8.1.1.9</span><span class="sxs-lookup"><span data-stu-id="612bb-233">1.3.36.3.3.2.8.1.1.9</span></span>                                                                                              |



 

<span data-ttu-id="612bb-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP32 0T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP32 0T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-235">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-235">Requirement</span></span> | <span data-ttu-id="612bb-236">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-236">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-237">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-237">Name</span></span>              | <span data-ttu-id="612bb-238">brainpoolP320t1</span><span class="sxs-lookup"><span data-stu-id="612bb-238">brainpoolP320t1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-239">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-239">Standard</span></span>          | [<span data-ttu-id="612bb-240">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-240">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-241">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-241">Key size (bits)</span></span>   | <span data-ttu-id="612bb-242">320</span><span class="sxs-lookup"><span data-stu-id="612bb-242">320</span></span>                                                                                                               |
| <span data-ttu-id="612bb-243">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-243">TLS capable</span></span>       | <span data-ttu-id="612bb-244">No</span><span class="sxs-lookup"><span data-stu-id="612bb-244">No</span></span>                                                                                                                |
| <span data-ttu-id="612bb-245">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-245">Object identifier</span></span> | <span data-ttu-id="612bb-246">1.3.36.3.3.2.8.1.1.10</span><span class="sxs-lookup"><span data-stu-id="612bb-246">1.3.36.3.3.2.8.1.1.10</span></span>                                                                                             |



 

<span data-ttu-id="612bb-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP384R1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-248">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-248">Requirement</span></span> | <span data-ttu-id="612bb-249">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-249">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-250">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-250">Name</span></span>              | <span data-ttu-id="612bb-251">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="612bb-251">brainpoolP384r1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-252">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-252">Standard</span></span>          | [<span data-ttu-id="612bb-253">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-253">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-254">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-254">Key size (bits)</span></span>   | <span data-ttu-id="612bb-255">384</span><span class="sxs-lookup"><span data-stu-id="612bb-255">384</span></span>                                                                                                               |
| <span data-ttu-id="612bb-256">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-256">TLS capable</span></span>       | <span data-ttu-id="612bb-257">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-257">Yes</span></span>                                                                                                               |
| <span data-ttu-id="612bb-258">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-258">Object identifier</span></span> | <span data-ttu-id="612bb-259">1.3.36.3.3.2.8.1.1.11</span><span class="sxs-lookup"><span data-stu-id="612bb-259">1.3.36.3.3.2.8.1.1.11</span></span>                                                                                             |



 

<span data-ttu-id="612bb-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**\_BRAINPOOLP384T1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-261">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-261">Requirement</span></span> | <span data-ttu-id="612bb-262">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-262">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-263">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-263">Name</span></span>              | <span data-ttu-id="612bb-264">brainpoolP384t1</span><span class="sxs-lookup"><span data-stu-id="612bb-264">brainpoolP384t1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-265">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-265">Standard</span></span>          | [<span data-ttu-id="612bb-266">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-266">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-267">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-267">Key size (bits)</span></span>   | <span data-ttu-id="612bb-268">384</span><span class="sxs-lookup"><span data-stu-id="612bb-268">384</span></span>                                                                                                               |
| <span data-ttu-id="612bb-269">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-269">TLS capable</span></span>       | <span data-ttu-id="612bb-270">No</span><span class="sxs-lookup"><span data-stu-id="612bb-270">No</span></span>                                                                                                                |
| <span data-ttu-id="612bb-271">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-271">Object identifier</span></span> | <span data-ttu-id="612bb-272">1.3.36.3.3.2.8.1.1.12</span><span class="sxs-lookup"><span data-stu-id="612bb-272">1.3.36.3.3.2.8.1.1.12</span></span>                                                                                             |



 

<span data-ttu-id="612bb-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**\_BRAINPOOLP512R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-274">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-274">Requirement</span></span> | <span data-ttu-id="612bb-275">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-275">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-276">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-276">Name</span></span>              | <span data-ttu-id="612bb-277">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="612bb-277">brainpoolP512r1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-278">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-278">Standard</span></span>          | [<span data-ttu-id="612bb-279">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-279">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-280">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-280">Key size (bits)</span></span>   | <span data-ttu-id="612bb-281">512</span><span class="sxs-lookup"><span data-stu-id="612bb-281">512</span></span>                                                                                                               |
| <span data-ttu-id="612bb-282">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-282">TLS capable</span></span>       | <span data-ttu-id="612bb-283">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-283">Yes</span></span>                                                                                                               |
| <span data-ttu-id="612bb-284">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-284">Object identifier</span></span> | <span data-ttu-id="612bb-285">1.3.36.3.3.2.8.1.1.13</span><span class="sxs-lookup"><span data-stu-id="612bb-285">1.3.36.3.3.2.8.1.1.13</span></span>                                                                                             |



 

<span data-ttu-id="612bb-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**\_BRAINPOOLP512T1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-287">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-287">Requirement</span></span> | <span data-ttu-id="612bb-288">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-288">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-289">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-289">Name</span></span>              | <span data-ttu-id="612bb-290">brainpoolP512t1</span><span class="sxs-lookup"><span data-stu-id="612bb-290">brainpoolP512t1</span></span>                                                                                                   |
| <span data-ttu-id="612bb-291">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-291">Standard</span></span>          | [<span data-ttu-id="612bb-292">Curvas estándar de ECC Brainpool y generación de curvas</span><span class="sxs-lookup"><span data-stu-id="612bb-292">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="612bb-293">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-293">Key size (bits)</span></span>   | <span data-ttu-id="612bb-294">512</span><span class="sxs-lookup"><span data-stu-id="612bb-294">512</span></span>                                                                                                               |
| <span data-ttu-id="612bb-295">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-295">TLS capable</span></span>       | <span data-ttu-id="612bb-296">No</span><span class="sxs-lookup"><span data-stu-id="612bb-296">No</span></span>                                                                                                                |
| <span data-ttu-id="612bb-297">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-297">Object identifier</span></span> | <span data-ttu-id="612bb-298">1.3.36.3.3.2.8.1.1.14</span><span class="sxs-lookup"><span data-stu-id="612bb-298">1.3.36.3.3.2.8.1.1.14</span></span>                                                                                             |



 

<span data-ttu-id="612bb-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ \_ \_ EC192WAPI de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT\_ECC\_CURVE\_EC192WAPI** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-300">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-300">Requirement</span></span> | <span data-ttu-id="612bb-301">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-301">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="612bb-302">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-302">Name</span></span>              | <span data-ttu-id="612bb-303">ec192wapi</span><span class="sxs-lookup"><span data-stu-id="612bb-303">ec192wapi</span></span>                                                      |
| <span data-ttu-id="612bb-304">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-304">Standard</span></span>          | <span data-ttu-id="612bb-305">Chino estándar nacional para LAN inalámbricas (GB 15629.11-2003)</span><span class="sxs-lookup"><span data-stu-id="612bb-305">Chinese National Standard for Wireless LANs (GB 15629.11-2003)</span></span> |
| <span data-ttu-id="612bb-306">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-306">Key size (bits)</span></span>   | <span data-ttu-id="612bb-307">192</span><span class="sxs-lookup"><span data-stu-id="612bb-307">192</span></span>                                                            |
| <span data-ttu-id="612bb-308">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-308">TLS capable</span></span>       | <span data-ttu-id="612bb-309">No</span><span class="sxs-lookup"><span data-stu-id="612bb-309">No</span></span>                                                             |
| <span data-ttu-id="612bb-310">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-310">Object identifier</span></span> | <span data-ttu-id="612bb-311">1.2.156.11235.1.1.2.1</span><span class="sxs-lookup"><span data-stu-id="612bb-311">1.2.156.11235.1.1.2.1</span></span>                                          |



 

<span data-ttu-id="612bb-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**\_NISTP192 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT\_ECC\_CURVE\_NISTP192**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-313">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-313">Requirement</span></span> | <span data-ttu-id="612bb-314">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-314">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-315">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-315">Name</span></span>              | <span data-ttu-id="612bb-316">nistP192</span><span class="sxs-lookup"><span data-stu-id="612bb-316">nistP192</span></span>                                                                                                                     |
| <span data-ttu-id="612bb-317">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-317">Standard</span></span>          | [<span data-ttu-id="612bb-318">Curvas elípticas recomendadas para uso del gobierno federal</span><span class="sxs-lookup"><span data-stu-id="612bb-318">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="612bb-319">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-319">Key size (bits)</span></span>   | <span data-ttu-id="612bb-320">192</span><span class="sxs-lookup"><span data-stu-id="612bb-320">192</span></span>                                                                                                                          |
| <span data-ttu-id="612bb-321">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-321">TLS capable</span></span>       | <span data-ttu-id="612bb-322">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-322">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="612bb-323">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-323">Object identifier</span></span> | <span data-ttu-id="612bb-324">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="612bb-324">1.2.840.10045.3.1.1</span></span>                                                                                                          |



 

<span data-ttu-id="612bb-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ \_ \_ NISTP224 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT\_ECC\_CURVE\_NISTP224** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-326">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-326">Requirement</span></span> | <span data-ttu-id="612bb-327">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-327">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-328">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-328">Name</span></span>              | <span data-ttu-id="612bb-329">nistP224</span><span class="sxs-lookup"><span data-stu-id="612bb-329">nistP224</span></span>                                                                                                                     |
| <span data-ttu-id="612bb-330">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-330">Standard</span></span>          | [<span data-ttu-id="612bb-331">Curvas elípticas recomendadas para uso del gobierno federal</span><span class="sxs-lookup"><span data-stu-id="612bb-331">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="612bb-332">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-332">Key size (bits)</span></span>   | <span data-ttu-id="612bb-333">224</span><span class="sxs-lookup"><span data-stu-id="612bb-333">224</span></span>                                                                                                                          |
| <span data-ttu-id="612bb-334">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-334">TLS capable</span></span>       | <span data-ttu-id="612bb-335">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-335">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="612bb-336">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-336">Object identifier</span></span> | <span data-ttu-id="612bb-337">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="612bb-337">1.3.132.0.33</span></span>                                                                                                                 |



 

<span data-ttu-id="612bb-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**\_NISTP256 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT\_ECC\_CURVE\_NISTP256**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-339">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-339">Requirement</span></span> | <span data-ttu-id="612bb-340">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-340">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-341">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-341">Name</span></span>              | <span data-ttu-id="612bb-342">nistP256</span><span class="sxs-lookup"><span data-stu-id="612bb-342">nistP256</span></span>                                                                                                                     |
| <span data-ttu-id="612bb-343">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-343">Standard</span></span>          | [<span data-ttu-id="612bb-344">Curvas elípticas recomendadas para uso del gobierno federal</span><span class="sxs-lookup"><span data-stu-id="612bb-344">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="612bb-345">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-345">Key size (bits)</span></span>   | <span data-ttu-id="612bb-346">256</span><span class="sxs-lookup"><span data-stu-id="612bb-346">256</span></span>                                                                                                                          |
| <span data-ttu-id="612bb-347">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-347">TLS capable</span></span>       | <span data-ttu-id="612bb-348">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-348">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="612bb-349">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-349">Object identifier</span></span> | <span data-ttu-id="612bb-350">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="612bb-350">1.2.840.10045.3.1.7</span></span>                                                                                                          |



 

<span data-ttu-id="612bb-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ \_ \_ NISTP384 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT\_ECC\_CURVE\_NISTP384** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-352">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-352">Requirement</span></span> | <span data-ttu-id="612bb-353">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-353">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-354">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-354">Name</span></span>              | <span data-ttu-id="612bb-355">nistP384</span><span class="sxs-lookup"><span data-stu-id="612bb-355">nistP384</span></span>                                                                                                                     |
| <span data-ttu-id="612bb-356">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-356">Standard</span></span>          | [<span data-ttu-id="612bb-357">Curvas elípticas recomendadas para uso del gobierno federal</span><span class="sxs-lookup"><span data-stu-id="612bb-357">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="612bb-358">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-358">Key size (bits)</span></span>   | <span data-ttu-id="612bb-359">384</span><span class="sxs-lookup"><span data-stu-id="612bb-359">384</span></span>                                                                                                                          |
| <span data-ttu-id="612bb-360">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-360">TLS capable</span></span>       | <span data-ttu-id="612bb-361">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-361">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="612bb-362">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-362">Object identifier</span></span> | <span data-ttu-id="612bb-363">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="612bb-363">1.3.132.0.34</span></span>                                                                                                                 |



 

<span data-ttu-id="612bb-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**\_NISTP521 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT\_ECC\_CURVE\_NISTP521**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-365">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-365">Requirement</span></span> | <span data-ttu-id="612bb-366">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-366">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-367">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-367">Name</span></span>              | <span data-ttu-id="612bb-368">nistP521</span><span class="sxs-lookup"><span data-stu-id="612bb-368">nistP521</span></span>                                                                                                                     |
| <span data-ttu-id="612bb-369">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-369">Standard</span></span>          | [<span data-ttu-id="612bb-370">Curvas elípticas recomendadas para uso del gobierno federal</span><span class="sxs-lookup"><span data-stu-id="612bb-370">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="612bb-371">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-371">Key size (bits)</span></span>   | <span data-ttu-id="612bb-372">521</span><span class="sxs-lookup"><span data-stu-id="612bb-372">521</span></span>                                                                                                                          |
| <span data-ttu-id="612bb-373">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-373">TLS capable</span></span>       | <span data-ttu-id="612bb-374">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-374">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="612bb-375">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-375">Object identifier</span></span> | <span data-ttu-id="612bb-376">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="612bb-376">1.3.132.0.35</span></span>                                                                                                                 |



 

<span data-ttu-id="612bb-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ \_ \_ NUMSP256T1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP256T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-378">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-378">Requirement</span></span> | <span data-ttu-id="612bb-379">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-379">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-380">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-380">Name</span></span>              | <span data-ttu-id="612bb-381">numsP256t1</span><span class="sxs-lookup"><span data-stu-id="612bb-381">numsP256t1</span></span>                                                                                                                              |
| <span data-ttu-id="612bb-382">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-382">Standard</span></span>          | [<span data-ttu-id="612bb-383">Especificación de selección de curva y parámetros de curva admitidos en MSR ECCLib</span><span class="sxs-lookup"><span data-stu-id="612bb-383">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="612bb-384">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-384">Key size (bits)</span></span>   | <span data-ttu-id="612bb-385">256</span><span class="sxs-lookup"><span data-stu-id="612bb-385">256</span></span>                                                                                                                                     |
| <span data-ttu-id="612bb-386">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-386">TLS capable</span></span>       | <span data-ttu-id="612bb-387">No</span><span class="sxs-lookup"><span data-stu-id="612bb-387">No</span></span>                                                                                                                                      |
| <span data-ttu-id="612bb-388">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-388">Object identifier</span></span> | <span data-ttu-id="612bb-389">None</span><span class="sxs-lookup"><span data-stu-id="612bb-389">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="612bb-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ \_ \_ NUMSP384T1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP384T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-391">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-391">Requirement</span></span> | <span data-ttu-id="612bb-392">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-392">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-393">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-393">Name</span></span>              | <span data-ttu-id="612bb-394">numsP384t1</span><span class="sxs-lookup"><span data-stu-id="612bb-394">numsP384t1</span></span>                                                                                                                              |
| <span data-ttu-id="612bb-395">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-395">Standard</span></span>          | [<span data-ttu-id="612bb-396">Especificación de selección de curva y parámetros de curva admitidos en MSR ECCLib</span><span class="sxs-lookup"><span data-stu-id="612bb-396">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="612bb-397">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-397">Key size (bits)</span></span>   | <span data-ttu-id="612bb-398">384</span><span class="sxs-lookup"><span data-stu-id="612bb-398">384</span></span>                                                                                                                                     |
| <span data-ttu-id="612bb-399">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-399">TLS capable</span></span>       | <span data-ttu-id="612bb-400">No</span><span class="sxs-lookup"><span data-stu-id="612bb-400">No</span></span>                                                                                                                                      |
| <span data-ttu-id="612bb-401">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-401">Object identifier</span></span> | <span data-ttu-id="612bb-402">None</span><span class="sxs-lookup"><span data-stu-id="612bb-402">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="612bb-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**\_NUMSP512T1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT\_ECC\_CURVE\_NUMSP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-404">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-404">Requirement</span></span> | <span data-ttu-id="612bb-405">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-405">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-406">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-406">Name</span></span>              | <span data-ttu-id="612bb-407">numsP512t1</span><span class="sxs-lookup"><span data-stu-id="612bb-407">numsP512t1</span></span>                                                                                                                              |
| <span data-ttu-id="612bb-408">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-408">Standard</span></span>          | [<span data-ttu-id="612bb-409">Especificación de selección de curva y parámetros de curva admitidos en MSR ECCLib</span><span class="sxs-lookup"><span data-stu-id="612bb-409">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="612bb-410">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-410">Key size (bits)</span></span>   | <span data-ttu-id="612bb-411">512</span><span class="sxs-lookup"><span data-stu-id="612bb-411">512</span></span>                                                                                                                                     |
| <span data-ttu-id="612bb-412">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-412">TLS capable</span></span>       | <span data-ttu-id="612bb-413">No</span><span class="sxs-lookup"><span data-stu-id="612bb-413">No</span></span>                                                                                                                                      |
| <span data-ttu-id="612bb-414">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-414">Object identifier</span></span> | <span data-ttu-id="612bb-415">None</span><span class="sxs-lookup"><span data-stu-id="612bb-415">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="612bb-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ \_ \_ SECP160K1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160K1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-417">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-417">Requirement</span></span> | <span data-ttu-id="612bb-418">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-418">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-419">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-419">Name</span></span>              | <span data-ttu-id="612bb-420">secP160k1</span><span class="sxs-lookup"><span data-stu-id="612bb-420">secP160k1</span></span>                                                                       |
| <span data-ttu-id="612bb-421">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-421">Standard</span></span>          | [<span data-ttu-id="612bb-422">Parámetros de dominio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="612bb-422">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="612bb-423">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-423">Key size (bits)</span></span>   | <span data-ttu-id="612bb-424">160</span><span class="sxs-lookup"><span data-stu-id="612bb-424">160</span></span>                                                                             |
| <span data-ttu-id="612bb-425">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-425">TLS capable</span></span>       | <span data-ttu-id="612bb-426">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-426">Yes</span></span>                                                                             |
| <span data-ttu-id="612bb-427">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-427">Object identifier</span></span> | <span data-ttu-id="612bb-428">1.3.132.0.9</span><span class="sxs-lookup"><span data-stu-id="612bb-428">1.3.132.0.9</span></span>                                                                     |



 

<span data-ttu-id="612bb-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-430">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-430">Requirement</span></span> | <span data-ttu-id="612bb-431">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-431">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-432">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-432">Name</span></span>              | <span data-ttu-id="612bb-433">secP160r1</span><span class="sxs-lookup"><span data-stu-id="612bb-433">secP160r1</span></span>                                                                       |
| <span data-ttu-id="612bb-434">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-434">Standard</span></span>          | [<span data-ttu-id="612bb-435">Parámetros de dominio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="612bb-435">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="612bb-436">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-436">Key size (bits)</span></span>   | <span data-ttu-id="612bb-437">160</span><span class="sxs-lookup"><span data-stu-id="612bb-437">160</span></span>                                                                             |
| <span data-ttu-id="612bb-438">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-438">TLS capable</span></span>       | <span data-ttu-id="612bb-439">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-439">Yes</span></span>                                                                             |
| <span data-ttu-id="612bb-440">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-440">Object identifier</span></span> | <span data-ttu-id="612bb-441">1.3.132.0.8</span><span class="sxs-lookup"><span data-stu-id="612bb-441">1.3.132.0.8</span></span>                                                                     |



 

<span data-ttu-id="612bb-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-443">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-443">Requirement</span></span> | <span data-ttu-id="612bb-444">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-444">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-445">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-445">Name</span></span>              | <span data-ttu-id="612bb-446">secP160r2</span><span class="sxs-lookup"><span data-stu-id="612bb-446">secP160r2</span></span>                                                                       |
| <span data-ttu-id="612bb-447">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-447">Standard</span></span>          | [<span data-ttu-id="612bb-448">Parámetros de dominio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="612bb-448">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="612bb-449">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-449">Key size (bits)</span></span>   | <span data-ttu-id="612bb-450">160</span><span class="sxs-lookup"><span data-stu-id="612bb-450">160</span></span>                                                                             |
| <span data-ttu-id="612bb-451">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-451">TLS capable</span></span>       | <span data-ttu-id="612bb-452">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-452">Yes</span></span>                                                                             |
| <span data-ttu-id="612bb-453">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-453">Object identifier</span></span> | <span data-ttu-id="612bb-454">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="612bb-454">1.3.132.0.30</span></span>                                                                    |



 

<span data-ttu-id="612bb-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**\_SECP192K1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT\_ECC\_CURVE\_SECP192K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-456">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-456">Requirement</span></span> | <span data-ttu-id="612bb-457">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-457">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-458">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-458">Name</span></span>              | <span data-ttu-id="612bb-459">secP192k1</span><span class="sxs-lookup"><span data-stu-id="612bb-459">secP192k1</span></span>                                                                       |
| <span data-ttu-id="612bb-460">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-460">Standard</span></span>          | [<span data-ttu-id="612bb-461">Parámetros de dominio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="612bb-461">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="612bb-462">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-462">Key size (bits)</span></span>   | <span data-ttu-id="612bb-463">192</span><span class="sxs-lookup"><span data-stu-id="612bb-463">192</span></span>                                                                             |
| <span data-ttu-id="612bb-464">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-464">TLS capable</span></span>       | <span data-ttu-id="612bb-465">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-465">Yes</span></span>                                                                             |
| <span data-ttu-id="612bb-466">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-466">Object identifier</span></span> | <span data-ttu-id="612bb-467">1.3.132.0.31</span><span class="sxs-lookup"><span data-stu-id="612bb-467">1.3.132.0.31</span></span>                                                                    |



 

<span data-ttu-id="612bb-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ \_ \_ SECP192R1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP192R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-469">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-469">Requirement</span></span> | <span data-ttu-id="612bb-470">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-470">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-471">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-471">Name</span></span>              | <span data-ttu-id="612bb-472">secP192r1</span><span class="sxs-lookup"><span data-stu-id="612bb-472">secP192r1</span></span>                                                                       |
| <span data-ttu-id="612bb-473">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-473">Standard</span></span>          | [<span data-ttu-id="612bb-474">Parámetros de dominio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="612bb-474">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="612bb-475">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-475">Key size (bits)</span></span>   | <span data-ttu-id="612bb-476">192</span><span class="sxs-lookup"><span data-stu-id="612bb-476">192</span></span>                                                                             |
| <span data-ttu-id="612bb-477">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-477">TLS capable</span></span>       | <span data-ttu-id="612bb-478">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-478">Yes</span></span>                                                                             |
| <span data-ttu-id="612bb-479">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-479">Object identifier</span></span> | <span data-ttu-id="612bb-480">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="612bb-480">1.2.840.10045.3.1.1</span></span>                                                             |



 

<span data-ttu-id="612bb-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**\_SECP224K1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT\_ECC\_CURVE\_SECP224K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-482">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-482">Requirement</span></span> | <span data-ttu-id="612bb-483">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-483">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-484">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-484">Name</span></span>              | <span data-ttu-id="612bb-485">secP224k1</span><span class="sxs-lookup"><span data-stu-id="612bb-485">secP224k1</span></span>                                                                       |
| <span data-ttu-id="612bb-486">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-486">Standard</span></span>          | [<span data-ttu-id="612bb-487">Parámetros de dominio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="612bb-487">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="612bb-488">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-488">Key size (bits)</span></span>   | <span data-ttu-id="612bb-489">224</span><span class="sxs-lookup"><span data-stu-id="612bb-489">224</span></span>                                                                             |
| <span data-ttu-id="612bb-490">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-490">TLS capable</span></span>       | <span data-ttu-id="612bb-491">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-491">Yes</span></span>                                                                             |
| <span data-ttu-id="612bb-492">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-492">Object identifier</span></span> | <span data-ttu-id="612bb-493">1.3.132.0.32</span><span class="sxs-lookup"><span data-stu-id="612bb-493">1.3.132.0.32</span></span>                                                                    |



 

<span data-ttu-id="612bb-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**\_SECP224R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT\_ECC\_CURVE\_SECP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-495">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-495">Requirement</span></span> | <span data-ttu-id="612bb-496">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-496">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-497">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-497">Name</span></span>              | <span data-ttu-id="612bb-498">secP224r1</span><span class="sxs-lookup"><span data-stu-id="612bb-498">secP224r1</span></span>                                                                       |
| <span data-ttu-id="612bb-499">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-499">Standard</span></span>          | [<span data-ttu-id="612bb-500">Parámetros de dominio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="612bb-500">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="612bb-501">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-501">Key size (bits)</span></span>   | <span data-ttu-id="612bb-502">224</span><span class="sxs-lookup"><span data-stu-id="612bb-502">224</span></span>                                                                             |
| <span data-ttu-id="612bb-503">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-503">TLS capable</span></span>       | <span data-ttu-id="612bb-504">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-504">Yes</span></span>                                                                             |
| <span data-ttu-id="612bb-505">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-505">Object identifier</span></span> | <span data-ttu-id="612bb-506">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="612bb-506">1.3.132.0.33</span></span>                                                                    |



 

<span data-ttu-id="612bb-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**\_SECP256K1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT\_ECC\_CURVE\_SECP256K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-508">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-508">Requirement</span></span> | <span data-ttu-id="612bb-509">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-509">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-510">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-510">Name</span></span>              | <span data-ttu-id="612bb-511">secP256k1</span><span class="sxs-lookup"><span data-stu-id="612bb-511">secP256k1</span></span>                                                                       |
| <span data-ttu-id="612bb-512">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-512">Standard</span></span>          | [<span data-ttu-id="612bb-513">Parámetros de dominio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="612bb-513">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="612bb-514">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-514">Key size (bits)</span></span>   | <span data-ttu-id="612bb-515">256</span><span class="sxs-lookup"><span data-stu-id="612bb-515">256</span></span>                                                                             |
| <span data-ttu-id="612bb-516">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-516">TLS capable</span></span>       | <span data-ttu-id="612bb-517">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-517">Yes</span></span>                                                                             |
| <span data-ttu-id="612bb-518">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-518">Object identifier</span></span> | <span data-ttu-id="612bb-519">1.3.132.0.10</span><span class="sxs-lookup"><span data-stu-id="612bb-519">1.3.132.0.10</span></span>                                                                    |



 

<span data-ttu-id="612bb-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**\_SECP256R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT\_ECC\_CURVE\_SECP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-521">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-521">Requirement</span></span> | <span data-ttu-id="612bb-522">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-522">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-523">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-523">Name</span></span>              | <span data-ttu-id="612bb-524">secP256r1</span><span class="sxs-lookup"><span data-stu-id="612bb-524">secP256r1</span></span>                                                                       |
| <span data-ttu-id="612bb-525">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-525">Standard</span></span>          | [<span data-ttu-id="612bb-526">Parámetros de dominio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="612bb-526">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="612bb-527">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-527">Key size (bits)</span></span>   | <span data-ttu-id="612bb-528">256</span><span class="sxs-lookup"><span data-stu-id="612bb-528">256</span></span>                                                                             |
| <span data-ttu-id="612bb-529">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-529">TLS capable</span></span>       | <span data-ttu-id="612bb-530">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-530">Yes</span></span>                                                                             |
| <span data-ttu-id="612bb-531">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-531">Object identifier</span></span> | <span data-ttu-id="612bb-532">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="612bb-532">1.2.840.10045.3.1.7</span></span>                                                             |



 

<span data-ttu-id="612bb-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ \_ \_ SECP384R1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-534">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-534">Requirement</span></span> | <span data-ttu-id="612bb-535">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-535">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-536">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-536">Name</span></span>              | <span data-ttu-id="612bb-537">secP384r1</span><span class="sxs-lookup"><span data-stu-id="612bb-537">secP384r1</span></span>                                                                       |
| <span data-ttu-id="612bb-538">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-538">Standard</span></span>          | [<span data-ttu-id="612bb-539">Parámetros de dominio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="612bb-539">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="612bb-540">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-540">Key size (bits)</span></span>   | <span data-ttu-id="612bb-541">384</span><span class="sxs-lookup"><span data-stu-id="612bb-541">384</span></span>                                                                             |
| <span data-ttu-id="612bb-542">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-542">TLS capable</span></span>       | <span data-ttu-id="612bb-543">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-543">Yes</span></span>                                                                             |
| <span data-ttu-id="612bb-544">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-544">Object identifier</span></span> | <span data-ttu-id="612bb-545">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="612bb-545">1.3.132.0.34</span></span>                                                                    |



 

<span data-ttu-id="612bb-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**\_SECP521R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT\_ECC\_CURVE\_SECP521R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-547">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-547">Requirement</span></span> | <span data-ttu-id="612bb-548">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-548">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-549">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-549">Name</span></span>              | <span data-ttu-id="612bb-550">secP521r1</span><span class="sxs-lookup"><span data-stu-id="612bb-550">secP521r1</span></span>                                                                       |
| <span data-ttu-id="612bb-551">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-551">Standard</span></span>          | [<span data-ttu-id="612bb-552">Parámetros de dominio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="612bb-552">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="612bb-553">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-553">Key size (bits)</span></span>   | <span data-ttu-id="612bb-554">521</span><span class="sxs-lookup"><span data-stu-id="612bb-554">521</span></span>                                                                             |
| <span data-ttu-id="612bb-555">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-555">TLS capable</span></span>       | <span data-ttu-id="612bb-556">Sí</span><span class="sxs-lookup"><span data-stu-id="612bb-556">Yes</span></span>                                                                             |
| <span data-ttu-id="612bb-557">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-557">Object identifier</span></span> | <span data-ttu-id="612bb-558">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="612bb-558">1.3.132.0.35</span></span>                                                                    |



 

<span data-ttu-id="612bb-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**\_WTLS12 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT\_ECC\_CURVE\_WTLS12**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-560">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-560">Requirement</span></span> | <span data-ttu-id="612bb-561">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-561">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="612bb-562">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-562">Name</span></span>              | <span data-ttu-id="612bb-563">wtls12</span><span class="sxs-lookup"><span data-stu-id="612bb-563">wtls12</span></span>       |
| <span data-ttu-id="612bb-564">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-564">Standard</span></span>          | <span data-ttu-id="612bb-565">WTLS</span><span class="sxs-lookup"><span data-stu-id="612bb-565">WTLS</span></span>         |
| <span data-ttu-id="612bb-566">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-566">Key size (bits)</span></span>   | <span data-ttu-id="612bb-567">224</span><span class="sxs-lookup"><span data-stu-id="612bb-567">224</span></span>          |
| <span data-ttu-id="612bb-568">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-568">TLS capable</span></span>       | <span data-ttu-id="612bb-569">No</span><span class="sxs-lookup"><span data-stu-id="612bb-569">No</span></span>           |
| <span data-ttu-id="612bb-570">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-570">Object identifier</span></span> | <span data-ttu-id="612bb-571">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="612bb-571">1.3.132.0.33</span></span> |



 

<span data-ttu-id="612bb-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**\_WTLS7 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT\_ECC\_CURVE\_WTLS7**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-573">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-573">Requirement</span></span> | <span data-ttu-id="612bb-574">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-574">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="612bb-575">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-575">Name</span></span>              | <span data-ttu-id="612bb-576">wtls7</span><span class="sxs-lookup"><span data-stu-id="612bb-576">wtls7</span></span>        |
| <span data-ttu-id="612bb-577">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-577">Standard</span></span>          | <span data-ttu-id="612bb-578">WTLS</span><span class="sxs-lookup"><span data-stu-id="612bb-578">WTLS</span></span>         |
| <span data-ttu-id="612bb-579">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-579">Key size (bits)</span></span>   | <span data-ttu-id="612bb-580">160</span><span class="sxs-lookup"><span data-stu-id="612bb-580">160</span></span>          |
| <span data-ttu-id="612bb-581">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-581">TLS capable</span></span>       | <span data-ttu-id="612bb-582">No</span><span class="sxs-lookup"><span data-stu-id="612bb-582">No</span></span>           |
| <span data-ttu-id="612bb-583">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-583">Object identifier</span></span> | <span data-ttu-id="612bb-584">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="612bb-584">1.3.132.0.30</span></span> |



 

<span data-ttu-id="612bb-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ \_ \_ WTLS9 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT\_ECC\_CURVE\_WTLS9** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-586">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-586">Requirement</span></span> | <span data-ttu-id="612bb-587">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-587">Value</span></span> |
|-------------------|---------------|
| <span data-ttu-id="612bb-588">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-588">Name</span></span>              | <span data-ttu-id="612bb-589">wtls9</span><span class="sxs-lookup"><span data-stu-id="612bb-589">wtls9</span></span>         |
| <span data-ttu-id="612bb-590">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-590">Standard</span></span>          | <span data-ttu-id="612bb-591">WTLS</span><span class="sxs-lookup"><span data-stu-id="612bb-591">WTLS</span></span>          |
| <span data-ttu-id="612bb-592">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-592">Key size (bits)</span></span>   | <span data-ttu-id="612bb-593">160</span><span class="sxs-lookup"><span data-stu-id="612bb-593">160</span></span>           |
| <span data-ttu-id="612bb-594">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-594">TLS capable</span></span>       | <span data-ttu-id="612bb-595">No</span><span class="sxs-lookup"><span data-stu-id="612bb-595">No</span></span>            |
| <span data-ttu-id="612bb-596">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-596">Object identifier</span></span> | <span data-ttu-id="612bb-597">2.23.43.1.4.9</span><span class="sxs-lookup"><span data-stu-id="612bb-597">2.23.43.1.4.9</span></span> |



 

<span data-ttu-id="612bb-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**\_X962P192V1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT\_ECC\_CURVE\_X962P192V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-599">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-599">Requirement</span></span> | <span data-ttu-id="612bb-600">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-600">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="612bb-601">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-601">Name</span></span>              | <span data-ttu-id="612bb-602">x962P192v1</span><span class="sxs-lookup"><span data-stu-id="612bb-602">x962P192v1</span></span>          |
| <span data-ttu-id="612bb-603">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-603">Standard</span></span>          | <span data-ttu-id="612bb-604">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="612bb-604">ANSI X9.62</span></span>          |
| <span data-ttu-id="612bb-605">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-605">Key size (bits)</span></span>   | <span data-ttu-id="612bb-606">192</span><span class="sxs-lookup"><span data-stu-id="612bb-606">192</span></span>                 |
| <span data-ttu-id="612bb-607">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-607">TLS capable</span></span>       | <span data-ttu-id="612bb-608">No</span><span class="sxs-lookup"><span data-stu-id="612bb-608">No</span></span>                  |
| <span data-ttu-id="612bb-609">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-609">Object identifier</span></span> | <span data-ttu-id="612bb-610">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="612bb-610">1.2.840.10045.3.1.1</span></span> |



 

<span data-ttu-id="612bb-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ \_ \_ X962P192V2 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P192V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-612">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-612">Requirement</span></span> | <span data-ttu-id="612bb-613">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-613">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="612bb-614">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-614">Name</span></span>              | <span data-ttu-id="612bb-615">x962P192v2</span><span class="sxs-lookup"><span data-stu-id="612bb-615">x962P192v2</span></span>          |
| <span data-ttu-id="612bb-616">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-616">Standard</span></span>          | <span data-ttu-id="612bb-617">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="612bb-617">ANSI X9.62</span></span>          |
| <span data-ttu-id="612bb-618">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-618">Key size (bits)</span></span>   | <span data-ttu-id="612bb-619">192</span><span class="sxs-lookup"><span data-stu-id="612bb-619">192</span></span>                 |
| <span data-ttu-id="612bb-620">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-620">TLS capable</span></span>       | <span data-ttu-id="612bb-621">No</span><span class="sxs-lookup"><span data-stu-id="612bb-621">No</span></span>                  |
| <span data-ttu-id="612bb-622">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-622">Object identifier</span></span> | <span data-ttu-id="612bb-623">1.2.840.10045.3.1.2</span><span class="sxs-lookup"><span data-stu-id="612bb-623">1.2.840.10045.3.1.2</span></span> |



 

<span data-ttu-id="612bb-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**\_X962P192V3 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT\_ECC\_CURVE\_X962P192V3**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-625">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-625">Requirement</span></span> | <span data-ttu-id="612bb-626">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-626">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="612bb-627">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-627">Name</span></span>              | <span data-ttu-id="612bb-628">x962P192v3</span><span class="sxs-lookup"><span data-stu-id="612bb-628">x962P192v3</span></span>          |
| <span data-ttu-id="612bb-629">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-629">Standard</span></span>          | <span data-ttu-id="612bb-630">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="612bb-630">ANSI X9.62</span></span>          |
| <span data-ttu-id="612bb-631">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-631">Key size (bits)</span></span>   | <span data-ttu-id="612bb-632">192</span><span class="sxs-lookup"><span data-stu-id="612bb-632">192</span></span>                 |
| <span data-ttu-id="612bb-633">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-633">TLS capable</span></span>       | <span data-ttu-id="612bb-634">No</span><span class="sxs-lookup"><span data-stu-id="612bb-634">No</span></span>                  |
| <span data-ttu-id="612bb-635">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-635">Object identifier</span></span> | <span data-ttu-id="612bb-636">1.2.840.10045.3.1.3</span><span class="sxs-lookup"><span data-stu-id="612bb-636">1.2.840.10045.3.1.3</span></span> |



 

<span data-ttu-id="612bb-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ \_ \_ X962P239V1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-638">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-638">Requirement</span></span> | <span data-ttu-id="612bb-639">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-639">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="612bb-640">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-640">Name</span></span>              | <span data-ttu-id="612bb-641">x962P239v1</span><span class="sxs-lookup"><span data-stu-id="612bb-641">x962P239v1</span></span>          |
| <span data-ttu-id="612bb-642">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-642">Standard</span></span>          | <span data-ttu-id="612bb-643">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="612bb-643">ANSI X9.62</span></span>          |
| <span data-ttu-id="612bb-644">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-644">Key size (bits)</span></span>   | <span data-ttu-id="612bb-645">239</span><span class="sxs-lookup"><span data-stu-id="612bb-645">239</span></span>                 |
| <span data-ttu-id="612bb-646">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-646">TLS capable</span></span>       | <span data-ttu-id="612bb-647">No</span><span class="sxs-lookup"><span data-stu-id="612bb-647">No</span></span>                  |
| <span data-ttu-id="612bb-648">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-648">Object identifier</span></span> | <span data-ttu-id="612bb-649">1.2.840.10045.3.1.4</span><span class="sxs-lookup"><span data-stu-id="612bb-649">1.2.840.10045.3.1.4</span></span> |



 

<span data-ttu-id="612bb-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ \_ \_ X962P239V2 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-651">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-651">Requirement</span></span> | <span data-ttu-id="612bb-652">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-652">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="612bb-653">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-653">Name</span></span>              | <span data-ttu-id="612bb-654">x962P239v2</span><span class="sxs-lookup"><span data-stu-id="612bb-654">x962P239v2</span></span>          |
| <span data-ttu-id="612bb-655">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-655">Standard</span></span>          | <span data-ttu-id="612bb-656">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="612bb-656">ANSI X9.62</span></span>          |
| <span data-ttu-id="612bb-657">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-657">Key size (bits)</span></span>   | <span data-ttu-id="612bb-658">239</span><span class="sxs-lookup"><span data-stu-id="612bb-658">239</span></span>                 |
| <span data-ttu-id="612bb-659">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-659">TLS capable</span></span>       | <span data-ttu-id="612bb-660">No</span><span class="sxs-lookup"><span data-stu-id="612bb-660">No</span></span>                  |
| <span data-ttu-id="612bb-661">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-661">Object identifier</span></span> | <span data-ttu-id="612bb-662">1.2.840.10045.3.1.5</span><span class="sxs-lookup"><span data-stu-id="612bb-662">1.2.840.10045.3.1.5</span></span> |



 

<span data-ttu-id="612bb-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ \_ \_ X962P239V3 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V3** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-664">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-664">Requirement</span></span> | <span data-ttu-id="612bb-665">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-665">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="612bb-666">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-666">Name</span></span>              | <span data-ttu-id="612bb-667">x962P239v3</span><span class="sxs-lookup"><span data-stu-id="612bb-667">x962P239v3</span></span>          |
| <span data-ttu-id="612bb-668">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-668">Standard</span></span>          | <span data-ttu-id="612bb-669">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="612bb-669">ANSI X9.62</span></span>          |
| <span data-ttu-id="612bb-670">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-670">Key size (bits)</span></span>   | <span data-ttu-id="612bb-671">239</span><span class="sxs-lookup"><span data-stu-id="612bb-671">239</span></span>                 |
| <span data-ttu-id="612bb-672">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-672">TLS capable</span></span>       | <span data-ttu-id="612bb-673">No</span><span class="sxs-lookup"><span data-stu-id="612bb-673">No</span></span>                  |
| <span data-ttu-id="612bb-674">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-674">Object identifier</span></span> | <span data-ttu-id="612bb-675">1.2.840.10045.3.1.6</span><span class="sxs-lookup"><span data-stu-id="612bb-675">1.2.840.10045.3.1.6</span></span> |



 

<span data-ttu-id="612bb-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**\_X962P256V1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="612bb-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT\_ECC\_CURVE\_X962P256V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="612bb-677">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-677">Requirement</span></span> | <span data-ttu-id="612bb-678">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-678">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="612bb-679">Nombre</span><span class="sxs-lookup"><span data-stu-id="612bb-679">Name</span></span>              | <span data-ttu-id="612bb-680">x962P256v1</span><span class="sxs-lookup"><span data-stu-id="612bb-680">x962P256v1</span></span>          |
| <span data-ttu-id="612bb-681">Estándar</span><span class="sxs-lookup"><span data-stu-id="612bb-681">Standard</span></span>          | <span data-ttu-id="612bb-682">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="612bb-682">ANSI X9.62</span></span>          |
| <span data-ttu-id="612bb-683">Tamaño de la clave (bits)</span><span class="sxs-lookup"><span data-stu-id="612bb-683">Key size (bits)</span></span>   | <span data-ttu-id="612bb-684">256</span><span class="sxs-lookup"><span data-stu-id="612bb-684">256</span></span>                 |
| <span data-ttu-id="612bb-685">Compatible con TLS</span><span class="sxs-lookup"><span data-stu-id="612bb-685">TLS capable</span></span>       | <span data-ttu-id="612bb-686">No</span><span class="sxs-lookup"><span data-stu-id="612bb-686">No</span></span>                  |
| <span data-ttu-id="612bb-687">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="612bb-687">Object identifier</span></span> | <span data-ttu-id="612bb-688">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="612bb-688">1.2.840.10045.3.1.7</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="612bb-689">Observaciones</span><span class="sxs-lookup"><span data-stu-id="612bb-689">Remarks</span></span>

<span data-ttu-id="612bb-690">Para usar una curva con nombre, llame a [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) con el algoritmo de la **\_ ECDSA \_ de bcrypt** o el **\_ \_ algoritmo ECDH de bcrypt** como el identificador del algoritmo.</span><span class="sxs-lookup"><span data-stu-id="612bb-690">To use a named curve, call [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) using either the **BCRYPT\_ECDSA\_ALGORITHM** or the **BCRYPT\_ECDH\_ALGORITHM** as the algorithm ID.</span></span> <span data-ttu-id="612bb-691">A continuación, llame a [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) y establezca la propiedad **BCRYPT \_ ECC \_ Curve \_ Name** en una de las curvas anteriores o en cualquier curva con nombre registrada en el equipo, tal como se muestra en el `certutil -displayEccCurve` comando.</span><span class="sxs-lookup"><span data-stu-id="612bb-691">Then, call [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) and set the **BCRYPT\_ECC\_CURVE\_NAME** property to one of the above curves or any named curves registered on the computer as shown by the `certutil -displayEccCurve` command.</span></span>

## <a name="requirements"></a><span data-ttu-id="612bb-692">Requisitos</span><span class="sxs-lookup"><span data-stu-id="612bb-692">Requirements</span></span>



| <span data-ttu-id="612bb-693">Requisito</span><span class="sxs-lookup"><span data-stu-id="612bb-693">Requirement</span></span> | <span data-ttu-id="612bb-694">Value</span><span class="sxs-lookup"><span data-stu-id="612bb-694">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="612bb-695">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="612bb-695">Minimum supported client</span></span><br/> | <span data-ttu-id="612bb-696">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="612bb-696">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="612bb-697">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="612bb-697">Minimum supported server</span></span><br/> | <span data-ttu-id="612bb-698">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="612bb-698">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="612bb-699">Encabezado</span><span class="sxs-lookup"><span data-stu-id="612bb-699">Header</span></span><br/>                   | <dl> <span data-ttu-id="612bb-700"><dt>Bcrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="612bb-700"><dt>Bcrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="612bb-701">Vea también</span><span class="sxs-lookup"><span data-stu-id="612bb-701">See also</span></span>

<dl> <dt>

[<span data-ttu-id="612bb-702">**BCryptOpenAlgorithmProvider**</span><span class="sxs-lookup"><span data-stu-id="612bb-702">**BCryptOpenAlgorithmProvider**</span></span>](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[<span data-ttu-id="612bb-703">**NCryptCreatePersistedKey**</span><span class="sxs-lookup"><span data-stu-id="612bb-703">**NCryptCreatePersistedKey**</span></span>](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




