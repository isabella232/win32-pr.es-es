---
description: Describe un disco duro, la creación de particiones y el registro de arranque maestro.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Dispositivos y particiones de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063b943d33118a45cb6ab4c304569094af2c32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562601"
---
# <a name="disk-devices-and-partitions"></a>Dispositivos y particiones de disco

Un disco duro se compone de un conjunto de discos apilados, cada uno de los cuales tiene datos almacenados de forma magnética en círculos concéntricos o *pistas*. Cada platter tiene dos cabezas, una en cada lado del platter, que lee o escribe datos a medida que el disco gira. Una *unidad de disco duro* controla el posicionamiento, la lectura y la escritura del disco duro. Tenga en cuenta que los encabezados de todos los Platters están colocados como una unidad.

La unidad más pequeña direccionable de una pista es un *sector*. Un *cilindro* se define como el conjunto de pistas que aparecen en la misma ubicación en cada platter. Por ejemplo, en el diagrama siguiente se muestra un disco duro con cuatro platters. El cilindro X está formado por ocho pistas (pista X desde cada lado de cada platter).

![disco duro, incluidos pistas, sectores y platters](images/diskdevice.png)

Un disco duro puede contener una o varias regiones lógicas denominadas *particiones*. Las particiones se crean cuando el usuario da formato a un disco duro como *disco básico*. Windows también admite *discos dinámicos*, que no se describen en este tema. Para obtener más información acerca de los discos básicos y los discos dinámicos, consulte [discos básicos y dinámicos](basic-and-dynamic-disks.md).

La creación de varias particiones en un disco permite la aparición de unidades de disco duro independientes. Por ejemplo, un sistema con un disco duro que tiene una partición contiene un solo volumen, designado por el sistema como la unidad C. Un sistema con un disco duro con dos particiones normalmente contiene las unidades C y D. Tener varias particiones en un disco duro puede facilitar la administración del sistema, por ejemplo, para organizar archivos o para admitir varios usuarios.

El primer sector físico de un disco básico contiene una estructura de datos conocida como registro de arranque maestro (MBR). El MBR contiene lo siguiente:

-   Un programa de arranque (hasta 442 bytes de tamaño)
-   Una firma de disco (un número de 4 bytes único)
-   Una tabla de particiones (hasta cuatro entradas)
-   Un marcador de fin de MBR (siempre 0x55AA)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de volúmenes](about-volume-management.md)
</dt> <dt>

[Discos básicos y dinámicos](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



