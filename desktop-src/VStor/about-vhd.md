---
description: El formato disco duro virtual (VHD) es una especificación de formato de imagen disponible públicamente que permite encapsular el disco duro en un archivo individual para que lo use el sistema operativo como disco virtual de las mismas maneras que se usan los discos duros físicos.
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Acerca de VHD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a79bd7695144811a1ec98f79e736760bbaddc8ef4b7460e55c5a66353a0b2ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865965"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span id="vhd.about_vhd"></span>Acerca del disco duro virtual

El formato disco duro virtual (VHD) es [](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) una especificación de formato de imagen disponible públicamente que permite encapsular el disco duro en un archivo individual para que lo use el sistema operativo como disco *virtual* de las mismas maneras que se usan los discos duros físicos. Estos discos virtuales son capaces de hospedar sistemas de archivos nativos (NTFS, FAT, ex SATA y UDFS), al tiempo que admiten operaciones estándar de archivos y discos. La compatibilidad con la API de VHD permite la administración de los discos virtuales. Los discos virtuales creados con la API de VHD pueden funcionar como discos de arranque.

Un ejemplo de cómo se usan los archivos VHD es la característica [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) de Windows 7, Windows Server 2008, Virtual Server y Windows Virtual PC. Estos productos usan la API de VHD para contener la imagen Windows de sistema operativo utilizada por una máquina virtual como disco de arranque del sistema.

El Kit de desarrollo de software (SDK) de Microsoft Windows integra la compatibilidad con VHD nativo para trabajar con discos virtuales, lo que facilita a los desarrolladores y administradores la creación, administración e implementación de imágenes de Windows en archivos VHD mediante las herramientas de administración o compatibilidad de API de la plataforma. No es necesario instalar aplicaciones independientes ni implementar un analizador de formato VHD para habilitar estas operaciones. Estas API permiten el uso genérico de discos virtuales independientemente de cualquier otra tecnología de virtualización.

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminología

El término *memoria caché se* usa para hacer referencia al archivo físico que existe en el disco duro real. El almacén de respaldo se representa mediante un *archivo de imagen vhd*.

Los *términos dinámico,* *expandible* *y* disperso se suelen usar indistintamente al hacer referencia a discos virtuales que se pueden expandir dinámicamente. En el caso de la tecnología vhd, estos términos son idénticos.

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>Introducción a las características del sistema vhd

En el diagrama siguiente se presenta información general de las características del disco duro virtual y sus relaciones.

![Diagrama de bloques vhd](images/vhd.png)

A continuación se muestra una explicación resumida de las características descritas anteriormente.

API nativas de Windows usuario:

-   VirtDisk.dll: biblioteca común para las API de administración de VHD.

Contenedores de administración específicos del dominio del modo de usuario:

-   [API de VHD de VDS:](/windows/desktop/VDS/about-vds) contenedores del modelo de objetos VDS para las API Windows VHD.

Controladores de modo kernel:

-   VDrvRoot.sys: enumerador de unidad virtual raíz.
-   FsDepends.sys: administración de dependencias de volumen anidadas.
-   Vhdmp.sys: analizador de VHD y proveedor de propiedades de dependencia.

En la documentación del SDK de esta sección se tratan las API de VHD nativas Windows modo de usuario.

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Tipos de disco virtual

Hay consideraciones para usar discos virtuales y qué tipos de discos virtuales están disponibles:

-   **Corregido:** el archivo de imagen vhd está asignado previamente en la memoria auxiliar para el tamaño máximo solicitado.
-   **Ampliable:** también conocido como "dinámico", "ampliable dinámicamente" y "disperso", el archivo de imagen vhd solo usa tanto espacio en la memoria auxiliar como sea necesario para almacenar los datos reales que el disco virtual contiene actualmente. Al crear este tipo de disco virtual, la API de VHD no prueba espacio libre en el disco físico en función del tamaño máximo solicitado, por lo que es posible crear correctamente un disco virtual dinámico con un tamaño máximo mayor que el espacio libre disponible en disco físico. Para obtener más información, [**vea ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).
    **Nota**  El tamaño máximo de un disco virtual dinámico es de 2040 GB.

     

-   **Diferenciación:** se usa un disco virtual primario como base de este tipo, con las escrituras posteriores escritas en el disco virtual como diferencias en el nuevo archivo de imagen VHD de diferenciación, y el archivo de imagen vhd primario no se modifica. Por ejemplo, si tiene un disco virtual del sistema operativo de arranque del sistema de instalación limpia como elemento primario y designa el disco virtual de diferenciación como el disco virtual actual que va a usar el sistema, el sistema operativo del disco virtual primario permanece en su estado original para una recuperación rápida o para crear rápidamente más imágenes de arranque basadas en discos virtuales de diferenciación adicionales. Para obtener más información, [**vea MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).
    **Nota**  El tamaño máximo de un disco virtual de diferenciación es de 2040 GB.

     

Todos los tipos de disco virtual tienen un tamaño mínimo de 3 MB.

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Temas relacionados

[Acerca de VDS](/windows/desktop/VDS/about-vds)

[Referencia de VHD](vhd-reference.md)

[Especificación de formato de imagen de disco duro virtual](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
