---
description: Las aplicaciones pueden usar de forma segura las características de administración de memoria de la biblioteca en tiempo de ejecución de C (malloc, free, etc.) y C++ (nuevo, eliminar, etc.).
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Funciones de la biblioteca estándar de C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303333b32f5645f19d8d22a072d25692cea4607f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666687"
---
# <a name="standard-c-library-functions"></a><span data-ttu-id="0bd5a-103">Funciones de la biblioteca estándar de C</span><span class="sxs-lookup"><span data-stu-id="0bd5a-103">Standard C Library Functions</span></span>

<span data-ttu-id="0bd5a-104">Las aplicaciones pueden usar de forma segura las características de administración de memoria de la biblioteca en tiempo de ejecución de C (**malloc**, **Free**, etc.) y C++ (**nuevo**, **eliminar**, etc.).</span><span class="sxs-lookup"><span data-stu-id="0bd5a-104">Applications can safely use the memory management features of the C run-time library (**malloc**, **free**, and so on) and C++ (**new**, **delete**, and so on).</span></span> <span data-ttu-id="0bd5a-105">Las funciones de la biblioteca en tiempo de ejecución de C no tienen los posibles problemas que tienen en Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-105">The C run-time library functions do not have the potential problems they have under 16-bit Windows.</span></span> <span data-ttu-id="0bd5a-106">La administración de memoria ya no es un problema porque el sistema es libre de administrar la memoria moviendo páginas de la memoria física sin afectar a las direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-106">Memory management is no longer a problem because the system is free to manage memory by moving pages of physical memory without affecting the virtual addresses.</span></span> <span data-ttu-id="0bd5a-107">Del mismo modo, la distinción entre punteros Near y Far ya no es relevante.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-107">Similarly, the distinction between near and far pointers is no longer relevant.</span></span> <span data-ttu-id="0bd5a-108">Por lo tanto, puede usar las funciones de la biblioteca estándar de C para la administración de memoria.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-108">Therefore, you can use the standard C library functions for memory management.</span></span> <span data-ttu-id="0bd5a-109">Sin embargo, las funciones de administración de memoria proporcionan funcionalidad que no está disponible en la biblioteca en tiempo de ejecución de C.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-109">However, the memory management functions do provide functionality that is unavailable in the C run-time library.</span></span>

 

 



