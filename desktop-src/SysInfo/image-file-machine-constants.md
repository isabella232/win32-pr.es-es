---
description: Describe las posibles arquitecturas de máquina.
ms.assetid: 1E5E4F98-925B-424D-9B3D-BC6716FBF990
title: Constantes del equipo de archivos de imagen (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c43767ce0d86edf2285241772ea060573efc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542670"
---
# <a name="image-file-machine-constants"></a><span data-ttu-id="f1f03-103">Constantes del equipo de archivos de imagen</span><span class="sxs-lookup"><span data-stu-id="f1f03-103">Image File Machine Constants</span></span>

<span data-ttu-id="f1f03-104">Describe las posibles arquitecturas de máquina.</span><span class="sxs-lookup"><span data-stu-id="f1f03-104">Describes possible machine architectures.</span></span> <span data-ttu-id="f1f03-105">Se usa en [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) y [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).</span><span class="sxs-lookup"><span data-stu-id="f1f03-105">Used in [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) and [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).</span></span>

<dl> <dt>

<span data-ttu-id="f1f03-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**máquina de archivo de imagen \_ \_ \_ desconocida**</span><span class="sxs-lookup"><span data-stu-id="f1f03-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**IMAGE\_FILE\_MACHINE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-107">0</span><span class="sxs-lookup"><span data-stu-id="f1f03-107">0</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-108">Unknown</span><span class="sxs-lookup"><span data-stu-id="f1f03-108">Unknown</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**\_host de \_ destino del equipo de archivos de imagen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f1f03-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**IMAGE\_FILE\_MACHINE\_TARGET\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="f1f03-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-111">Interactúa con el host y no con un invitado WOW64</span><span class="sxs-lookup"><span data-stu-id="f1f03-111">Interacts with the host and not a WOW64 guest</span></span>

> [!Note]  
> <span data-ttu-id="f1f03-112">Esta constante está disponible a partir de Windows 10, la versión 1607 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f1f03-112">This constant is available starting with Windows 10, version 1607 and Windows Server 2016.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**Máquina de archivos de imagen \_ \_ \_ i386**</span><span class="sxs-lookup"><span data-stu-id="f1f03-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**IMAGE\_FILE\_MACHINE\_I386**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-114">0x014c</span><span class="sxs-lookup"><span data-stu-id="f1f03-114">0x014c</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-115">Intel 386</span><span class="sxs-lookup"><span data-stu-id="f1f03-115">Intel 386</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**Máquina de archivos de imagen \_ \_ \_ R3000**</span><span class="sxs-lookup"><span data-stu-id="f1f03-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**IMAGE\_FILE\_MACHINE\_R3000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-117">0x0162</span><span class="sxs-lookup"><span data-stu-id="f1f03-117">0x0162</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-118">Little-Endian de MIPS, 0x160 Big-Endian</span><span class="sxs-lookup"><span data-stu-id="f1f03-118">MIPS little-endian, 0x160 big-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**Máquina de archivos de imagen \_ \_ \_ R4000**</span><span class="sxs-lookup"><span data-stu-id="f1f03-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**IMAGE\_FILE\_MACHINE\_R4000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-120">0x0166</span><span class="sxs-lookup"><span data-stu-id="f1f03-120">0x0166</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-121">Little-Endian de MIPS</span><span class="sxs-lookup"><span data-stu-id="f1f03-121">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**Máquina de archivos de imagen \_ \_ \_ R10000**</span><span class="sxs-lookup"><span data-stu-id="f1f03-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**IMAGE\_FILE\_MACHINE\_R10000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-123">0x0168</span><span class="sxs-lookup"><span data-stu-id="f1f03-123">0x0168</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-124">Little-Endian de MIPS</span><span class="sxs-lookup"><span data-stu-id="f1f03-124">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**Máquina de archivos de imagen \_ \_ \_ WCEMIPSV2**</span><span class="sxs-lookup"><span data-stu-id="f1f03-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**IMAGE\_FILE\_MACHINE\_WCEMIPSV2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-126">0x0169</span><span class="sxs-lookup"><span data-stu-id="f1f03-126">0x0169</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-127">MIPS Little-endian, WCE V2</span><span class="sxs-lookup"><span data-stu-id="f1f03-127">MIPS little-endian WCE v2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**\_alfa del \_ equipo de archivos de imagen \_**</span><span class="sxs-lookup"><span data-stu-id="f1f03-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**IMAGE\_FILE\_MACHINE\_ALPHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-129">0x0184</span><span class="sxs-lookup"><span data-stu-id="f1f03-129">0x0184</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-130">Alpha \_ AXP</span><span class="sxs-lookup"><span data-stu-id="f1f03-130">Alpha\_AXP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**Máquina de archivos de imagen \_ \_ \_ SH3**</span><span class="sxs-lookup"><span data-stu-id="f1f03-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**IMAGE\_FILE\_MACHINE\_SH3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-132">0x01a2</span><span class="sxs-lookup"><span data-stu-id="f1f03-132">0x01a2</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-133">SH3 Little-endian</span><span class="sxs-lookup"><span data-stu-id="f1f03-133">SH3 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**Máquina de archivos de imagen \_ \_ \_ SH3DSP**</span><span class="sxs-lookup"><span data-stu-id="f1f03-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**IMAGE\_FILE\_MACHINE\_SH3DSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-135">0x01a3</span><span class="sxs-lookup"><span data-stu-id="f1f03-135">0x01a3</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-136">SH3DSP</span><span class="sxs-lookup"><span data-stu-id="f1f03-136">SH3DSP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**Máquina de archivos de imagen \_ \_ \_ SH3E**</span><span class="sxs-lookup"><span data-stu-id="f1f03-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**IMAGE\_FILE\_MACHINE\_SH3E**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-138">0x01a4</span><span class="sxs-lookup"><span data-stu-id="f1f03-138">0x01a4</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-139">SH3E Little-endian</span><span class="sxs-lookup"><span data-stu-id="f1f03-139">SH3E little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**Máquina de archivos de imagen \_ \_ \_ SH4**</span><span class="sxs-lookup"><span data-stu-id="f1f03-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**IMAGE\_FILE\_MACHINE\_SH4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-141">0x01a6</span><span class="sxs-lookup"><span data-stu-id="f1f03-141">0x01a6</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-142">SH4 Little-endian</span><span class="sxs-lookup"><span data-stu-id="f1f03-142">SH4 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**Máquina de archivos de imagen \_ \_ \_ SH5**</span><span class="sxs-lookup"><span data-stu-id="f1f03-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**IMAGE\_FILE\_MACHINE\_SH5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-144">0x01a8</span><span class="sxs-lookup"><span data-stu-id="f1f03-144">0x01a8</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-145">SH5</span><span class="sxs-lookup"><span data-stu-id="f1f03-145">SH5</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**\_ARM del \_ equipo de archivos de imagen \_**</span><span class="sxs-lookup"><span data-stu-id="f1f03-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**IMAGE\_FILE\_MACHINE\_ARM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-147">0x01c0</span><span class="sxs-lookup"><span data-stu-id="f1f03-147">0x01c0</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-148">Little-Endian ARM</span><span class="sxs-lookup"><span data-stu-id="f1f03-148">ARM Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**\_control de \_ equipo de archivo de imagen \_**</span><span class="sxs-lookup"><span data-stu-id="f1f03-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**IMAGE\_FILE\_MACHINE\_THUMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-150">0x01c2</span><span class="sxs-lookup"><span data-stu-id="f1f03-150">0x01c2</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-151">Thumb Thumb/Thumb-2 Little-Endian</span><span class="sxs-lookup"><span data-stu-id="f1f03-151">ARM Thumb/Thumb-2 Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**máquina de archivos de imagen \_ \_ \_ ARMNT**</span><span class="sxs-lookup"><span data-stu-id="f1f03-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**IMAGE\_FILE\_MACHINE\_ARMNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-153">0x01c4</span><span class="sxs-lookup"><span data-stu-id="f1f03-153">0x01c4</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-154">Control de ARM: 2 Little-Endian</span><span class="sxs-lookup"><span data-stu-id="f1f03-154">ARM Thumb-2 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="f1f03-155">Esta constante está disponible a partir de Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="f1f03-155">This constant is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**Máquina de archivos de imagen \_ \_ \_ AM33**</span><span class="sxs-lookup"><span data-stu-id="f1f03-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**IMAGE\_FILE\_MACHINE\_AM33**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-157">0x01d3</span><span class="sxs-lookup"><span data-stu-id="f1f03-157">0x01d3</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-158">TAM33BD</span><span class="sxs-lookup"><span data-stu-id="f1f03-158">TAM33BD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**máquina de archivos de imagen \_ \_ \_ POWERPC**</span><span class="sxs-lookup"><span data-stu-id="f1f03-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**IMAGE\_FILE\_MACHINE\_POWERPC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-160">0x01F0</span><span class="sxs-lookup"><span data-stu-id="f1f03-160">0x01F0</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-161">Little-Endian de IBM PowerPC</span><span class="sxs-lookup"><span data-stu-id="f1f03-161">IBM PowerPC Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**máquina de archivos de imagen \_ \_ \_ POWERPCFP**</span><span class="sxs-lookup"><span data-stu-id="f1f03-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**IMAGE\_FILE\_MACHINE\_POWERPCFP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-163">0x01f1</span><span class="sxs-lookup"><span data-stu-id="f1f03-163">0x01f1</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-164">POWERPCFP</span><span class="sxs-lookup"><span data-stu-id="f1f03-164">POWERPCFP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**Máquina de archivos de imagen \_ \_ \_ ia64**</span><span class="sxs-lookup"><span data-stu-id="f1f03-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**IMAGE\_FILE\_MACHINE\_IA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-166">0x0200</span><span class="sxs-lookup"><span data-stu-id="f1f03-166">0x0200</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-167">Intel 64</span><span class="sxs-lookup"><span data-stu-id="f1f03-167">Intel 64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**Máquina de archivos de imagen \_ \_ \_ MIPS16**</span><span class="sxs-lookup"><span data-stu-id="f1f03-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**IMAGE\_FILE\_MACHINE\_MIPS16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-169">0x0266</span><span class="sxs-lookup"><span data-stu-id="f1f03-169">0x0266</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-170">MIPS</span><span class="sxs-lookup"><span data-stu-id="f1f03-170">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**Máquina de archivos de imagen \_ \_ \_ ALPHA64**</span><span class="sxs-lookup"><span data-stu-id="f1f03-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**IMAGE\_FILE\_MACHINE\_ALPHA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-172">0x0284</span><span class="sxs-lookup"><span data-stu-id="f1f03-172">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-173">ALPHA64</span><span class="sxs-lookup"><span data-stu-id="f1f03-173">ALPHA64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**máquina de archivos de imagen \_ \_ \_ MIPSFPU**</span><span class="sxs-lookup"><span data-stu-id="f1f03-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-175">0x0366</span><span class="sxs-lookup"><span data-stu-id="f1f03-175">0x0366</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-176">MIPS</span><span class="sxs-lookup"><span data-stu-id="f1f03-176">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**Máquina de archivos de imagen \_ \_ \_ MIPSFPU16**</span><span class="sxs-lookup"><span data-stu-id="f1f03-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-178">0x0466</span><span class="sxs-lookup"><span data-stu-id="f1f03-178">0x0466</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-179">MIPS</span><span class="sxs-lookup"><span data-stu-id="f1f03-179">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**Máquina de archivos de imagen \_ \_ \_ AXP64**</span><span class="sxs-lookup"><span data-stu-id="f1f03-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**IMAGE\_FILE\_MACHINE\_AXP64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-181">0x0284</span><span class="sxs-lookup"><span data-stu-id="f1f03-181">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-182">AXP64</span><span class="sxs-lookup"><span data-stu-id="f1f03-182">AXP64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**máquina de archivos de imagen de \_ \_ \_ trinúcleo**</span><span class="sxs-lookup"><span data-stu-id="f1f03-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**IMAGE\_FILE\_MACHINE\_TRICORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-184">0x0520</span><span class="sxs-lookup"><span data-stu-id="f1f03-184">0x0520</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-185">Infineon</span><span class="sxs-lookup"><span data-stu-id="f1f03-185">Infineon</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**máquina de archivos de imagen \_ \_ \_ CEF**</span><span class="sxs-lookup"><span data-stu-id="f1f03-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**IMAGE\_FILE\_MACHINE\_CEF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-187">0x0CEF</span><span class="sxs-lookup"><span data-stu-id="f1f03-187">0x0CEF</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-188">CEF</span><span class="sxs-lookup"><span data-stu-id="f1f03-188">CEF</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**archivo de imagen del \_ \_ sistema \_ EBC**</span><span class="sxs-lookup"><span data-stu-id="f1f03-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**IMAGE\_FILE\_MACHINE\_EBC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-190">0x0EBC</span><span class="sxs-lookup"><span data-stu-id="f1f03-190">0x0EBC</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-191">Código de byte EFI</span><span class="sxs-lookup"><span data-stu-id="f1f03-191">EFI Byte Code</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**Máquina de archivos de imagen \_ \_ \_ AMD64**</span><span class="sxs-lookup"><span data-stu-id="f1f03-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**IMAGE\_FILE\_MACHINE\_AMD64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-193">0x8664</span><span class="sxs-lookup"><span data-stu-id="f1f03-193">0x8664</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-194">AMD64 (K8)</span><span class="sxs-lookup"><span data-stu-id="f1f03-194">AMD64 (K8)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**Máquina de archivos de imagen \_ \_ \_ M32R**</span><span class="sxs-lookup"><span data-stu-id="f1f03-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**IMAGE\_FILE\_MACHINE\_M32R**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-196">0x9041</span><span class="sxs-lookup"><span data-stu-id="f1f03-196">0x9041</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-197">M32R Little-endian</span><span class="sxs-lookup"><span data-stu-id="f1f03-197">M32R little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**Máquina de archivos de imagen \_ \_ \_ ARM64**</span><span class="sxs-lookup"><span data-stu-id="f1f03-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**IMAGE\_FILE\_MACHINE\_ARM64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-199">0xAA64</span><span class="sxs-lookup"><span data-stu-id="f1f03-199">0xAA64</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-200">Little-Endian ARM64</span><span class="sxs-lookup"><span data-stu-id="f1f03-200">ARM64 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="f1f03-201">Esta constante está disponible a partir de Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="f1f03-201">This constant is available starting with Windows 8.1 and Windows Server 2012 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1f03-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**máquina del archivo de imagen \_ \_ \_ CEE**</span><span class="sxs-lookup"><span data-stu-id="f1f03-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**IMAGE\_FILE\_MACHINE\_CEE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1f03-203">0xC0EE</span><span class="sxs-lookup"><span data-stu-id="f1f03-203">0xC0EE</span></span>
</dt> <dt>



<span data-ttu-id="f1f03-204">CEE</span><span class="sxs-lookup"><span data-stu-id="f1f03-204">CEE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1f03-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1f03-205">Requirements</span></span>



| <span data-ttu-id="f1f03-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1f03-206">Requirement</span></span> | <span data-ttu-id="f1f03-207">Value</span><span class="sxs-lookup"><span data-stu-id="f1f03-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f03-208">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1f03-208">Minimum supported client</span></span><br/> | <span data-ttu-id="f1f03-209">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f1f03-209">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1f03-210">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1f03-210">Minimum supported server</span></span><br/> | <span data-ttu-id="f1f03-211">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1f03-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f1f03-212">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1f03-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1f03-213"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1f03-213"><dt>Winnt.h</dt></span></span> </dl> |



 

 




