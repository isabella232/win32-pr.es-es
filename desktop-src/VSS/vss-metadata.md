---
description: Tanto los escritores como los solicitantes mantienen la información necesaria para una operación de copia de seguridad o restauración en sus propios documentos de metadatos.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: Metadatos de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e718d3fb0290f8610944180c079e4d615124eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696463"
---
# <a name="vss-metadata"></a><span data-ttu-id="a1f32-103">Metadatos de VSS</span><span class="sxs-lookup"><span data-stu-id="a1f32-103">VSS Metadata</span></span>

<span data-ttu-id="a1f32-104">Tanto los escritores como los solicitantes mantienen la información necesaria para una operación de copia de seguridad o restauración en sus propios documentos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="a1f32-104">Both writers and requesters maintain information necessary to a backup or restore operation in their own metadata documents.</span></span>

<span data-ttu-id="a1f32-105">Estos documentos, el [*documento de metadatos de escritor*](vssgloss-w.md) y el [*documento de componentes de copia de seguridad*](vssgloss-b.md), respectivamente, se usan como base para la comunicación del escritor y el solicitante y la coordinación durante las actividades de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="a1f32-105">These documents, the [*Writer Metadata Document*](vssgloss-w.md) and the [*Backup Components Document*](vssgloss-b.md), respectively, are used as the basis for writer and requester communication and coordination during backup and restore activities.</span></span>

<span data-ttu-id="a1f32-106">Los metadatos se representan en formato XML con un esquema de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a1f32-106">The metadata is represented in XML format using a proprietary schema.</span></span> <span data-ttu-id="a1f32-107">Los metadatos se pueden copiar en disco, en cinta o en cualquier otro dispositivo de almacenamiento masivo.</span><span class="sxs-lookup"><span data-stu-id="a1f32-107">Metadata can be copied to disk, tape, or any other mass storage device.</span></span> <span data-ttu-id="a1f32-108">Siempre debe guardarse en el medio de copia de seguridad durante una operación de copia de seguridad y tendrá que recuperarse de ese medio en el transcurso de una operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="a1f32-108">It should always be saved to the backup media during a backup operation, and will need to be retrieved from that media in the course of a restore operation.</span></span>

<span data-ttu-id="a1f32-109">**PRECAUCIÓN:** Los detalles específicos del formato y del esquema son solo para uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="a1f32-109">**Caution:** The specific details of the format and schema are for system use only.</span></span> <span data-ttu-id="a1f32-110">Los desarrolladores no deben intentar modificar o usar directamente la representación XML de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="a1f32-110">Developers should not attempt to modify or directly use the XML representation of the metadata.</span></span>

<span data-ttu-id="a1f32-111">Los escritores y solicitantes se proporcionan con una variedad de métodos de consulta y de conjunto para obtener acceso y modificar los componentes de copia de seguridad y los documentos de metadatos del escritor:</span><span class="sxs-lookup"><span data-stu-id="a1f32-111">Writers and requesters are provided with a variety of query and set methods to access and modify the Backup Components and Writer Metadata documents:</span></span>

-   [<span data-ttu-id="a1f32-112">Trabajar con el documento de metadatos del escritor</span><span class="sxs-lookup"><span data-stu-id="a1f32-112">Working with the Writer Metadata Document</span></span>](working-with-the-writer-metadata-document.md)
-   [<span data-ttu-id="a1f32-113">Trabajar con el documento componentes de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="a1f32-113">Working with the Backup Components Document</span></span>](working-with-the-backup-components-document.md)
-   [<span data-ttu-id="a1f32-114">Componentes de metadatos de VSS</span><span class="sxs-lookup"><span data-stu-id="a1f32-114">VSS Metadata Components</span></span>](vss-metadata-components.md)

 

 



