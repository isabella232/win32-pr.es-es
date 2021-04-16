---
description: Encapsular el disco duro en un solo archivo para que lo use el sistema operativo como un disco virtual. Los discos virtuales pueden funcionar como discos de arranque y pueden hospedar sistemas de archivos nativos (NTFS, FAT, exFAT y UDF) mientras se admiten operaciones de archivos y discos estándar.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Disco virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044145f5d631b878b533bbd409fad5eda5b4863f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275418"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span data-ttu-id="1cb69-104"><span id="vhd.portal"></span>Disco virtual</span><span class="sxs-lookup"><span data-stu-id="1cb69-104"><span id="vhd.portal"></span>Virtual Disk</span></span>

## <a name="span-idpurposespanpurpose"></a><span data-ttu-id="1cb69-105"><span id="purpose"></span>Propósito</span><span class="sxs-lookup"><span data-stu-id="1cb69-105"><span id="purpose"></span>Purpose</span></span>

<span data-ttu-id="1cb69-106">El formato de disco duro virtual (VHD) es una especificación de formato de imagen disponible públicamente que especifica un disco duro virtual encapsulado en un único archivo, capaz de hospedar sistemas de archivos nativos mientras se admiten operaciones de archivos y discos estándar.</span><span class="sxs-lookup"><span data-stu-id="1cb69-106">The Virtual Hard Disk (VHD) format is a publicly-available image format specification that specifies a virtual hard disk encapsulated in a single file, capable of hosting native file systems while supporting standard disk and file operations.</span></span> <span data-ttu-id="1cb69-107">Un ejemplo de cómo se usan los archivos VHD es la característica [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) de windows Server 2008, Virtual Server y Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="1cb69-107">An example of how VHD files are used is the [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) feature in Windows Server 2008, Virtual Server, and Windows Virtual PC.</span></span> <span data-ttu-id="1cb69-108">Estos productos usan discos duros virtuales para contener la imagen de sistema operativo Windows utilizada por una máquina virtual como disco de arranque del sistema.</span><span class="sxs-lookup"><span data-stu-id="1cb69-108">These products use VHDs to contain the Windows operating system image utilized by a virtual machine as its system boot disk.</span></span>

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span data-ttu-id="1cb69-109"><span id="developer_audience_heading"></span>Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="1cb69-109"><span id="developer_audience_heading"></span>Developer audience</span></span>

<span data-ttu-id="1cb69-110">El kit de desarrollo de software (SDK) de Microsoft Windows integra compatibilidad nativa con VHD para trabajar con discos duros virtuales, lo que facilita a los desarrolladores y administradores la creación, administración e implementación de imágenes de Windows en VHD mediante la compatibilidad de la API de la plataforma o las herramientas de administración.</span><span class="sxs-lookup"><span data-stu-id="1cb69-110">The Microsoft Windows Software Development Kit (SDK) integrates Native VHD support for working with VHDs, making it easier for developers and administrators to create, manage, and deploy Windows images in VHDs using the platform API support or management tools.</span></span> <span data-ttu-id="1cb69-111">No es necesario instalar aplicaciones independientes ni implementar un analizador de formato VHD para habilitar estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="1cb69-111">It is not necessary to install separate applications or implement a VHD format parser to enable these operations.</span></span> <span data-ttu-id="1cb69-112">Estas API permiten el uso genérico de los VHD independientemente de cualquier otra tecnología de virtualización.</span><span class="sxs-lookup"><span data-stu-id="1cb69-112">These APIs allow for generic use of VHDs independent of any other virtualization technologies.</span></span>

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span data-ttu-id="1cb69-113"><span id="run_time_requirements_heading"></span>Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="1cb69-113"><span id="run_time_requirements_heading"></span>Run-time requirements</span></span>

<span data-ttu-id="1cb69-114">VHD es compatible con Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1cb69-114">VHD is supported on Windows 7 and Windows Server 2008 R2.</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="1cb69-115"><span id="in_this_section"></span>En esta sección</span><span class="sxs-lookup"><span data-stu-id="1cb69-115"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1cb69-116">Tema</span><span class="sxs-lookup"><span data-stu-id="1cb69-116">Topic</span></span></th>
<th><span data-ttu-id="1cb69-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cb69-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cb69-118"><a href="about-vhd.md">Acerca de VHD</a></span><span class="sxs-lookup"><span data-stu-id="1cb69-118"><a href="about-vhd.md">About VHD</a></span></span></p></td>
<td><p><span data-ttu-id="1cb69-119">Describe el formato VHD con sugerencias y sugerencias de uso de la API.</span><span class="sxs-lookup"><span data-stu-id="1cb69-119">Describes the VHD format with API usage tips and suggestions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cb69-120"><a href="vhd-reference.md">Referencia de VHD</a></span><span class="sxs-lookup"><span data-stu-id="1cb69-120"><a href="vhd-reference.md">VHD Reference</a></span></span></p></td>
<td><p><span data-ttu-id="1cb69-121">Describe las funciones, estructuras y enumeraciones de la API de VHD.</span><span class="sxs-lookup"><span data-stu-id="1cb69-121">Describes the VHD API functions, structures, and enumerations.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span data-ttu-id="1cb69-122"><span id="related_topics"></span>Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1cb69-122"><span id="related_topics"></span>Related topics</span></span>

[<span data-ttu-id="1cb69-123">Servicio de disco virtual</span><span class="sxs-lookup"><span data-stu-id="1cb69-123">Virtual Disk Service</span></span>](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
