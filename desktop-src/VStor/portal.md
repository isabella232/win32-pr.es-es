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
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>Disco virtual

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>Propósito

El formato de disco duro virtual (VHD) es una especificación de formato de imagen disponible públicamente que especifica un disco duro virtual encapsulado en un único archivo, capaz de hospedar sistemas de archivos nativos mientras se admiten operaciones de archivos y discos estándar. Un ejemplo de cómo se usan los archivos VHD es la característica [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) de windows Server 2008, Virtual Server y Windows Virtual PC. Estos productos usan discos duros virtuales para contener la imagen de sistema operativo Windows utilizada por una máquina virtual como disco de arranque del sistema.

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>Audiencia de desarrolladores

El kit de desarrollo de software (SDK) de Microsoft Windows integra compatibilidad nativa con VHD para trabajar con discos duros virtuales, lo que facilita a los desarrolladores y administradores la creación, administración e implementación de imágenes de Windows en VHD mediante la compatibilidad de la API de la plataforma o las herramientas de administración. No es necesario instalar aplicaciones independientes ni implementar un analizador de formato VHD para habilitar estas operaciones. Estas API permiten el uso genérico de los VHD independientemente de cualquier otra tecnología de virtualización.

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>Requisitos de tiempo de ejecución

VHD es compatible con Windows 7 y Windows Server 2008 R2.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>En esta sección

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="about-vhd.md">Acerca de VHD</a></p></td>
<td><p>Describe el formato VHD con sugerencias y sugerencias de uso de la API.</p></td>
</tr>
<tr class="even">
<td><p><a href="vhd-reference.md">Referencia de VHD</a></p></td>
<td><p>Describe las funciones, estructuras y enumeraciones de la API de VHD.</p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Temas relacionados

[Servicio de disco virtual](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
