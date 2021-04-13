---
description: Glosario de términos usados en la documentación del SDK de virtualización de Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 365D0295-EA0B-4B40-8272-DFF62B2A6F3D
title: Glosario de Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badb8fdfd25c4b7e11529778ab2cbd3c8cee5f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278616"
---
# <a name="hyper-v-glossary"></a>Glosario de Hyper-V

En este tema se proporciona un glosario de términos que se usan en la documentación del SDK de virtualización de Windows.

<dl> <dt>

<span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**enlace**
</dt> <dd>

Proceso por el que se vinculan los servicios y las capas de software. Cuando se instala un servicio de red, se establecen las relaciones de enlace y las dependencias de los servicios.

</dd> <dt>

<span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**SnapSure**
</dt> <dd>

Una instantánea de una máquina virtual que permite a un administrador revertir la máquina virtual a su estado en el momento en que se creó el punto de control.

</dd> <dt>

<span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**unidad**
</dt> <dd>

Para reducir el tamaño de un disco duro virtual de expansión dinámica quitando el espacio no utilizado del archivo. VHD.

</dd> <dt>

<span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**disco duro virtual de diferenciación**
</dt> <dd>

Un disco duro virtual que almacena los cambios en un disco duro virtual principal asociado con el fin de mantener el elemento primario intacto. El disco de diferenciación es un archivo. vhd independiente que está asociado con el archivo. vhd del disco primario. Los cambios se siguen acumulando en el disco de diferenciación hasta que se combinan en el disco primario.

</dd> <dt>

<span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**disco duro virtual de expansión dinámica**
</dt> <dd>

Un disco duro virtual que aumenta de tamaño cada vez que se modifica. Este tipo de disco duro virtual se inicia como un archivo. vhd de 3 KB y puede crecer hasta alcanzar el tamaño máximo especificado cuando se creó el archivo. La única manera de reducir el tamaño del archivo es eliminar los datos eliminados y, a continuación, compactar el disco duro virtual.

</dd> <dt>

<span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**disco duro virtual de tamaño fijo**
</dt> <dd>

Un disco duro virtual con un tamaño fijo que se determina y para el que se asigna todo el espacio cuando se crea el disco. El tamaño del disco no cambia cuando se agregan o eliminan datos.

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Máquina virtual de generación 1**
</dt> <dd>

Una máquina virtual (VM) que contiene el mismo hardware virtual presente en versiones de Hyper-V anteriores a Windows 8.1 y Windows Server 2012 R2

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Máquina virtual de generación 2**
</dt> <dd>

Una máquina virtual (VM) que contiene un modelo de hardware virtual simplificado y utiliza el firmware UEFI en lugar del BIOS. En esta máquina virtual, la mayoría de los dispositivos emulados se quitan, lo que reduce la complejidad de la administración y la superficie expuesta a ataques de seguridad.

</dd> <dt>

<span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**sistema operativo invitado**
</dt> <dd>

Es el sistema operativo que se ejecuta en una máquina virtual.

</dd> <dt>

<span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**servicios de integración**
</dt> <dd>

Colección de servicios y controladores de software que maximizan el rendimiento y proporcionan una mejor experiencia de usuario en una máquina virtual. Los servicios de integración solo están disponibles para los sistemas operativos invitados admitidos.

</dd> <dt>

<span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**par clave-valor**
</dt> <dd>

Conjunto de elementos de datos que contiene un identificador único, denominado clave, y un valor que es los datos reales de la clave.

</dd> <dt>

<span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**equipo físico**
</dt> <dd>

Un equipo basado en hardware, en lugar de una máquina virtual basada en software.

</dd> <dt>

<span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**estado guardado**
</dt> <dd>

Manera de almacenar una máquina virtual para que se pueda reanudar rápidamente, de forma similar a un equipo portátil en hibernación. Cuando se coloca una máquina virtual en ejecución en un estado guardado, Virtual Server e Hyper-V detienen la máquina virtual, escriben los datos existentes en la memoria en archivos temporales y detienen el consumo de recursos del sistema. Al restaurar una máquina virtual a partir de un estado guardado, se devuelve a la misma condición en que se encontraba cuando se guardó su estado.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**disquete virtual**
</dt> <dd>

Es una versión basada en archivos de un disquete físico. Un disquete virtual se almacena como un archivo con la extensión de nombre de archivo. VFD.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**disco duro virtual**
</dt> <dd>

El medio de almacenamiento de una máquina virtual. Puede residir en cualquier topología de almacenamiento a la que el sistema operativo host pueda acceder, incluidos dispositivos externos, redes de área de almacenamiento y almacenamiento conectado a la red. La extensión de nombre de archivo es. VHD.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**máquina virtual**
</dt> <dd>

Un equipo dentro de un equipo, implementado en el software. Una máquina virtual emula un sistema de hardware completo, desde el procesador a la tarjeta de red, en un entorno de software independiente y aislado que permite el funcionamiento simultáneo de sistemas operativos que serían incompatibles de otro modo. Cada sistema operativo secundario se ejecuta en su propia máquina virtual de software aislado.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**configuración de la máquina virtual**
</dt> <dd>

La configuración de los recursos asignados a una máquina virtual. Algunos ejemplos son los dispositivos como los discos y los adaptadores de red, así como la memoria y los procesadores.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Servicio de administración de máquinas virtuales**
</dt> <dd>

El servicio de Hyper-V que proporciona acceso de administración a las máquinas virtuales.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**instantánea de máquina virtual**
</dt> <dd>

Una instantánea basada en archivos del estado, los datos de disco y la configuración de una máquina virtual en un momento específico.

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**red virtual**
</dt> <dd>

Una versión virtual de un conmutador de red físico. Una red virtual se puede configurar para proporcionar acceso a recursos de red locales o externos para una o más máquinas virtuales.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Administrador de redes virtuales**
</dt> <dd>

Servicio de Hyper-V que se usa para crear y administrar redes virtuales.

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**conmutador virtual**
</dt> <dd>

Vea Virtual Network.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**Cambiar el tamaño de VHDX**
</dt> <dd>

Operación que reduce o expande un disco duro virtual.

</dd> </dl>

 

 



