---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb67a0f4ae622e0fead791d1876236794806c9b9e725d1c60f7712fd44cbe573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118842567"
---
# <a name="w-volume-shadow-copy-service"></a>W (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) H [](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N O](vssgloss-n.md) [](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z

<dl> <dt>

<span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows Protección de archivos**
</dt> <dd>

Un servicio del sistema que protege los archivos de sistema operativo especiales. Si se elimina o sobrescribe uno de estos archivos, Windows File Protection reemplaza el archivo por el original de su caché.

</dd> <dt>

<span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**Escritor**
</dt> <dd>

Una aplicación que coordina sus operaciones de E/S con operaciones relacionadas con instantáneas de VSS y instantáneas (como copias de seguridad y restauraciones) para que sus datos contenidos en el volumen de instantáneas se encuentran en un estado coherente.

Para admitir esta coordinación, un escritor debe implementar una instancia de una clase derivada de la clase base abstracta **CVssWriter** para comunicarse con la infraestructura de VSS. Consulte también [*instantánea.*](vssgloss-s.md)

</dd> <dt>

<span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**writer (clase)**
</dt> <dd>

Identificador único global (GUID) proporcionado por un escritor durante la inicialización para indicar que pertenece a un tipo determinado de escritores. Por ejemplo, varias implementaciones de un sistema de escritura podrían compartir el mismo identificador de clase de escritor.

Los escritores de la misma clase pueden distinguirse por sus instancias de escritor. Es un desarrollador de aplicaciones el que debe especificar clases de escritor. Vea también la *instancia de escritor*.

</dd> <dt>

<span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**instancia de escritor**
</dt> <dd>

Identificador único global (GUID) proporcionado por VSS para cada proceso de escritura que se ejecuta en un sistema. Cada vez que se inicia el sistema de escritura, se genera un valor único para la instancia de escritor.

</dd> <dt>

<span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Documento de metadatos del escritor**
</dt> <dd>

Documento XML creado por un escritor (mediante la interfaz **IVssCreateWriterMetadata)** que contiene información sobre el estado y los componentes del escritor. Un solicitante puede consultar los documentos de metadatos del escritor (mediante la **interfaz IVssExgvWriterMetadata)** al realizar una operación de restauración o copia de seguridad.

Un documento de metadatos del escritor contiene la lista de todos los componentes de un escritor, cualquiera de los cuales puede participar en una copia de seguridad. Esto difiere del documento componentes de copia de seguridad del solicitante, que contiene solo los componentes incluidos explícitamente para una operación de copia de seguridad o restauración.

Una vez construido, el documento de metadatos del escritor se debe ver como un objeto de solo lectura. Se puede guardar en el disco. Vea también Documento de [*componentes de copia de seguridad*](vssgloss-b.md), [*inclusión explícita de componentes,*](vssgloss-e.md) [*inclusión implícita de componentes*](vssgloss-i.md).

</dd> </dl>

 

 



