---
description: Bloque de entorno de subproceso (notas de depuración)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Bloque de entorno de subproceso (notas de depuración)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9397c2d442b09b308c4886c2672e3be58b661c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550590"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="a1e8c-103">Bloque de entorno de subproceso (notas de depuración)</span><span class="sxs-lookup"><span data-stu-id="a1e8c-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="a1e8c-104">El bloque de entorno de subproceso [**(estructura TEB)**](/windows/win32/api/winternl/ns-winternl-teb)contiene información de contexto para un subproceso.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="a1e8c-105">En las siguientes versiones de Windows, el desplazamiento de la dirección TEB de 32 bits dentro del TEB de 64 bits es 0.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="a1e8c-106">Se puede usar para acceder directamente al TEB de 32 bits de un subproceso WOW64.</span><span class="sxs-lookup"><span data-stu-id="a1e8c-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="a1e8c-107">Esto podría cambiar en versiones posteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="a1e8c-107">This might change in later versions of Windows</span></span>



|  <span data-ttu-id="a1e8c-108">Plataforma</span><span class="sxs-lookup"><span data-stu-id="a1e8c-108">Platform</span></span>     | <span data-ttu-id="a1e8c-109">Versión</span><span class="sxs-lookup"><span data-stu-id="a1e8c-109">Version</span></span>                |
|---------------|------------------------|
| <span data-ttu-id="a1e8c-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1e8c-110">Windows Vista</span></span> | <span data-ttu-id="a1e8c-111">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1e8c-111">Windows Server 2008</span></span>    |
| <span data-ttu-id="a1e8c-112">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a1e8c-112">Windows 7</span></span>     | <span data-ttu-id="a1e8c-113">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1e8c-113">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="a1e8c-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a1e8c-114">Windows 8</span></span>     | <span data-ttu-id="a1e8c-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1e8c-115">Windows Server 2012</span></span>    |
| <span data-ttu-id="a1e8c-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a1e8c-116">Windows 8.1</span></span>   | <span data-ttu-id="a1e8c-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a1e8c-117">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a1e8c-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1e8c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1e8c-119">Estructuras de depuración</span><span class="sxs-lookup"><span data-stu-id="a1e8c-119">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="a1e8c-120">**CONTEXTO DE \_ WOW64**</span><span class="sxs-lookup"><span data-stu-id="a1e8c-120">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
