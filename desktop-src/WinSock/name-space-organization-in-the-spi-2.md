---
description: Organización del espacio de nombres en el SPI de Windows Sockets (Winsock).
ms.assetid: c369a476-23e4-48a1-912b-2d876deb0b88
title: Organización del espacio de nombres en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a572ad86299f0bf5ba3e7f95662e1616da520608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648188"
---
# <a name="namespace-organization-in-the-spi"></a><span data-ttu-id="a9a5c-103">Organización del espacio de nombres en el SPI</span><span class="sxs-lookup"><span data-stu-id="a9a5c-103">Namespace Organization in the SPI</span></span>

<span data-ttu-id="a9a5c-104">Muchos espacios de nombres se organizan jerárquicamente.</span><span class="sxs-lookup"><span data-stu-id="a9a5c-104">Many namespaces are arranged hierarchically.</span></span> <span data-ttu-id="a9a5c-105">Algunos, como X. 500 y NDS, permiten un anidamiento ilimitado.</span><span class="sxs-lookup"><span data-stu-id="a9a5c-105">Some, such as X.500 and NDS, allow unlimited nesting.</span></span> <span data-ttu-id="a9a5c-106">Otros permiten que los servicios se combinen en un solo nivel de jerarquía o grupo.</span><span class="sxs-lookup"><span data-stu-id="a9a5c-106">Others allow services to be combined into a single level of hierarchy or group.</span></span> <span data-ttu-id="a9a5c-107">Esto se conoce normalmente como grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a9a5c-107">This is typically referred to as a workgroup.</span></span> <span data-ttu-id="a9a5c-108">Al construir una consulta, a menudo es necesario establecer un punto de contexto dentro de una jerarquía de espacios de nombres desde la que comenzará la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a9a5c-108">When constructing a query, it is often necessary to establish a context point within a namespace hierarchy from which the search will begin.</span></span>

 

 



