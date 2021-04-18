---
description: El IMM incluye la comprobación de identificación de subprocesos que determina si un subproceso que realiza la llamada es el creador de un identificador de contexto de método de entrada especificado (tipo HIMC) o un identificador de ventana (tipo HWND).
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Desarrollar IME-Aware aplicaciones de varios subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5730fc72ef41a84e01655116f94fc274f60548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688350"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a><span data-ttu-id="6d48d-103">Desarrollar IME-Aware aplicaciones de varios subprocesos</span><span class="sxs-lookup"><span data-stu-id="6d48d-103">Developing IME-Aware Multiple-thread Applications</span></span>

<span data-ttu-id="6d48d-104">El IMM incluye la comprobación de identificación de subprocesos que determina si un subproceso que realiza la llamada es el creador de un identificador de contexto de método de entrada especificado (tipo HIMC) o un identificador de ventana (tipo HWND).</span><span class="sxs-lookup"><span data-stu-id="6d48d-104">The IMM includes thread identification checking that determines if a calling thread is the creator of a specified input method context handle (HIMC type) or window handle (HWND type).</span></span> <span data-ttu-id="6d48d-105">Si el subproceso no es el creador del identificador, se produce un error en la función denominada IMM y una llamada subsiguiente a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de \_ acceso no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="6d48d-105">If the thread is not the creator of the handle, the called IMM function fails and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_ACCESS.</span></span>

> [!Note]  
> <span data-ttu-id="6d48d-106">La arquitectura de IMM actual no proporciona una utilidad de sincronización para el acceso a los identificadores de IMM.</span><span class="sxs-lookup"><span data-stu-id="6d48d-106">The current IMM architecture does not provide a synchronization facility for access to IMM handles.</span></span>

 

<span data-ttu-id="6d48d-107">Para usar la comprobación de identificación de subprocesos, las aplicaciones deben cumplir las siguientes directrices:</span><span class="sxs-lookup"><span data-stu-id="6d48d-107">To use thread identification checking, your applications must adhere to the following guidelines:</span></span>

-   <span data-ttu-id="6d48d-108">Un subproceso no debe tener acceso al contexto de entrada creado por otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="6d48d-108">A thread should not access the input context created by another thread.</span></span>
-   <span data-ttu-id="6d48d-109">Un subproceso no debe asociar un contexto de entrada a una ventana creada por otro subproceso, y viceversa.</span><span class="sxs-lookup"><span data-stu-id="6d48d-109">A thread should not associate an input context with a window created by another thread, and vice versa.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d48d-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d48d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d48d-111">Usar el administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="6d48d-111">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
