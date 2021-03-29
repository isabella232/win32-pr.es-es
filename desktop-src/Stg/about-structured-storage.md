---
title: Acerca del almacenamiento estructurado
description: Los sistemas de archivos tradicionales tienen problemas cuando intentan almacenar de forma eficaz varios tipos de objetos en un documento.
ms.assetid: a571f7c2-0490-463c-813e-de4a9fd12a2d
keywords:
- Acerca del almacenamiento estructurado
- STG de almacenamiento estructurado Strctd, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d048907c196c871af943e5a15cc95b367724a31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774616"
---
# <a name="about-structured-storage"></a><span data-ttu-id="e9c42-105">Acerca del almacenamiento estructurado</span><span class="sxs-lookup"><span data-stu-id="e9c42-105">About Structured Storage</span></span>

<span data-ttu-id="e9c42-106">Los sistemas de archivos tradicionales tienen problemas cuando intentan almacenar de forma eficaz varios tipos de objetos en un documento.</span><span class="sxs-lookup"><span data-stu-id="e9c42-106">Traditional file systems encounter challenges when they attempt to store efficiently multiple kinds of objects in one document.</span></span> <span data-ttu-id="e9c42-107">COM proporciona una solución: un sistema de archivos dentro de un archivo.</span><span class="sxs-lookup"><span data-stu-id="e9c42-107">COM provides a solution: a file system within a file.</span></span> <span data-ttu-id="e9c42-108">El almacenamiento estructurado COM define cómo tratar una entidad de un solo archivo como una colección estructurada de dos tipos de objetos (almacenamientos y secuencias) que funcionan como archivos y directorios.</span><span class="sxs-lookup"><span data-stu-id="e9c42-108">COM structured storage defines how to treat a single file entity as a structured collection of two types of objects—storages and streams—that perform like directories and files.</span></span> <span data-ttu-id="e9c42-109">Este esquema se denomina *almacenamiento estructurado*.</span><span class="sxs-lookup"><span data-stu-id="e9c42-109">This scheme is called *structured storage*.</span></span> <span data-ttu-id="e9c42-110">El propósito del almacenamiento estructurado es reducir las penalizaciones de rendimiento y la sobrecarga asociada al almacenamiento de objetos independientes en un archivo plano.</span><span class="sxs-lookup"><span data-stu-id="e9c42-110">The purpose of structured storage is to reduce the performance penalties and overhead associated with storing separate objects in a flat file.</span></span>

<span data-ttu-id="e9c42-111">Esta sección contiene información general sobre las ventajas y los aspectos básicos del almacenamiento estructurado, los conjuntos de propiedades y el almacenamiento estructurado asincrónico, así como una visión histórica de los sistemas de archivos:</span><span class="sxs-lookup"><span data-stu-id="e9c42-111">This section contains an overview of structured storage benefits and fundamentals, property sets and asynchronous structured storage as well as a historical look at file systems:</span></span>

-   <span data-ttu-id="e9c42-112">Implementación de archivos compuestos</span><span class="sxs-lookup"><span data-stu-id="e9c42-112">Compound file implementation</span></span>
-   <span data-ttu-id="e9c42-113">Implementación del sistema de archivos NTFS</span><span class="sxs-lookup"><span data-stu-id="e9c42-113">NTFS file system implementation</span></span>
-   <span data-ttu-id="e9c42-114">Implementación independiente</span><span class="sxs-lookup"><span data-stu-id="e9c42-114">Stand-alone implementation</span></span>

<span data-ttu-id="e9c42-115">En esta sección se incluyen vínculos a [la evolución de los sistemas de archivos](the-evolution-of-file-systems.md), los [almacenamientos y las secuencias](storages-and-streams.md), [los archivos compuestos, los](compound-files.md) [aspectos básicos de almacenamiento estructurado](structured-storage-fundamentals.md)y los [ejemplos de almacenamiento estructurado](using-structured-storage.md).</span><span class="sxs-lookup"><span data-stu-id="e9c42-115">This section includes links to [The Evolution of File Systems](the-evolution-of-file-systems.md), [Storages and Streams](storages-and-streams.md), [Compound Files](compound-files.md), [Structured Storage Fundamentals](structured-storage-fundamentals.md), and [Structured Storage Samples](using-structured-storage.md).</span></span>

 

 




