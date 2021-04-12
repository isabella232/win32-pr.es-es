---
description: El modo de error indica al sistema cómo la aplicación va a responder a errores graves.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Modo de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75238e7ee64f40950c3df3aba36d28d95c953267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152734"
---
# <a name="error-mode"></a><span data-ttu-id="3f0ce-103">Modo de error</span><span class="sxs-lookup"><span data-stu-id="3f0ce-103">Error Mode</span></span>

<span data-ttu-id="3f0ce-104">El modo de error indica al sistema cómo la aplicación va a responder a errores graves.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-104">The error mode indicates to the system how the application is going to respond to serious errors.</span></span> <span data-ttu-id="3f0ce-105">Los errores graves incluyen el error de disco, los errores de unidad no preparada, la falta de alineación de los datos y las excepciones no controladas.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-105">Serious errors include disk failure, drive-not-ready errors, data misalignment, and unhandled exceptions.</span></span> <span data-ttu-id="3f0ce-106">Este modo de error se puede administrar por subproceso o por proceso.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-106">This error mode can be managed by either a per-thread or per-process basis.</span></span> <span data-ttu-id="3f0ce-107">Una aplicación puede permitir que el sistema muestre un cuadro de mensaje que informa al usuario de que se ha producido un error o puede controlar los errores.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-107">An application can let the system display a message box informing the user that an error has occurred, or it can handle the errors.</span></span>

<span data-ttu-id="3f0ce-108">Para controlar estos errores sin la intervención del usuario, use [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) o el [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)específico del subproceso.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-108">To handle these errors without user intervention, use [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) or the thread-specific [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode).</span></span> <span data-ttu-id="3f0ce-109">Después de llamar a una de estas funciones y especificar las marcas apropiadas, el sistema no mostrará los cuadros de mensaje de error correspondientes.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-109">After calling one of these functions and specifying appropriate flags, the system will not display the corresponding error message boxes.</span></span>

<span data-ttu-id="3f0ce-110">Un proceso puede recuperar su modo de error mediante [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) o [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).</span><span class="sxs-lookup"><span data-stu-id="3f0ce-110">A process can retrieve its error mode using [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) or [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).</span></span>

<span data-ttu-id="3f0ce-111">Se recomienda que todas las aplicaciones llamen a la función [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) de todo el proceso con un parámetro de **SEM \_ FAILCRITICALERRORS** en el inicio.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-111">Best practice is that all applications call the process-wide [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with a parameter of **SEM\_FAILCRITICALERRORS** at startup.</span></span> <span data-ttu-id="3f0ce-112">Esto es para evitar que los cuadros de diálogo del modo de error bloqueen la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-112">This is to prevent error mode dialogs from hanging the application.</span></span>

<span data-ttu-id="3f0ce-113">Aparte de eso, los autores de las llamadas deberían favorecer las versiones específicas del subproceso de estas funciones, ya que son menos perjudiciales para el comportamiento normal del sistema.</span><span class="sxs-lookup"><span data-stu-id="3f0ce-113">Other than that, callers should favor the thread-specific versions of these functions since they are less disruptive to the normal behavior of the system.</span></span>

 

 
