---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f60a456ce6ea795dc8376c0f707d028523cec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809806"
---
# <a name="f-volume-shadow-copy-service"></a><span data-ttu-id="1577a-103">F (Servicio de instantáneas de volumen)</span><span class="sxs-lookup"><span data-stu-id="1577a-103">F (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="1577a-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="1577a-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="1577a-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**componente de grupo de archivos**</span><span class="sxs-lookup"><span data-stu-id="1577a-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**file group component**</span></span>
</dt> <dd>

<span data-ttu-id="1577a-106">Grupo de archivos que no son los que se usan como base de datos y que define un escritor, ya que es necesario controlarlos como una unidad durante las operaciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="1577a-106">A group of files other than those used as a database and defined by a writer as needing to be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="1577a-107">Vea también [*componente*](vssgloss-c.md), [*componente de base de datos*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="1577a-107">See also [*component*](vssgloss-c.md), [*database component*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577a-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**conjunto de archivos**</span><span class="sxs-lookup"><span data-stu-id="1577a-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**file set**</span></span>
</dt> <dd>

<span data-ttu-id="1577a-109">Combinación de una ruta de acceso, especificación de archivo y marca recursiva que describe uno de un archivo o un grupo de archivos.</span><span class="sxs-lookup"><span data-stu-id="1577a-109">The combination of a path, file specification, and recursive flag describing one of a file or group of files.</span></span> <span data-ttu-id="1577a-110">Por ejemplo, los archivos se agregan a los componentes de los conjuntos de archivos.</span><span class="sxs-lookup"><span data-stu-id="1577a-110">For example, files are added to components in file sets.</span></span>

<span data-ttu-id="1577a-111">A menos que se indique lo contrario, las rutas de acceso de un conjunto de archivos son rutas de Windows estándar y pueden contener variables de entorno (por ejemplo,% SystemRoot%) pero no puede contener caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="1577a-111">Unless otherwise indicated, a file set's paths are standard Windows paths and can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.</span></span> <span data-ttu-id="1577a-112">No es necesario que la ruta de acceso finalice con una barra diagonal inversa (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="1577a-112">There is no requirement that the path end with a backslash ("\\").</span></span> <span data-ttu-id="1577a-113">Depende de las aplicaciones que recuperan esta información para comprobarlo.</span><span class="sxs-lookup"><span data-stu-id="1577a-113">It is up to applications that retrieve this information to check it.</span></span>

<span data-ttu-id="1577a-114">La especificación de archivo incluida en un conjunto de archivos indica el nombre del archivo o los archivos que incluye.</span><span class="sxs-lookup"><span data-stu-id="1577a-114">The file specification contained in a file set indicates the name of the file or files it includes.</span></span> <span data-ttu-id="1577a-115">Esta especificación de archivo no puede contener especificaciones de directorio (por ejemplo, sin barras diagonales inversas), pero puede contener el carácter?</span><span class="sxs-lookup"><span data-stu-id="1577a-115">This file specification cannot contain directory specifications (for example, no backslashes) but can contain the ?</span></span> <span data-ttu-id="1577a-116">y \* caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="1577a-116">and \* wildcard characters.</span></span>

<span data-ttu-id="1577a-117">La etiqueta recursiva es un valor booleano que especifica si la ruta de acceso del conjunto de archivos se debe tratar como un solo directorio o si indica una jerarquía de directorios que se va a atravesar de forma recursiva.</span><span class="sxs-lookup"><span data-stu-id="1577a-117">The recursive tag is a Boolean specifying whether the file set's path should be treated as a only a single directory or if it indicates a hierarchy of directories to be traversed recursively.</span></span> <span data-ttu-id="1577a-118">El valor booleano es **true** si la ruta de acceso se trata como una jerarquía de directorios que se va a recorrer de forma recursiva, o bien **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1577a-118">The Boolean is **true** if the path is treated as a hierarchy of directories to be traversed recursively, or **false** if not.</span></span>

<span data-ttu-id="1577a-119">La información sobre un conjunto de archivos se devuelve a través de instancias de la interfaz **IVssWMFiledesc** y puede contener información adicional que incluye rutas de acceso alternativas, asignaciones de ubicaciones alternativas y configuraciones de compatibilidad con esquemas de nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="1577a-119">Information about a file set is returned through instances of the **IVssWMFiledesc** interface, and can contain additional information includes alternate paths, alternate location mappings, and file-level schema support settings.</span></span>

<span data-ttu-id="1577a-120">Vea también [*ruta alternativa*](vssgloss-a.md), [*asignación de ubicación alternativa*](vssgloss-a.md), [*componente*](vssgloss-c.md), *especificación de archivo*.</span><span class="sxs-lookup"><span data-stu-id="1577a-120">See also [*alternate path*](vssgloss-a.md), [*alternate location mapping*](vssgloss-a.md), [*component*](vssgloss-c.md), *file specification*.</span></span>

</dd> <dt>

<span data-ttu-id="1577a-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**Especificación de archivo**</span><span class="sxs-lookup"><span data-stu-id="1577a-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**file specification**</span></span>
</dt> <dd>

<span data-ttu-id="1577a-122">Se usa para hacer coincidir los archivos de un directorio y definir un conjunto de archivos.</span><span class="sxs-lookup"><span data-stu-id="1577a-122">Used to match files within a directory and to define a file set.</span></span> <span data-ttu-id="1577a-123">No puede contener especificaciones de directorio (por ejemplo, sin barras diagonales inversas), pero puede contener el carácter?</span><span class="sxs-lookup"><span data-stu-id="1577a-123">It cannot contain directory specifications (for example, no backslashes) but it can contain the ?</span></span> <span data-ttu-id="1577a-124">y \* caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="1577a-124">and \* wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="1577a-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Servicio de replicación de archivos**</span><span class="sxs-lookup"><span data-stu-id="1577a-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**File Replication Service**</span></span>
</dt> <dd>

<span data-ttu-id="1577a-126">Se usa para replicar archivos del sistema en un directorio de volumen del sistema (SysVol) redundante para admitir la supervivencia del sistema de archivos, especialmente en el caso de los sistemas de archivos distribuidos.</span><span class="sxs-lookup"><span data-stu-id="1577a-126">Used to replicate system files in a redundant system volume (SysVol) directory to support file system survivability, particularly for distributed file systems.</span></span>

</dd> <dt>

<span data-ttu-id="1577a-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**Inmovilice**</span><span class="sxs-lookup"><span data-stu-id="1577a-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**freeze**</span></span>
</dt> <dd>

<span data-ttu-id="1577a-128">Un período de tiempo durante el proceso de creación de instantáneas cuando todos los escritores han vaciado sus escrituras en los volúmenes y no inician escrituras adicionales.</span><span class="sxs-lookup"><span data-stu-id="1577a-128">A period of time during the shadow copy creation process when all writers have flushed their writes to the volumes and are not initiating additional writes.</span></span>

</dd> <dt>

<span data-ttu-id="1577a-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Evento Freeze**</span><span class="sxs-lookup"><span data-stu-id="1577a-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Freeze event**</span></span>
</dt> <dd>

<span data-ttu-id="1577a-130">Un evento de VSS que indica que hay una inmovilización de instantáneas en curso.</span><span class="sxs-lookup"><span data-stu-id="1577a-130">A VSS event indicating that a shadow copy freeze is in progress.</span></span> <span data-ttu-id="1577a-131">Vea también *inmovilizar*, [*instantánea*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="1577a-131">See also *freeze*, [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577a-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**aplicaciones de nivel de front-end**</span><span class="sxs-lookup"><span data-stu-id="1577a-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**front-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="1577a-133">Indica el punto en el que se notifica a un escritor de una inmovilización de VSS.</span><span class="sxs-lookup"><span data-stu-id="1577a-133">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="1577a-134">Los escritores que se inicializaron como aplicaciones de nivel de front-end reciben una notificación antes de que los escritores se inicialicen como aplicaciones de nivel de back-end o como aplicaciones de nivel de sistema.</span><span class="sxs-lookup"><span data-stu-id="1577a-134">Writers that were initialized as front-end level applications are notified prior to writers initialized either as back-end level applications or as system-level applications.</span></span> <span data-ttu-id="1577a-135">Vea también [*nivel de aplicación*](vssgloss-a.md), [*aplicaciones de nivel de back-end*](vssgloss-b.md), [*aplicaciones de nivel de sistema*](vssgloss-s.md), [*escritor*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="1577a-135">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> </dl>

 

 



