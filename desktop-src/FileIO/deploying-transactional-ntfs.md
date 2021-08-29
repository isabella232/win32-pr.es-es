---
description: Control de almacenamiento en caché en NTFS transaccional.
ms.assetid: 0fd272ee-cf5f-4ba9-b8aa-ff0016f51d4b
title: Implementación de NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ca732bedaa833227e3960337dcf1ed068b7659a0f4c01849181e5bdfff7a7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982115"
---
# <a name="deploying-transactional-ntfs"></a>Implementación de NTFS transaccional

NTFS transaccional (TxF), como la mayoría de los mecanismos de transacción, depende del orden correcto de las escrituras de datos. Garantizar una ordenación de escritura adecuada requiere un control explícito del almacenamiento en caché de datos. Para cumplir este requisito, TxF requiere que las unidades de disco implementen los mecanismos de control de almacenamiento en caché que forman parte de interfaces de unidades estandarizadas como SCSI, SATA y ATA.

El mecanismo de control de almacenamiento en caché utilizado por TxF es una marca conocida como función Force Unit Access (FUA). Esta marca especifica que la unidad debe escribir los datos en un almacenamiento multimedia estable antes de que se complete la señalización. En determinados puntos críticos dentro de una transacción, TxF debe emitir un FUA para asegurarse de que algunos datos de control necesarios para revertir correctamente una transacción no se pierdan si se produce un error de alimentación.

Las unidades de disco de clase de servidor (SCSI y canal de fibra) generalmente admiten la marca FUA. A partir de Vista, Windows admite la marca FUA solo para discos SCSI y de canal de fibra.

En las unidades estándar (ATA/SATA/USB), TxF tiene períodos de vulnerabilidad durante los cuales un error de alimentación de la unidad puede dar lugar a que TxF no pueda revertir correctamente la transacción, lo que deja los datos en un estado incoherente a menos que la memoria caché de escritura de la unidad esté deshabilitada.

Algunos adaptadores de bus host (HBA) y controladores de almacenamiento (por ejemplo, sistemas RAID) tienen memorias caché integradas con batería. Dado que estos dispositivos conservan los datos almacenados en caché si se produce un error de alimentación, no es necesario que los discos conectados a ellos respetan la marca FUA. Además, un disco cuya fuente de alimentación está protegida por una fuente de alimentación ininterrumpida (UPS) no necesita respetar la marca FUA. Esto se debe a que el UPS mantendrá la energía lo suficientemente larga como para que el disco vacíe su memoria caché en el medio.

Al deshabilitar la memoria caché de escritura de una unidad, se elimina el requisito de que la unidad respeta la marca FUA. Puede deshabilitar el almacenamiento en caché de escritura de un disco mediante la emisión del código de control [**IOCTL \_ DISK SET CACHE \_ \_ \_ INFORMATION**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_set_cache_information) al disco. El estado de la caché de escritura (on/off) se conservará en los reinicios del sistema. La emisión de este código de control tendrá consecuencias de rendimiento muy significativas para todas las E/S emitidas en ese disco, lo que probablemente será una degradación notable del rendimiento. El uso de este código de control debe tenerse en cuenta cuidadosamente antes de la implementación.

> [!Note]  
> Para que TxF sea capaz de proteger de forma coherente la integridad de los datos a través de errores de alimentación, el sistema debe cumplir al menos uno de los siguientes criterios:
>
> -   Use discos de clase de servidor (SCSI, canal de fibra).
> -   Asegúrese de que los discos están conectados a un HBA de almacenamiento en caché con batería.
> -   Use un controlador de almacenamiento (por ejemplo, el sistema RAID) como dispositivo de almacenamiento.
> -   Asegúrese de que la alimentación del disco está protegida por un UPS.
> -   Asegúrese de que la característica de almacenamiento en caché de escritura del disco está deshabilitada.

 

 

 



