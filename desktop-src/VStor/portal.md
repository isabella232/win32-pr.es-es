---
description: Encapsula el disco duro en un único archivo para que lo use el sistema operativo como disco virtual. Los discos virtuales pueden funcionar como discos de arranque y pueden hospedar sistemas de archivos nativos (NTFS, FAT, ex SATA y UDFS) al tiempo que admiten operaciones estándar de archivos y discos.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Disco virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfa2d39ea786029e8be319d7affaa2214682ce05
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480991"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>Disco virtual

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>Propósito

El formato disco duro virtual (VHD) es una especificación de formato de imagen disponible públicamente que especifica un disco duro virtual encapsulado en un solo archivo, capaz de hospedar sistemas de archivos nativos al tiempo que admite operaciones estándar de archivos y discos. Un ejemplo de cómo se usan los archivos VHD es la característica [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) de Windows Server 2008, Virtual Server y Windows Virtual PC. Estos productos usan discos duros virtuales para contener Windows imagen de sistema operativo utilizada por una máquina virtual como disco de arranque del sistema.

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>Audiencia de desarrolladores

El Kit de desarrollo de software (SDK) de Microsoft Windows integra la compatibilidad con VHD nativo para trabajar con discos duros virtuales, lo que facilita a los desarrolladores y administradores la creación, administración e implementación de imágenes de Windows en discos duros virtuales mediante las herramientas de administración o soporte de API de la plataforma. No es necesario instalar aplicaciones independientes ni implementar un analizador de formato VHD para habilitar estas operaciones. Estas API permiten el uso genérico de VHD independientemente de cualquier otra tecnología de virtualización.

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>Requisitos de tiempo de ejecución

VhD se admite en Windows 7 y Windows Server 2008 R2.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>En esta sección


| Tema | Descripción | 
|-------|-------------|
| <p><a href="about-vhd.md">Acerca de VHD</a></p> | <p>Describe el formato VHD con sugerencias y sugerencias de uso de API.</p> | 
| <p><a href="vhd-reference.md">Referencia de VHD</a></p> | <p>Describe las funciones, estructuras y enumeraciones de la API de VHD.</p> | 


 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Temas relacionados

[Servicio de disco virtual](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
