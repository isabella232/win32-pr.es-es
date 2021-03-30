---
description: La plantilla CMSPArray implementa una matriz inteligente que crecerá a petición.
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: CMSPArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002063"
---
# <a name="cmsparray"></a><span data-ttu-id="7b2ef-103">CMSPArray</span><span class="sxs-lookup"><span data-stu-id="7b2ef-103">CMSPArray</span></span>

<span data-ttu-id="7b2ef-104">La plantilla CMSPArray implementa una matriz inteligente que crecerá a petición.</span><span class="sxs-lookup"><span data-stu-id="7b2ef-104">The CMSPArray template implements a smart array that will grow on demand.</span></span> <span data-ttu-id="7b2ef-105">Está diseñado para contener matrices pequeñas con tipos de datos simples.</span><span class="sxs-lookup"><span data-stu-id="7b2ef-105">It is designed to hold small arrays with simple data types.</span></span> <span data-ttu-id="7b2ef-106">No tiene una sección crítica.</span><span class="sxs-lookup"><span data-stu-id="7b2ef-106">It doesn't have a critical section.</span></span> <span data-ttu-id="7b2ef-107">Sus únicas dependencias son **realloc** y **memmove**.</span><span class="sxs-lookup"><span data-stu-id="7b2ef-107">Its only dependencies are **realloc** and **memmove**.</span></span> <span data-ttu-id="7b2ef-108">Se utiliza internamente para mantener listas de punteros de objeto.</span><span class="sxs-lookup"><span data-stu-id="7b2ef-108">It is used internally to keep lists of object pointers.</span></span> <span data-ttu-id="7b2ef-109">Es similar a la implementación de **CSimpleArray** de ATL, pero es más eficaz para las asignaciones iniciales.</span><span class="sxs-lookup"><span data-stu-id="7b2ef-109">It is similar to ATL's **CSimpleArray** implementation, but it is more efficient for initial allocations.</span></span>

<span data-ttu-id="7b2ef-110">Esta plantilla se define en MSPutils. h.</span><span class="sxs-lookup"><span data-stu-id="7b2ef-110">This template is defined in MSPutils.h.</span></span>

 

 



