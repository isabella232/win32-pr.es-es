---
description: Un solicitante crea un documento de componentes de copia de seguridad al inicio de la realización de una copia de seguridad.
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: Trabajar con el documento componentes de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d5d3c97696b85d589501f6d3af0b6c7d0e6d47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696425"
---
# <a name="working-with-the-backup-components-document"></a><span data-ttu-id="09525-103">Trabajar con el documento componentes de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="09525-103">Working with the Backup Components Document</span></span>

<span data-ttu-id="09525-104">Un solicitante crea un documento de componentes de copia de seguridad al inicio de la realización de una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="09525-104">A requester creates a Backup Components Document at the start of performing a backup.</span></span> <span data-ttu-id="09525-105">El documento contiene inicialmente solo una descripción del estado de la operación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="09525-105">The document initially contains only a description of the state of the backup operation.</span></span> <span data-ttu-id="09525-106">Durante la restauración, el documento debe proporcionar instrucciones sobre el modo en que un solicitante debe continuar en la copia de archivos de nuevo en el disco.</span><span class="sxs-lookup"><span data-stu-id="09525-106">During restore, the document should provide instructions on how a requester should proceed in copying files back to disk.</span></span> <span data-ttu-id="09525-107">En el transcurso de la operación de restauración, se modifica el documento componentes de copia de seguridad y contiene el estado de esa operación.</span><span class="sxs-lookup"><span data-stu-id="09525-107">In the course of the restore operation, the Backup Components Document is modified and contains the state of that operation.</span></span>

<span data-ttu-id="09525-108">A diferencia del documento de metadatos del escritor, que es de solo lectura, hay una ventana en la que el documento componentes de copia de seguridad puede ser modificado por los solicitantes y los escritores.</span><span class="sxs-lookup"><span data-stu-id="09525-108">Unlike the Writer Metadata Document, which is read-only, there is a window in which the Backup Components Document can be modified by both requesters and writers.</span></span> <span data-ttu-id="09525-109">El documento puede actualizarse hasta la generación de un evento [*BackupComplete*](vssgloss-b.md) o [*BackupShutdown*](vssgloss-b.md) durante las operaciones de copia de seguridad y hasta un evento [*postrestore*](vssgloss-p.md) durante la restauración.</span><span class="sxs-lookup"><span data-stu-id="09525-109">The document can be updated until the generation of a [*BackupComplete*](vssgloss-b.md) or [*BackupShutdown*](vssgloss-b.md) event during backup operations, and until a [*PostRestore*](vssgloss-p.md) event during restores.</span></span>

<span data-ttu-id="09525-110">Para usar el documento componentes de copia de seguridad del solicitante, es necesario conocer los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="09525-110">To use a requester's Backup Components Document requires an understanding of the following topics:</span></span>

-   [<span data-ttu-id="09525-111">Ciclo de vida de documentos de componentes de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="09525-111">Backup Components Document Life Cycle</span></span>](backup-components-document-life-cycle.md)
-   [<span data-ttu-id="09525-112">Contenido del documento componentes de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="09525-112">Backup Components Document Contents</span></span>](backup-components-document-contents.md)

 

 



