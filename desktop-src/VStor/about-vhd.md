---
description: El formato de disco duro virtual (VHD) es una especificación de formato de imagen disponible públicamente que permite la encapsulación del disco duro en un archivo individual para que lo use el sistema operativo como un disco virtual en el mismo modo en que se usan los discos duros físicos.
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Acerca de VHD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ea37851360e70c1108e0715a47c77163c2c2fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809793"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span data-ttu-id="7e4c9-103"><span id="vhd.about_vhd"></span>Acerca de VHD</span><span class="sxs-lookup"><span data-stu-id="7e4c9-103"><span id="vhd.about_vhd"></span>About VHD</span></span>

<span data-ttu-id="7e4c9-104">El formato de disco duro virtual (VHD) es una [especificación](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) de formato de imagen disponible públicamente que permite la encapsulación del disco duro en un archivo individual para que lo use el sistema operativo como un *disco virtual* en el mismo modo en que se usan los discos duros físicos.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-104">The Virtual Hard Disk (VHD) format is a publicly-available image format [specification](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) that allows encapsulation of the hard disk into an individual file for use by the operating system as a *virtual disk* in all the same ways physical hard disks are used.</span></span> <span data-ttu-id="7e4c9-105">Estos discos virtuales pueden hospedar sistemas de archivos nativos (NTFS, FAT, exFAT y UDF) mientras se admiten operaciones de archivos y discos estándar.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-105">These virtual disks are capable of hosting native file systems (NTFS, FAT, exFAT, and UDFS) while supporting standard disk and file operations.</span></span> <span data-ttu-id="7e4c9-106">La compatibilidad con la API de VHD permite la administración de los discos virtuales.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-106">VHD API support allows management of the virtual disks.</span></span> <span data-ttu-id="7e4c9-107">Los discos virtuales creados con la API de VHD pueden funcionar como discos de arranque.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-107">Virtual disks created with the VHD API can function as boot disks.</span></span>

<span data-ttu-id="7e4c9-108">Un ejemplo de cómo se usan los archivos VHD es la característica [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) de Windows 7, windows Server 2008, Virtual Server y Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-108">An example of how VHD files are used is the [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) feature in Windows 7, Windows Server 2008, Virtual Server, and Windows Virtual PC.</span></span> <span data-ttu-id="7e4c9-109">Estos productos usan la API de VHD para contener la imagen de sistema operativo Windows utilizada por una máquina virtual como disco de arranque del sistema.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-109">These products use the VHD API to contain the Windows operating system image utilized by a virtual machine as its system boot disk.</span></span>

<span data-ttu-id="7e4c9-110">El kit de desarrollo de software (SDK) de Microsoft Windows integra compatibilidad nativa con VHD para trabajar con discos virtuales, lo que facilita a los desarrolladores y administradores la creación, administración e implementación de imágenes de Windows en archivos VHD mediante la compatibilidad de la API de la plataforma o las herramientas de administración.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-110">The Microsoft Windows Software Development Kit (SDK) integrates Native VHD support for working with virtual disks, making it easier for developers and administrators to create, manage, and deploy Windows images in VHD files using either the platform API support or management tools.</span></span> <span data-ttu-id="7e4c9-111">No es necesario instalar aplicaciones independientes ni implementar un analizador de formato VHD para habilitar estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-111">It is not necessary to install separate applications or implement a VHD format parser to enable these operations.</span></span> <span data-ttu-id="7e4c9-112">Estas API permiten el uso genérico de discos virtuales independientemente de cualquier otra tecnología de virtualización.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-112">These APIs allow for generic use of virtual disks independent of any other virtualization technologies.</span></span>

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span data-ttu-id="7e4c9-113"><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminología</span><span class="sxs-lookup"><span data-stu-id="7e4c9-113"><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminology</span></span>

<span data-ttu-id="7e4c9-114">El término *memoria auxiliar* se usa para hacer referencia al archivo físico que existe en el disco duro real.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-114">The term *backing store* is used to refer to the physical file that exists on the actual hard disk.</span></span> <span data-ttu-id="7e4c9-115">La memoria auxiliar se representa mediante un *archivo de imagen de disco duro virtual*.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-115">The backing store is represented by a *VHD image file*.</span></span>

<span data-ttu-id="7e4c9-116">Los términos *Dynamic*, *Expandable* y *Sparse* suelen usarse indistintamente al hacer referencia a discos virtuales expansibles dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-116">The terms *dynamic*, *expandable*, and *sparse* are often used interchangeably when referring to dynamically expandable virtual disks.</span></span> <span data-ttu-id="7e4c9-117">En el caso de la tecnología de VHD, estos términos son idénticos.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-117">For VHD technology, these terms are identical.</span></span>

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span data-ttu-id="7e4c9-118"><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>Información general sobre las características del sistema VHD</span><span class="sxs-lookup"><span data-stu-id="7e4c9-118"><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>VHD System Features Overview</span></span>

<span data-ttu-id="7e4c9-119">En el diagrama siguiente se presenta información general sobre las características de VHD y sus relaciones.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-119">The following diagram presents an overview of the VHD features and their relationships.</span></span>

![diagrama de bloque de VHD](images/vhd.png)

<span data-ttu-id="7e4c9-121">A continuación se ofrece una explicación resumida de las características descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-121">The following is a summary explanation of the previously described features.</span></span>

<span data-ttu-id="7e4c9-122">API nativas de Windows en modo usuario:</span><span class="sxs-lookup"><span data-stu-id="7e4c9-122">User Mode Native Windows APIs:</span></span>

-   <span data-ttu-id="7e4c9-123">VirtDisk.dll: biblioteca común para las API de administración de VHD.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-123">VirtDisk.dll - Common library for VHD management APIs.</span></span>

<span data-ttu-id="7e4c9-124">Contenedores de administración específicos de dominio en modo de usuario:</span><span class="sxs-lookup"><span data-stu-id="7e4c9-124">User Mode Domain-specific Management Wrappers:</span></span>

-   <span data-ttu-id="7e4c9-125">[API de VHD de VDS](/windows/desktop/VDS/about-vds) : contenedores del modelo de objetos VDS para las API de Windows de VHD.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-125">[VDS VHD APIs](/windows/desktop/VDS/about-vds) - VDS Object Model wrappers for the VHD Windows APIs.</span></span>

<span data-ttu-id="7e4c9-126">Controladores de modo kernel:</span><span class="sxs-lookup"><span data-stu-id="7e4c9-126">Kernel Mode Drivers:</span></span>

-   <span data-ttu-id="7e4c9-127">VDrvRoot.sys enumerador de unidad virtual raíz.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-127">VDrvRoot.sys - Root virtual drive enumerator.</span></span>
-   <span data-ttu-id="7e4c9-128">FsDepends.sys: administración de dependencias de volumen anidada.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-128">FsDepends.sys - Nested volume dependency management.</span></span>
-   <span data-ttu-id="7e4c9-129">Vhdmp.sys: el proveedor de propiedades de dependencia y el analizador de VHD.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-129">Vhdmp.sys - VHD parser and dependency property provider.</span></span>

<span data-ttu-id="7e4c9-130">La documentación del SDK de esta sección trata las API de VHD nativas de Windows en modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-130">The SDK documentation in this section covers the user-mode native Windows VHD APIs.</span></span>

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span data-ttu-id="7e4c9-131"><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Tipos de discos virtuales</span><span class="sxs-lookup"><span data-stu-id="7e4c9-131"><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Virtual Disk Types</span></span>

<span data-ttu-id="7e4c9-132">Existen consideraciones para el uso de discos virtuales y los tipos de discos virtuales disponibles:</span><span class="sxs-lookup"><span data-stu-id="7e4c9-132">There are considerations for using virtual disks, and what types of virtual disks are available:</span></span>

-   <span data-ttu-id="7e4c9-133">**Corrección**: el archivo de imagen de disco duro virtual se ha asignado previamente en la memoria auxiliar para el tamaño máximo solicitado.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-133">**Fixed**—The VHD image file is pre-allocated on the backing store for the maximum size requested.</span></span>
-   <span data-ttu-id="7e4c9-134">**Expandible**: también conocido como "dinámico", "dinámicamente expansible" y "disperso", el archivo de imagen de VHD usa solo tanto espacio en la memoria auxiliar como sea necesario para almacenar los datos reales que contiene actualmente el disco virtual.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-134">**Expandable**—Also known as "dynamic", "dynamically expandable", and "sparse", the VHD image file uses only as much space on the backing store as needed to store the actual data the virtual disk currently contains.</span></span> <span data-ttu-id="7e4c9-135">Al crear este tipo de disco virtual, la API de VHD no comprueba el espacio disponible en el disco físico en función del tamaño máximo solicitado, por lo que es posible crear correctamente un disco virtual dinámico con un tamaño máximo mayor que el espacio disponible en disco físico.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-135">When creating this type of virtual disk, the VHD API does not test for free space on the physical disk based on the maximum size requested, therefore it is possible to successfully create a dynamic virtual disk with a maximum size larger than the available physical disk free space.</span></span> <span data-ttu-id="7e4c9-136">Para obtener más información, vea [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).</span><span class="sxs-lookup"><span data-stu-id="7e4c9-136">For more information, see [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).</span></span>
    <span data-ttu-id="7e4c9-137">**Nota:**  El tamaño máximo de un disco virtual dinámico es de 2.040 GB.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-137">**Note**  The maximum size of a dynamic virtual disk is 2,040 GB.</span></span>

     

-   <span data-ttu-id="7e4c9-138">**Diferencia**: se usa un disco virtual primario como base de este tipo, con las escrituras posteriores escritas en el disco virtual como diferencias con el nuevo archivo de imagen de VHD de diferenciación y el archivo de imagen de VHD primario no se modifica.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-138">**Differencing**—A parent virtual disk is used as the basis of this type, with any subsequent writes written to the virtual disk as differences to the new differencing VHD image file, and the parent VHD image file is not modified.</span></span> <span data-ttu-id="7e4c9-139">Por ejemplo, si tiene un disco virtual del sistema operativo de arranque del sistema de instalación limpia como principal y designa el disco virtual de diferenciación como el disco virtual actual que el sistema debe usar, el sistema operativo del disco virtual primario permanece en su estado original para una recuperación rápida o para crear rápidamente más imágenes de arranque basadas en discos virtuales de diferenciación adicionales.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-139">For example, if you have a clean-install system boot operating system virtual disk as a parent and designate the differencing virtual disk as the current virtual disk for the system to use, then the operating system on the parent virtual disk stays in its original state for quick recovery or for quickly creating more boot images based on additional differencing virtual disks.</span></span> <span data-ttu-id="7e4c9-140">Para obtener más información, vea [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).</span><span class="sxs-lookup"><span data-stu-id="7e4c9-140">For more information, see [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).</span></span>
    <span data-ttu-id="7e4c9-141">**Nota:**  El tamaño máximo de un disco virtual de diferenciación es de 2.040 GB.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-141">**Note**  The maximum size of a differencing virtual disk is 2,040 GB.</span></span>

     

<span data-ttu-id="7e4c9-142">Todos los tipos de discos virtuales tienen un tamaño mínimo de 3 MB.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-142">All virtual disk types have a minimum size of 3 MB.</span></span>

## <a name="span-idrelated_topicsspanrelated-topics"></a><span data-ttu-id="7e4c9-143"><span id="related_topics"></span>Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e4c9-143"><span id="related_topics"></span>Related topics</span></span>

[<span data-ttu-id="7e4c9-144">Acerca de VDS</span><span class="sxs-lookup"><span data-stu-id="7e4c9-144">About VDS</span></span>](/windows/desktop/VDS/about-vds)

[<span data-ttu-id="7e4c9-145">Referencia de VHD</span><span class="sxs-lookup"><span data-stu-id="7e4c9-145">VHD Reference</span></span>](vhd-reference.md)

[<span data-ttu-id="7e4c9-146">Especificación de formato de imagen de disco duro virtual</span><span class="sxs-lookup"><span data-stu-id="7e4c9-146">Virtual Hard Disk Image Format Specification</span></span>](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
