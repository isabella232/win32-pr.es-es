---
title: Copia de seguridad
description: Permita que las aplicaciones de copia de seguridad se comuniquen con otras aplicaciones y servicios sobre las operaciones de copia de seguridad y restauración. Realice una copia de seguridad en cinta, inicialice la cinta y recupere la información de la unidad de cinta. Mantener archivos duplicados con el almacén de instancia única (SIS).
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- Copia de seguridad de backup
- copia de seguridad, Inicio
- restauración de copias de seguridad de operaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689a5a4613bdf029b270947b523727ea00a6e05d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149451"
---
# <a name="backup"></a>Copia de seguridad

Las claves del registro para copias de seguridad y restauración permiten a las aplicaciones de copia de seguridad comunicarse con otras aplicaciones y servicios sobre las operaciones de copia de seguridad y restauración. Para obtener más información, vea [claves y valores del registro para copias de seguridad y restauración](registry-keys-for-backup-and-restore.md).

La API de copia de seguridad en cinta permite a las aplicaciones de copia de seguridad leer y escribir en una cinta, inicializar una cinta y recuperar la información de la unidad de cinta o cinta. Para obtener más información, consulte [copia de seguridad en cinta](tape-backup.md).

El almacén de instancia única (SIS) es una arquitectura diseñada para mantener archivos duplicados con una sobrecarga mínima. La aplicación de copia de seguridad usa la API de copia de seguridad de SIS para tener acceso a la arquitectura de SIS. Para obtener más información, vea [almacenamiento de instancia única y copia de seguridad de SIS](single-instance-store-and-sis-backup.md).

La copia de seguridad y restauración de archivos cifrados está habilitada por la API de cifrado sin formato, que lee y escribe archivos cifrados y mantiene los datos en formato cifrado. La API permite que se realicen copias de seguridad y restauraciones de los datos cifrados de estos archivos, a la vez que se cumplen los objetivos de mantenimiento de la seguridad de los datos de los que se ha realizado una copia de seguridad y que se pueden usar en una aplicación que no tiene permiso para utilizar las claves de cifrado en el archivo. Para obtener más información, vea [copia de seguridad y restauración de archivos cifrados](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).

La herramienta Srdelayed puede permitir que las aplicaciones de recuperación del estado del sistema muevan, eliminen y establezcan el nombre corto de los archivos del sistema. Para obtener más información, vea [Srdelayed.exe](srdelayed-exe.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de copia de seguridad](backup-reference.md)
</dt> </dl>

 

 