---
title: Árbol de nombres de MIB
description: El espacio de nombres para los identificadores de objeto MIB es jerárquico. Está estructurado de modo que cada objeto administrable puede tener asignado un nombre único global.
ms.assetid: eb3c855c-b36b-4675-8df4-e11c128b2b34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d77b0cb4c64d9645f54ec7416c45ba1a4620ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076050"
---
# <a name="mib-name-tree"></a><span data-ttu-id="4241c-104">Árbol de nombres de MIB</span><span class="sxs-lookup"><span data-stu-id="4241c-104">MIB Name Tree</span></span>

<span data-ttu-id="4241c-105">El espacio de nombres para los identificadores de objeto MIB es jerárquico.</span><span class="sxs-lookup"><span data-stu-id="4241c-105">The name space for MIB object identifiers is hierarchical.</span></span> <span data-ttu-id="4241c-106">Está estructurado de modo que cada objeto administrable puede tener asignado un nombre único global.</span><span class="sxs-lookup"><span data-stu-id="4241c-106">It is structured so that each manageable object can be assigned a globally unique name.</span></span>

<span data-ttu-id="4241c-107">La autoridad de partes del espacio de nombres se asigna a organizaciones individuales.</span><span class="sxs-lookup"><span data-stu-id="4241c-107">Authority for parts of the name space is assigned to individual organizations.</span></span> <span data-ttu-id="4241c-108">Esto permite a las organizaciones asignar nombres sin consultar una autoridad de Internet para cada asignación.</span><span class="sxs-lookup"><span data-stu-id="4241c-108">This allows organizations to assign names without consulting an Internet authority for each assignment.</span></span> <span data-ttu-id="4241c-109">Por ejemplo, el espacio de nombres asignado a Microsoft es 1.3.6.1.4.1.311, que se define en MSFT. MIB.</span><span class="sxs-lookup"><span data-stu-id="4241c-109">For example, the name space assigned to Microsoft is 1.3.6.1.4.1.311, which is defined in MSFT.MIB.</span></span> <span data-ttu-id="4241c-110">Microsoft tiene la autoridad para asignar nombres a objetos en cualquier lugar debajo de ese espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="4241c-110">Microsoft has the authority to assign names to objects anywhere below that name space.</span></span>

<span data-ttu-id="4241c-111">El identificador de objeto de la jerarquía se escribe como una secuencia de subidentificadors que comienzan en la raíz y terminan en el objeto.</span><span class="sxs-lookup"><span data-stu-id="4241c-111">The object identifier in the hierarchy is written as a sequence of subidentifiers beginning at the root and ending at the object.</span></span> <span data-ttu-id="4241c-112">Los subidentificadors se separan con un punto.</span><span class="sxs-lookup"><span data-stu-id="4241c-112">Subidentifiers are separated with a period.</span></span>

 

 




