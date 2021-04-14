---
description: Al desarrollar su propia aplicación de VSS, debe respetar las siguientes directrices y restricciones.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: Compatibilidad de aplicaciones de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9cc19b6a6d88365a67569bc4729855077c9da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360315"
---
# <a name="vss-application-compatibility"></a><span data-ttu-id="a0dae-103">Compatibilidad de aplicaciones de VSS</span><span class="sxs-lookup"><span data-stu-id="a0dae-103">VSS Application Compatibility</span></span>

<span data-ttu-id="a0dae-104">Al desarrollar su propia aplicación de VSS, debe respetar las siguientes directrices y restricciones.</span><span class="sxs-lookup"><span data-stu-id="a0dae-104">When developing your own VSS application, you should observe the following guidelines and restrictions.</span></span> <span data-ttu-id="a0dae-105">Puede que le resulte útil consultar el código de ejemplo de los solicitantes, proveedores y escritores de VSS que se proporcionan en el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a0dae-105">You may find it helpful to refer to the sample code for VSS requesters, providers, and writers that is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="a0dae-106">El Windows SDK se puede usar para desarrollar aplicaciones VSS solo para Windows Vista y versiones posteriores del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="a0dae-106">The Windows SDK can be used to develop VSS applications only for Windows Vista and later Windows operating system versions.</span></span> <span data-ttu-id="a0dae-107">No se puede usar para desarrollar solicitantes, proveedores o escritores de VSS para Windows Server 2003 R2, Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0dae-107">It cannot be used to develop VSS requesters, providers, or writers for Windows Server 2003 R2, Windows Server 2003, or Windows XP.</span></span>

 

<span data-ttu-id="a0dae-108">**Windows server 2003 R2, Windows server 2003 y Windows XP:** VSS está disponible en el SDK de Servicio de instantáneas de volumen 7,2, que puede descargar de [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) .</span><span class="sxs-lookup"><span data-stu-id="a0dae-108">**Windows Server 2003 R2, Windows Server 2003 and Windows XP:** VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="a0dae-109">Tenga en cuenta que los archivos vssapi. lib de 64 bits en los directorios del \\ directorio obj de Win2003 se pueden usar para las versiones de 64 bits de Windows server 2003 R2, Windows server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0dae-109">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 R2, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="a0dae-110">Este SDK también proporciona código de ejemplo para los solicitantes, proveedores y escritores de VSS.</span><span class="sxs-lookup"><span data-stu-id="a0dae-110">This SDK also provides sample code for VSS requesters, providers, and writers.</span></span>

## <a name="compiling-vss-applications"></a><span data-ttu-id="a0dae-111">Compilar aplicaciones VSS</span><span class="sxs-lookup"><span data-stu-id="a0dae-111">Compiling VSS Applications</span></span>

<span data-ttu-id="a0dae-112">Al desarrollar un solicitante, como una aplicación de copia de seguridad:</span><span class="sxs-lookup"><span data-stu-id="a0dae-112">When developing a requester, such as a backup application:</span></span>

-   <span data-ttu-id="a0dae-113">Incluya los encabezados siguientes:</span><span class="sxs-lookup"><span data-stu-id="a0dae-113">Include the following headers:</span></span> <dl> <span data-ttu-id="a0dae-114">VSS. h</span><span class="sxs-lookup"><span data-stu-id="a0dae-114">Vss.h</span></span>  
    <span data-ttu-id="a0dae-115">VsWriter. h</span><span class="sxs-lookup"><span data-stu-id="a0dae-115">VsWriter.h</span></span>  
    <span data-ttu-id="a0dae-116">VsBackup. h</span><span class="sxs-lookup"><span data-stu-id="a0dae-116">VsBackup.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="a0dae-117">VssApi. lib</span><span class="sxs-lookup"><span data-stu-id="a0dae-117">VssApi.Lib</span></span>  
    </dl>

<span data-ttu-id="a0dae-118">Al desarrollar un escritor:</span><span class="sxs-lookup"><span data-stu-id="a0dae-118">When developing a writer:</span></span>

-   <span data-ttu-id="a0dae-119">Incluya los encabezados siguientes:</span><span class="sxs-lookup"><span data-stu-id="a0dae-119">Include the following headers:</span></span> <dl> <span data-ttu-id="a0dae-120">VSS. h</span><span class="sxs-lookup"><span data-stu-id="a0dae-120">Vss.h</span></span>  
    <span data-ttu-id="a0dae-121">VsWriter. h</span><span class="sxs-lookup"><span data-stu-id="a0dae-121">VsWriter.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="a0dae-122">VssApi. lib</span><span class="sxs-lookup"><span data-stu-id="a0dae-122">VssApi.lib</span></span>  
    </dl>

## <a name="supported-configurations-and-restrictions"></a><span data-ttu-id="a0dae-123">Configuraciones y restricciones admitidas</span><span class="sxs-lookup"><span data-stu-id="a0dae-123">Supported Configurations and Restrictions</span></span>

<span data-ttu-id="a0dae-124">En la lista siguiente se describen las configuraciones admitidas y las restricciones:</span><span class="sxs-lookup"><span data-stu-id="a0dae-124">The following list describes supported configurations and restrictions:</span></span>

-   <span data-ttu-id="a0dae-125">Se proporciona VSS y se admite en las versiones del sistema operativo Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0dae-125">VSS is provided and supported on versions of the Windows operating system beginning with Windows XP.</span></span>
-   <span data-ttu-id="a0dae-126">En la tabla siguiente se resume la información de compatibilidad entre las versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="a0dae-126">The following table summarizes compatibility information across Windows versions.</span></span> <span data-ttu-id="a0dae-127">Tenga en cuenta que si una aplicación VSS se "compila para" una versión de Windows especificada, significa que la aplicación se compiló con los archivos de encabezado y las bibliotecas que son específicas de esa versión.</span><span class="sxs-lookup"><span data-stu-id="a0dae-127">Note that if a VSS application is "compiled for" a specified Windows version, this means that the application was compiled using the header files and libraries that are specific to that version.</span></span>

    > [!Note]  
    > <span data-ttu-id="a0dae-128">Los proveedores de hardware solo se ejecutarán en las versiones del sistema operativo Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a0dae-128">Hardware providers will run only on Windows server operating system versions.</span></span> <span data-ttu-id="a0dae-129">No se ejecutarán en las versiones de sistema operativo de cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="a0dae-129">They will not run on Windows client operating system versions.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="a0dae-130">En las tablas siguientes, Windows Server 2008 con Service Pack 2 (SP2) debe considerarse igual que Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a0dae-130">In the following tables, Windows Server 2008 with Service Pack 2 (SP2) should be considered the same as Windows Server 2008.</span></span> <span data-ttu-id="a0dae-131">Para obtener más información acerca de Windows Server 2008 con SP2, vea <https://go.microsoft.com/fwlink/p/?linkid=178730> .</span><span class="sxs-lookup"><span data-stu-id="a0dae-131">For more information about Windows Server 2008 with SP2, see <https://go.microsoft.com/fwlink/p/?linkid=178730>.</span></span> <span data-ttu-id="a0dae-132">Windows Server 2003 R2 debe considerarse igual que Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a0dae-132">Windows Server 2003 R2 should be considered the same as Windows Server 2003.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="a0dae-133">Si se compila una aplicación de VSS para Windows Server 2003 o una versión posterior, también se ejecutará en versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="a0dae-133">If a VSS application is compiled for Windows Server 2003 or later, it will also run on later versions of Windows.</span></span>

     

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="a0dae-134">Solicitantes, escritores y proveedores de VSS compilados para</span><span class="sxs-lookup"><span data-stu-id="a0dae-134">VSS requesters, writers, and providers compiled for</span></span></th>
    <th><span data-ttu-id="a0dae-135">Se ejecutará el</span><span class="sxs-lookup"><span data-stu-id="a0dae-135">Will run on</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="a0dae-136">Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) y Windows Vista (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a0dae-136">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    <td><span data-ttu-id="a0dae-137">Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) y Windows Vista (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a0dae-137">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="a0dae-138">Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) y Windows Vista (32 bits)</span><span class="sxs-lookup"><span data-stu-id="a0dae-138">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    <td><span data-ttu-id="a0dae-139">Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) y Windows Vista (32 bits)</span><span class="sxs-lookup"><span data-stu-id="a0dae-139">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="a0dae-140">Windows Server 2003 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a0dae-140">Windows Server 2003 (64-bit)</span></span></td>
    <td><span data-ttu-id="a0dae-141">Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits), Windows Vista (64 bits) y Windows Server 2003 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a0dae-141">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit), Windows Vista (64-bit), and Windows Server 2003 (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="a0dae-142">Windows Server 2003 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="a0dae-142">Windows Server 2003 (32-bit)</span></span></td>
    <td><span data-ttu-id="a0dae-143">Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits), Windows Vista (32 bits) y Windows Server 2003 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="a0dae-143">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit), Windows Vista (32-bit), and Windows Server 2003 (32-bit)</span></span> <blockquote>
    [!Note]<br />
<span data-ttu-id="a0dae-144">Los solicitantes también se ejecutarán en Windows Server 2003 (64 bits).</span><span class="sxs-lookup"><span data-stu-id="a0dae-144">Requesters will also run on Windows Server 2003 (64-bit).</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="a0dae-145">Windows XP 64-bit Edition</span><span class="sxs-lookup"><span data-stu-id="a0dae-145">Windows XP 64-Bit Edition</span></span></td>
    <td><span data-ttu-id="a0dae-146">Windows Server 2003 (64 bits) y Windows XP 64-bit Edition</span><span class="sxs-lookup"><span data-stu-id="a0dae-146">Windows Server 2003 (64-bit) and Windows XP 64-Bit Edition</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="a0dae-147">Windows XP (32 bits)</span><span class="sxs-lookup"><span data-stu-id="a0dae-147">Windows XP (32-bit)</span></span></td>
    <td><span data-ttu-id="a0dae-148">Windows XP (32 bits)</span><span class="sxs-lookup"><span data-stu-id="a0dae-148">Windows XP (32-bit)</span></span></td>
    </tr>
    </tbody>
    </table>

    

     

    

    | <span data-ttu-id="a0dae-149">Para compilar un solicitante, escritor o proveedor de VSS para</span><span class="sxs-lookup"><span data-stu-id="a0dae-149">To compile a VSS requester, writer, or provider for</span></span>        | <span data-ttu-id="a0dae-150">Use</span><span class="sxs-lookup"><span data-stu-id="a0dae-150">Use</span></span>                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="a0dae-151">Windows Server 2008 R2 o Windows 7</span><span class="sxs-lookup"><span data-stu-id="a0dae-151">Windows Server 2008 R2 or Windows 7</span></span>                        | <span data-ttu-id="a0dae-152">Windows SDK para Windows 7 (disponible en el [centro de descarga de Windows](https://www.microsoft.com/download/details.aspx?id=8279)).</span><span class="sxs-lookup"><span data-stu-id="a0dae-152">Windows SDK for Windows 7 (Available from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).)</span></span>                |
    | <span data-ttu-id="a0dae-153">Windows Server 2008 o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0dae-153">Windows Server 2008 or Windows Vista</span></span>                       | <span data-ttu-id="a0dae-154">Windows SDK para Windows Server 2008 (disponible en el [Centro para desarrolladores de Windows SDK](https://msdn.microsoft.com/windows/bb980924.aspx)).</span><span class="sxs-lookup"><span data-stu-id="a0dae-154">Windows SDK for Windows Server 2008 (Available from the [Windows SDK Developer Center](https://msdn.microsoft.com/windows/bb980924.aspx).)</span></span> |
    | <span data-ttu-id="a0dae-155">Windows Server 2003 R2, Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0dae-155">Windows Server 2003 R2, Windows Server 2003, or Windows XP</span></span> | [<span data-ttu-id="a0dae-156">SDK de Servicio de instantáneas de volumen 7,2</span><span class="sxs-lookup"><span data-stu-id="a0dae-156">Volume Shadow Copy Service 7.2 SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   <span data-ttu-id="a0dae-157">Todas las aplicaciones VSS de 32 bits (solicitantes, proveedores y escritores) deben ejecutarse como aplicaciones nativas de 32 bits o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a0dae-157">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="a0dae-158">No se admite su ejecución en WOW64.</span><span class="sxs-lookup"><span data-stu-id="a0dae-158">Running them under WOW64 is not supported.</span></span>

    <span data-ttu-id="a0dae-159">**Windows Server 2003 y Windows XP:** Se admite la ejecución de solicitantes de VSS de 32 bits bajo WOW64, pero no para copias de seguridad de estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="a0dae-159">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="a0dae-160">No se admite la ejecución de proveedores y escritores de VSS de 32 bits en WOW64.</span><span class="sxs-lookup"><span data-stu-id="a0dae-160">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="a0dae-161">Se quitó la compatibilidad con la ejecución de solicitantes de 32 bits en WOW64 en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a0dae-161">Support for running 32- bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

-   <span data-ttu-id="a0dae-162">Una instantánea creada en Windows Server 2003 R2 o Windows Server 2003 no se puede usar en un equipo que ejecute Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a0dae-162">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="a0dae-163">Una instantánea creada en Windows Server 2008 R2 o Windows Server 2008 no se puede usar en un equipo que ejecute Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a0dae-163">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="a0dae-164">Sin embargo, una instantánea creada en Windows Server 2008 puede usarse en un equipo que ejecute Windows Server 2008 R2 y viceversa.</span><span class="sxs-lookup"><span data-stu-id="a0dae-164">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>
-   <span data-ttu-id="a0dae-165">Para admitir instantáneas, un sistema que ejecute VSS debe tener al menos un sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="a0dae-165">To support shadow copies, a system running VSS must have at least one NTFS file system.</span></span> <span data-ttu-id="a0dae-166">Este sistema de archivos hospedará el "área de diferencias" de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="a0dae-166">This file system will host the shadow copy's "diff area."</span></span> <span data-ttu-id="a0dae-167">Para obtener más información, vea [proveedor del sistema](providers.md).</span><span class="sxs-lookup"><span data-stu-id="a0dae-167">For more information, see [System Provider](providers.md).</span></span>
-   <span data-ttu-id="a0dae-168">Dada la presencia de un sistema de archivos NTFS y dada la elección de contexto adecuada (vea [configuraciones de contexto de instantáneas](shadow-copy-context-configurations.md)), se puede realizar una instantánea de cualquier sistema de archivos local compatible.</span><span class="sxs-lookup"><span data-stu-id="a0dae-168">Given the presence of one NTFS file system, and given the appropriate choice of context (see [Shadow Copy Context Configurations](shadow-copy-context-configurations.md)), any supported local file system can be shadow copied.</span></span>
-   <span data-ttu-id="a0dae-169">Solo puede hacer instantáneas para sistemas de archivos montados localmente.</span><span class="sxs-lookup"><span data-stu-id="a0dae-169">You can make shadow copies only for locally mounted file systems.</span></span> <span data-ttu-id="a0dae-170">Los recursos compartidos remotos y otros sistemas de archivos entre montajes no pueden ser copiados por el sistema que los monta.</span><span class="sxs-lookup"><span data-stu-id="a0dae-170">Remote shares and other cross-mounted file systems cannot be shadow copied by the system that mounts them.</span></span> <span data-ttu-id="a0dae-171">Solo pueden realizarse instantáneas de estos sistemas de archivos los sistemas que prestan servicio a los sistemas de archivos.</span><span class="sxs-lookup"><span data-stu-id="a0dae-171">These file systems can be shadow copied only by the systems that serve out the file systems.</span></span>
-   <span data-ttu-id="a0dae-172">Los escritores y los solicitantes solo deben especificar recursos locales.</span><span class="sxs-lookup"><span data-stu-id="a0dae-172">Writers and requesters should specify only local resources.</span></span> <span data-ttu-id="a0dae-173">Los recursos locales son conjuntos de archivos cuya ruta de acceso absoluta empieza con una letra de unidad y la letra de unidad no se puede asociar a una carpeta montada en un recurso compartido remoto.</span><span class="sxs-lookup"><span data-stu-id="a0dae-173">Local resources are sets of files whose absolute path starts with a drive letter, and the drive letter cannot be associated with a mounted folder on a remote share.</span></span>
-   <span data-ttu-id="a0dae-174">El número máximo de instantáneas de software para cada volumen es 512.</span><span class="sxs-lookup"><span data-stu-id="a0dae-174">The maximum number is of software shadow copies for each volume is 512.</span></span> <span data-ttu-id="a0dae-175">Sin embargo, de forma predeterminada solo se pueden mantener 64 instantáneas utilizadas por la característica Instantáneas de carpetas compartidas.</span><span class="sxs-lookup"><span data-stu-id="a0dae-175">However, by default you can only maintain 64 shadow copies that are used by the Shadow Copies of Shared Folders feature.</span></span> <span data-ttu-id="a0dae-176">Para cambiar el límite de la característica instantáneas de carpetas compartidas, utilice la clave del registro [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="a0dae-176">To change the limit for the Shadow Copies of Shared Folders feature, use the [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) registry key.</span></span>
-   <span data-ttu-id="a0dae-177">La infraestructura de componentes de copia de seguridad no admite la copia de seguridad de recursos de clúster como componentes del escritor.</span><span class="sxs-lookup"><span data-stu-id="a0dae-177">The Backup Components infrastructure does not support backing up cluster resources as writer components.</span></span> <span data-ttu-id="a0dae-178">Para realizar una copia de seguridad de los recursos del clúster, las aplicaciones deben suponer que la ruta de acceso es local a un determinado nodo de clúster.</span><span class="sxs-lookup"><span data-stu-id="a0dae-178">To back up cluster resources, applications should assume that the path is local to a specified particular cluster node.</span></span>
-   [!Note]  
    > <span data-ttu-id="a0dae-179">Microsoft no proporciona soporte técnico para desarrolladores o profesionales de TI para implementar restauraciones de estado del sistema en línea en Windows (todas las versiones).</span><span class="sxs-lookup"><span data-stu-id="a0dae-179">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

     

    <span data-ttu-id="a0dae-180">Al realizar copias de seguridad y recuperar el estado del sistema, la estrategia recomendada es realizar copias de seguridad y recuperar los volúmenes del sistema y de arranque, además de los archivos enumerados por los escritores de estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="a0dae-180">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span>

    > [!Note]  
    > <span data-ttu-id="a0dae-181">Los escritores de estado del sistema son escritores que tienen el atributo [**\_ \_ tipo de uso de VSS**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) establecido en VSS \_ UT \_ BOOTABLESYSTEMSTATE o VSS \_ UT \_ SYSTEMSERVICE.</span><span class="sxs-lookup"><span data-stu-id="a0dae-181">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

     

 

 
