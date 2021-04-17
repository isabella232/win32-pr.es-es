---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541715"
---
# <a name="w-volume-shadow-copy-service"></a><span data-ttu-id="6f2fc-103">W (Servicio de instantáneas de volumen)</span><span class="sxs-lookup"><span data-stu-id="6f2fc-103">W (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="6f2fc-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="6f2fc-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="6f2fc-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Protección de archivos de Windows**</span><span class="sxs-lookup"><span data-stu-id="6f2fc-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="6f2fc-106">Servicio del sistema que protege los archivos especiales del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-106">A system service that protects special operating system files.</span></span> <span data-ttu-id="6f2fc-107">Si uno de estos archivos se elimina o se sobrescribe, la protección de archivos de Windows reemplaza el archivo por el original de su memoria caché.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-107">If one of these files is deleted or overwritten, Windows File Protection replaces the file with the original from its cache.</span></span>

</dd> <dt>

<span data-ttu-id="6f2fc-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**escritor**</span><span class="sxs-lookup"><span data-stu-id="6f2fc-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**writer**</span></span>
</dt> <dd>

<span data-ttu-id="6f2fc-109">Aplicación que coordina sus operaciones de e/s con las operaciones relacionadas con instantáneas y instantáneas de VSS (como copias de seguridad y restauraciones) para que sus datos contenidos en el volumen de la instantánea se encuentren en un estado coherente.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-109">An application that coordinates its I/O operations with VSS shadow copy and shadow copy related operations (such as backups and restores) so that their data contained on the shadow copied volume is in a consistent state.</span></span>

<span data-ttu-id="6f2fc-110">Para admitir esta coordinación, un escritor debe implementar una instancia de una clase derivada de la clase base abstracta **CVssWriter** para comunicarse con la infraestructura de VSS.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-110">To support this coordination, a writer must implement an instance of a class derived from the abstract base class **CVssWriter** to communicate with the VSS infrastructure.</span></span> <span data-ttu-id="6f2fc-111">Consulte también [*instantánea*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="6f2fc-111">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f2fc-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**Writer (clase)**</span><span class="sxs-lookup"><span data-stu-id="6f2fc-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**writer class**</span></span>
</dt> <dd>

<span data-ttu-id="6f2fc-113">Identificador único global (GUID) proporcionado por un escritor durante la inicialización para indicar que pertenece a un tipo determinado de escritores.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-113">A globally unique identifier (GUID) supplied by a writer during initialization to indicate that it belongs to a given type of writers.</span></span> <span data-ttu-id="6f2fc-114">Por ejemplo, varias implementaciones de un escritor podrían compartir el mismo identificador de clase del escritor.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-114">For instance, multiple implementations of a writer could share the same writer class ID.</span></span>

<span data-ttu-id="6f2fc-115">Los escritores de la misma clase se pueden distinguir por sus instancias del escritor.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-115">Writers of the same class may be distinguished by their writer instances.</span></span> <span data-ttu-id="6f2fc-116">Es un desarrollador de aplicaciones quien debe especificar las clases del escritor.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-116">It is up to an application developer to specify writer classes.</span></span> <span data-ttu-id="6f2fc-117">Vea también *instancia del escritor*.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-117">See also *writer instance*.</span></span>

</dd> <dt>

<span data-ttu-id="6f2fc-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**instancia del escritor**</span><span class="sxs-lookup"><span data-stu-id="6f2fc-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**writer instance**</span></span>
</dt> <dd>

<span data-ttu-id="6f2fc-119">Identificador único global (GUID) proporcionado por VSS para cada proceso de escritura que se ejecuta en un sistema.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-119">A globally unique identifier (GUID) supplied by VSS for each writer process running on a system.</span></span> <span data-ttu-id="6f2fc-120">Cada vez que se inicia el escritor, se genera un valor único para la instancia del escritor.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-120">A unique value for the writer instance is generated each time the writer starts.</span></span>

</dd> <dt>

<span data-ttu-id="6f2fc-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Documento de metadatos de escritor**</span><span class="sxs-lookup"><span data-stu-id="6f2fc-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Writer Metadata Document**</span></span>
</dt> <dd>

<span data-ttu-id="6f2fc-122">Documento XML creado por un escritor (mediante la interfaz **IVssCreateWriterMetadata** ) que contiene información sobre el estado y los componentes del escritor.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-122">An XML document created by a writer (using the **IVssCreateWriterMetadata** interface) containing information about the writer's state and components.</span></span> <span data-ttu-id="6f2fc-123">Un solicitante puede consultar los documentos de metadatos del escritor (mediante la interfaz **IVssExamineWriterMetadata** ) al realizar una operación de restauración o de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-123">A requester can query Writer Metadata Documents (using the **IVssExamineWriterMetadata** interface) when performing a restore or backup operation.</span></span>

<span data-ttu-id="6f2fc-124">Un documento de metadatos de escritor contiene la lista de todos los componentes de un escritor, cualquiera de los cuales puede participar en una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-124">A Writer Metadata Document contains the list of all of a writer's components, any one of which might participate in a backup.</span></span> <span data-ttu-id="6f2fc-125">Esto difiere del documento componentes de copia de seguridad del solicitante, que solo contiene los componentes incluidos explícitamente para una operación de copia de seguridad o restauración.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-125">This differs from the requester's Backup Components Document, which contains only those components explicitly included for a backup or restore operation.</span></span>

<span data-ttu-id="6f2fc-126">Una vez construida, el documento de metadatos del escritor debe verse como un objeto de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-126">Once constructed, the Writer Metadata Document should be viewed as a read-only object.</span></span> <span data-ttu-id="6f2fc-127">Se puede guardar en el disco.</span><span class="sxs-lookup"><span data-stu-id="6f2fc-127">It can be saved to disk.</span></span> <span data-ttu-id="6f2fc-128">Vea también [*documento componentes de copia de seguridad*](vssgloss-b.md), [*inclusión explícita de componentes*](vssgloss-e.md), [*inclusión implícita de componentes*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="6f2fc-128">See also [*Backup Components Document*](vssgloss-b.md), [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> </dl>

 

 



