---
description: 'Se puede hacer referencia a los clústeres desde dos perspectivas diferentes: dentro del archivo y en el volumen.'
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Clústeres y extensiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687658"
---
# <a name="clusters-and-extents"></a><span data-ttu-id="81376-103">Clústeres y extensiones</span><span class="sxs-lookup"><span data-stu-id="81376-103">Clusters and Extents</span></span>

<span data-ttu-id="81376-104">Se puede hacer referencia a los clústeres desde dos perspectivas diferentes: dentro del archivo y en el volumen.</span><span class="sxs-lookup"><span data-stu-id="81376-104">Clusters may be referred to from two different perspectives: within the file and on the volume.</span></span> <span data-ttu-id="81376-105">Cualquier clúster de un archivo tiene un *número de clúster virtual* (VCN), que es su desplazamiento relativo desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="81376-105">Any cluster in a file has a *virtual cluster number* (VCN), which is its relative offset from the beginning of the file.</span></span> <span data-ttu-id="81376-106">Por ejemplo, una búsqueda de dos veces el tamaño de un clúster, seguido de una lectura, devolverá datos que comienzan en el tercer VCN.</span><span class="sxs-lookup"><span data-stu-id="81376-106">For example, a seek to twice the size of a cluster, followed by a read, will return data beginning at the third VCN.</span></span> <span data-ttu-id="81376-107">Un *número de clúster lógico* (LCN) describe el desplazamiento de un clúster desde algún punto arbitrario dentro del volumen.</span><span class="sxs-lookup"><span data-stu-id="81376-107">A *logical cluster number* (LCN) describes the offset of a cluster from some arbitrary point within the volume.</span></span> <span data-ttu-id="81376-108">LCNs solo se debe tratar como números ordinales o relativos.</span><span class="sxs-lookup"><span data-stu-id="81376-108">LCNs should be treated only as ordinal, or relative, numbers.</span></span> <span data-ttu-id="81376-109">No hay ninguna asignación garantizada de clústeres lógicos a los sectores de la unidad de disco duro física.</span><span class="sxs-lookup"><span data-stu-id="81376-109">There is no guaranteed mapping of logical clusters to physical hard disk drive sectors.</span></span>

<span data-ttu-id="81376-110">Una *extensión* es una ejecución de clústeres contiguos.</span><span class="sxs-lookup"><span data-stu-id="81376-110">An *extent* is a run of contiguous clusters.</span></span> <span data-ttu-id="81376-111">Por ejemplo, supongamos que un archivo que consta de 30 clústeres se registra en dos extensiones.</span><span class="sxs-lookup"><span data-stu-id="81376-111">For example, suppose a file consisting of 30 clusters is recorded in two extents.</span></span> <span data-ttu-id="81376-112">La primera extensión puede constar de cinco clústeres contiguos, el otro de los 25 clústeres restantes.</span><span class="sxs-lookup"><span data-stu-id="81376-112">The first extent might consist of five contiguous clusters, the other of the remaining 25 clusters.</span></span>

<span data-ttu-id="81376-113">No hay ninguna garantía de ninguna relación en el disco de cualquier extensión en cualquier otra extensión.</span><span class="sxs-lookup"><span data-stu-id="81376-113">There is no guarantee of any relationship on the disk of any extent to any other extent.</span></span> <span data-ttu-id="81376-114">Por ejemplo, la primera extensión puede estar en un LCN superior al de una extensión posterior.</span><span class="sxs-lookup"><span data-stu-id="81376-114">For example, the first extent may be at a higher LCN than a subsequent extent.</span></span>

 

 



