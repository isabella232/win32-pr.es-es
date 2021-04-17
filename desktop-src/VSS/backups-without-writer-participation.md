---
description: Cuando se realiza una operación de copia de seguridad de VSS sin la implicación de un escritor, todavía se puede producir la creación de la instantánea.
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: Copias de seguridad sin participación del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a782fbcb9afe532f2f123151dc7998307157b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653046"
---
# <a name="backups-without-writer-participation"></a><span data-ttu-id="b9cf1-103">Copias de seguridad sin participación del escritor</span><span class="sxs-lookup"><span data-stu-id="b9cf1-103">Backups without Writer Participation</span></span>

<span data-ttu-id="b9cf1-104">Cuando se realiza una operación de copia de seguridad de VSS sin la implicación de un escritor, todavía se puede producir la creación de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="b9cf1-104">When a VSS backup operation is conducted without the involvement of a writer, the shadow copy creation can still occur.</span></span>

<span data-ttu-id="b9cf1-105">Como se indicó en otra parte (vea el estado de la [instantánea predeterminada](shadow-copies-and-shadow-copy-sets.md)), el resultado de este tipo de instantánea es un volumen que refleja el estado de un disco en el momento de la instantánea: los datos del volumen de copia sombra pueden reflejar operaciones de e/s parciales o incompletas y se describe como si estuvieran en un [*Estado de bloqueo coherente*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="b9cf1-105">As noted elsewhere (see [Default Shadow Copy State](shadow-copies-and-shadow-copy-sets.md)), the result of this type of shadow copy is a volume reflecting the state of a disk at the time of the shadow copy: data on the shadow-copied volume may reflect incomplete or partial I/O operations and is described as being in a [*crash-consistent state*](vssgloss-c.md).</span></span>

<span data-ttu-id="b9cf1-106">Hay varias situaciones que requerirán que una aplicación de copia de seguridad funcione con datos de instantáneas coherentes de bloqueos:</span><span class="sxs-lookup"><span data-stu-id="b9cf1-106">There are several situations that will require a backup application to work with crash consistent shadow copied data:</span></span>

-   <span data-ttu-id="b9cf1-107">**Los datos están administrados por aplicaciones que no reconocen VSS**</span><span class="sxs-lookup"><span data-stu-id="b9cf1-107">**Data is managed by VSS-unaware applications**</span></span>

    <span data-ttu-id="b9cf1-108">Casi todos los sistemas tendrán algunas aplicaciones (editores de texto, lectores de correo, procesadores de palabras, etc.) que no reconocen VSS, por lo que siempre es probable que algunos de los datos de una instantánea tengan que considerarse como si estuvieran en un estado coherente con el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="b9cf1-108">Almost every system will have some applications—text editors, mail readers, word processors, and so forth—that are VSS unaware, so it is always likely that some of the data on a shadow copy will need to be thought of as being in a crash consistent state.</span></span>

    <span data-ttu-id="b9cf1-109">Este tipo de datos no suele ser crítico para el sistema o el servicio, por lo que realizar una copia de seguridad no debe ser problemático o, al menos, no ser problemático que durante una copia de seguridad convencional.</span><span class="sxs-lookup"><span data-stu-id="b9cf1-109">This sort of data is not typically system- or service-critical, so backing it up should not be problematic, or at least no more problematic than during a conventional backup.</span></span>

    <span data-ttu-id="b9cf1-110">Al igual que con los preparativos de las copias de seguridad convencionales, si es posible, los operadores de copia de seguridad deben intentar suspender o finalizar dichas aplicaciones antes de iniciar un trabajo de copia de seguridad de VSS.</span><span class="sxs-lookup"><span data-stu-id="b9cf1-110">As with preparations for conventional backups, if possible, backup operators should attempt to suspend or terminate such applications prior to starting a VSS backup job.</span></span>

-   <span data-ttu-id="b9cf1-111">**Sistema sin escritores compatibles con VSS**</span><span class="sxs-lookup"><span data-stu-id="b9cf1-111">**System with no VSS-compatible writers**</span></span>

    <span data-ttu-id="b9cf1-112">Esta situación puede ser relativamente poco frecuente, porque la mayoría de los sistemas de los que una aplicación de copia de seguridad de VSS puede realizar la copia de seguridad tendrá una versión habilitada para VSS de Windows, que debe contener escritores.</span><span class="sxs-lookup"><span data-stu-id="b9cf1-112">This situation may be relatively rare because most systems that can be backed up by a VSS backup application will have a VSS-enabled version of Windows, which should contain writers.</span></span>

    <span data-ttu-id="b9cf1-113">Sin embargo, hay ciertas circunstancias en las que puede surgir este problema, por ejemplo, si se realiza una copia de seguridad de un sistema sin compatibilidad con VSS, pero el sistema usa un dispositivo en red habilitado para VSS para su almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="b9cf1-113">However, there are certain circumstances where this problem could arise—for instance, if you are backing up a system without VSS support but the system uses a VSS-enabled networked appliance for its storage.</span></span>

    <span data-ttu-id="b9cf1-114">Aunque la copia de seguridad del estado de un sistema desde una imagen coherente con bloqueos no es óptima, puede ser suficiente para que un equipo se reinicie en un estado operativo.</span><span class="sxs-lookup"><span data-stu-id="b9cf1-114">Although backing up a system's state from a crash-consistent image is not optimal, it may be sufficient for a computer to reboot to an operational status.</span></span> <span data-ttu-id="b9cf1-115">En muchos casos, el equipo se recuperará de las operaciones de e/s incompletas en los sistemas de archivos y funcionará con normalidad.</span><span class="sxs-lookup"><span data-stu-id="b9cf1-115">In many cases, the computer will recover from any incomplete I/O operations to the file systems and will operate normally.</span></span>

-   <span data-ttu-id="b9cf1-116">**Un solicitante que elige no trabajar con los escritores del sistema**</span><span class="sxs-lookup"><span data-stu-id="b9cf1-116">**A requester choosing not to work with the system writers**</span></span>

    <span data-ttu-id="b9cf1-117">Esta circunstancia se produciría si un solicitante decidió no agregar ningún componente de escritura o deshabilitar todos los escritores.</span><span class="sxs-lookup"><span data-stu-id="b9cf1-117">This circumstance would occur if a requester chose to add no writer components, or disabling all writers.</span></span>

    <span data-ttu-id="b9cf1-118">En general, no se recomienda realizar copias de seguridad de esta manera.</span><span class="sxs-lookup"><span data-stu-id="b9cf1-118">Performing backups in this way is generally discouraged.</span></span> <span data-ttu-id="b9cf1-119">Aunque el volumen de copia sombra del que se va a realizar la copia de seguridad puede ser suficiente para restaurar un sistema en ejecución, no es deseable.</span><span class="sxs-lookup"><span data-stu-id="b9cf1-119">Although the shadow-copied volume to back up might be sufficient to restore a system to running, it is not desirable.</span></span> <span data-ttu-id="b9cf1-120">De hecho, dado que los escritores que se ejecutan en el sistema están diseñados con funcionalidad para cooperar con VSS e instantáneas, la realización de copias de seguridad de los datos de esta manera podría provocar inestabilidad.</span><span class="sxs-lookup"><span data-stu-id="b9cf1-120">In fact, given that the writers running on the system are designed with functionality to cooperate with VSS and shadow copies, backing up their data in this way might result in instability.</span></span>

 

 



