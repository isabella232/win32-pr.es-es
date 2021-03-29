---
description: Control de almacenamiento en caché en NTFS transaccional.
ms.assetid: 0fd272ee-cf5f-4ba9-b8aa-ff0016f51d4b
title: Implementar NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7c44e0ad3b83854e56d18171072a7cb4615d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001569"
---
# <a name="deploying-transactional-ntfs"></a>Implementar NTFS transaccional

NTFS transaccional (TxF), al igual que la mayoría de los mecanismos de transacciones, depende del orden correcto de las escrituras de datos. Garantizar el orden correcto de escritura requiere un control explícito del almacenamiento en caché de los datos. Para cumplir este requisito, TxF requiere que las unidades de disco implementen los mecanismos de control de almacenamiento en caché que forman parte de interfaces de unidad normalizadas como SCSI, SATA y ATA.

El mecanismo de control de almacenamiento en caché que usa TxF es una marca conocida como la función Force Unit Access (FUA). Esta marca especifica que la unidad debe escribir los datos en el almacenamiento de medios estable antes de que se complete la señalización. En determinados puntos críticos de una transacción, TxF debe emitir un FUA para asegurarse de que algunos datos de control necesarios para revertir correctamente una transacción no se pierdan si se produce un error de alimentación.

Las unidades de disco de clase de servidor (canal SCSI y Fiber) suelen admitir la marca FUA. A partir de vista, Windows admite la marca FUA solo para discos SCSI y de canal de fibra.

En las unidades de disco (ATA/SATA/USB), TxF tiene períodos de vulnerabilidades durante los cuales un error de alimentación de la unidad puede dar lugar a que TxF no pueda revertir correctamente la transacción, lo que evita que los datos tengan un estado incoherente a menos que la memoria caché de escritura de la unidad esté deshabilitada.

Algunos adaptadores de bus host (HBA) y controladores de almacenamiento (por ejemplo, sistemas RAID) tienen memorias caché integradas con respaldo de batería. Dado que estos dispositivos conservan los datos en caché si se produce un error de alimentación, no es necesario que todos los discos conectados a ellos cumplan la marca FUA. Además, un disco cuya fuente de alimentación esté protegida por un sistema de alimentación ininterrumpida (SAI) no necesita cumplir la marca FUA. Esto se debe a que el SAI mantendrá el tiempo suficiente para que el disco vacíe su memoria caché al medio.

Al deshabilitar la caché de escritura de una unidad, se elimina el requisito de que la unidad respete la marca FUA. Puede deshabilitar el almacenamiento en caché de escritura de un disco emitiendo el código de control de la [**\_ \_ \_ memoria caché \_ del conjunto de discos ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_set_cache_information) en el disco. El estado de la memoria caché de escritura (activada/desactivada) se conservará entre los reinicios del sistema. La emisión de este código de control tendrá consecuencias de rendimiento muy significativas para todas las operaciones de e/s emitidas en ese disco, lo que probablemente supondrá una degradación notable del rendimiento. El uso de este código de control debe considerarse detenidamente antes de la implementación.

> [!Note]  
> Para que TxF sea capaz de proteger sistemáticamente la integridad de los datos a través de errores de energía, el sistema debe cumplir al menos uno de los siguientes criterios:
>
> -   Usar discos de clase de servidor (SCSI, canal de fibra).
> -   Asegúrese de que los discos estén conectados a un HBA de almacenamiento en caché con respaldo de batería.
> -   Use un controlador de almacenamiento (por ejemplo, sistema RAID) como dispositivo de almacenamiento.
> -   Asegúrese de que el disco está protegido por un SAI.
> -   Asegúrese de que la característica de almacenamiento en caché de escritura del disco está deshabilitada.

 

 

 



