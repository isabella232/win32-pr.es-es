---
description: Bloque de entorno de subprocesos (notas de depuración)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Bloque de entorno de subprocesos (notas de depuración)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907237"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="0d542-103">Bloque de entorno de subprocesos (notas de depuración)</span><span class="sxs-lookup"><span data-stu-id="0d542-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="0d542-104">El bloque de entorno de subprocesos ([**estructura TEB**](/windows/win32/api/winternl/ns-winternl-teb)) contiene información de contexto para un subproceso.</span><span class="sxs-lookup"><span data-stu-id="0d542-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="0d542-105">En las siguientes versiones de Windows, el desplazamiento de la dirección TEB de 32 bits en el TEB de 64 bits es 0.</span><span class="sxs-lookup"><span data-stu-id="0d542-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="0d542-106">Se puede usar para tener acceso directamente al TEB de 32 bits de un subproceso de WOW64.</span><span class="sxs-lookup"><span data-stu-id="0d542-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="0d542-107">Esto podría cambiar en versiones posteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="0d542-107">This might change in later versions of Windows</span></span>



|               |                        |
|---------------|------------------------|
| <span data-ttu-id="0d542-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d542-108">Windows Vista</span></span> | <span data-ttu-id="0d542-109">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d542-109">Windows Server 2008</span></span>    |
| <span data-ttu-id="0d542-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d542-110">Windows 7</span></span>     | <span data-ttu-id="0d542-111">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0d542-111">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="0d542-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0d542-112">Windows 8</span></span>     | <span data-ttu-id="0d542-113">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d542-113">Windows Server 2012</span></span>    |
| <span data-ttu-id="0d542-114">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0d542-114">Windows 8.1</span></span>   | <span data-ttu-id="0d542-115">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0d542-115">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0d542-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d542-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d542-117">Estructuras de depuración</span><span class="sxs-lookup"><span data-stu-id="0d542-117">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="0d542-118">**Contexto de WOW64 \_**</span><span class="sxs-lookup"><span data-stu-id="0d542-118">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
