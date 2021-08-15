---
description: Describe un disco duro, la creación de particiones y el registro de arranque maestro.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Dispositivos de disco y particiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758454c9fc9e684e918646bf99869c7544b3b02c0201eb2ba507f8ffbdc303d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015383"
---
# <a name="disk-devices-and-partitions"></a>Dispositivos de disco y particiones

Un disco duro consta de un conjunto de bandejas apiladas, cada una de las cuales tiene datos almacenados de forma inferida en círculos concéntricas o *realiza un seguimiento* de . Cada bandeja tiene dos caras, una a cada lado del bandeja, que lee o escribe datos a medida que gira el disco. Una *unidad de disco duro* controla el posicionamiento, la lectura y la escritura del disco duro. Tenga en cuenta que las cabezas de todos los bandejas se sitúan como una unidad.

La unidad direccionable más pequeña de una pista es un *sector*. Un *cilindro* se define como el conjunto de pistas que aparecen en la misma ubicación en cada bandeja. Por ejemplo, en el diagrama siguiente se muestra un disco duro con cuatro bandejas. El cilindro X consta de ocho pistas (pista X de cada lado de cada bandeja).

![disco duro, incluidas pistas, sectores y bandejas](images/diskdevice.png)

Un disco duro puede contener una o varias regiones lógicas *denominadas particiones*. Las particiones se crean cuando el usuario da formato a un disco duro como *un disco básico.* Windows también admite *discos dinámicos,* que no se de abordan en este tema. Para obtener más información sobre los discos básicos y los discos dinámicos, vea [Discos básicos y dinámicos.](basic-and-dynamic-disks.md)

La creación de varias particiones en un disco permite la apariencia de tener unidades de disco duro independientes. Por ejemplo, un sistema con un disco duro que tiene una partición contiene un único volumen, designado por el sistema como unidad C. Un sistema con un disco duro con dos particiones normalmente contiene las unidades C y D. Tener varias particiones en un disco duro puede facilitar la administración del sistema, por ejemplo, organizar archivos o admitir varios usuarios.

El primer sector físico de un disco básico contiene una estructura de datos conocida como registro de arranque maestro (MBR). MBR contiene lo siguiente:

-   Un programa de arranque (hasta 442 bytes de tamaño)
-   Una firma de disco (un número único de 4 bytes)
-   Una tabla de particiones (hasta cuatro entradas)
-   Marcador de fin de MBR (siempre 0x55AA)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de volúmenes](about-volume-management.md)
</dt> <dt>

[Discos básicos y dinámicos](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



