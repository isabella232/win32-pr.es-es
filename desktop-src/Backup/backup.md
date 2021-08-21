---
title: Backup
description: Permitir que las aplicaciones de copia de seguridad se comuniquen con otras aplicaciones y servicios sobre las operaciones de copia de seguridad y restauración. Realice una copia de seguridad de cinta, inicialice la cinta y recupere la información de la unidad de cinta. Mantener archivos duplicados con un almacén de instancia única (SIS).
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- copia de seguridad de copia de seguridad
- copia de seguridad de copia de seguridad , inicio
- operaciones de restauración Copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efe2668df47c271aba5befc3ba380c313b7bc15c11162a29b8364be6eb3fead
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588895"
---
# <a name="backup"></a>Backup

Las claves del Registro para copia de seguridad y restauración permiten que las aplicaciones de copia de seguridad se comuniquen con otras aplicaciones y servicios sobre las operaciones de copia de seguridad y restauración. Para obtener más información, vea Claves y valores [del Registro para copia de seguridad y restauración.](registry-keys-for-backup-and-restore.md)

La API de copia de seguridad de cinta permite a las aplicaciones de copia de seguridad leer y escribir en una cinta, inicializar una cinta y recuperar información de cinta o unidad de cinta. Para obtener más información, vea [Copia de seguridad en cinta.](tape-backup.md)

El almacén de instancia única (SIS) es una arquitectura diseñada para mantener archivos duplicados con un mínimo de sobrecarga. La aplicación de copia de seguridad usa la API de copia de seguridad de SIS para acceder a la arquitectura de SIS. Para obtener más información, vea [Almacenamiento de instancia única y Copia de seguridad de SIS.](single-instance-store-and-sis-backup.md)

La COPIA de seguridad y restauración de archivos cifrados está habilitada por la API de cifrado sin formato, que lee y escribe archivos cifrados mientras mantiene los datos en formato cifrado. La API permite realizar copias de seguridad y restaurar los datos cifrados de estos archivos, a la vez que se mantienen los objetivos de mantener la seguridad de los datos de los que se ha hecho una copia de seguridad y que una aplicación que carece de permiso para usar las claves de cifrado en el archivo. Para obtener más información, vea [Copia de seguridad y restauración de archivos cifrados.](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files)

La herramienta Srdelayed puede permitir que las aplicaciones de recuperación de estado del sistema muevan, eliminen y establezcan el nombre corto de los archivos del sistema. Para obtener más información, [ veaSrdelayed.exe](srdelayed-exe.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de copia de seguridad](backup-reference.md)
</dt> </dl>

 

 