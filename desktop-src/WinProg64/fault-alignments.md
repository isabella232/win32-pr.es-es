---
title: Errores de alineación
description: Errores de alineación
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- errores de alineación 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a7a55010ac148354d000ece32c91a8652f821
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714429"
---
# <a name="alignment-faults"></a><span data-ttu-id="7405e-104">Errores de alineación</span><span class="sxs-lookup"><span data-stu-id="7405e-104">Alignment Faults</span></span>

<span data-ttu-id="7405e-105">El controlador de errores de alineación del sistema está desactivado de forma predeterminada en los sistemas basados en Itanium.</span><span class="sxs-lookup"><span data-stu-id="7405e-105">The system alignment-fault handler is turned off by default on Itanium-based systems.</span></span> <span data-ttu-id="7405e-106">Por lo tanto, cualquier acceso a datos no alineado genera una excepción que el sistema no solucionará automáticamente a menos que la aplicación detecte la excepción en un [controlador de excepciones basado en marcos](/windows/desktop/Debug/frame-based-exception-handling).</span><span class="sxs-lookup"><span data-stu-id="7405e-106">Therefore, any unaligned data access generates an exception that will not automatically be fixed by the system unless the application catches the exception in a [frame-based exception handler](/windows/desktop/Debug/frame-based-exception-handling).</span></span> <span data-ttu-id="7405e-107">Para habilitar el controlador de errores de alineación del sistema, llame a la función [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) con **SEM \_ NOALIGNMENTFAULTEXCEPT**.</span><span class="sxs-lookup"><span data-stu-id="7405e-107">To enable the system alignment-fault hander, call the [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with **SEM\_NOALIGNMENTFAULTEXCEPT**.</span></span> <span data-ttu-id="7405e-108">Sin embargo, tenga en cuenta que los procesos pueden experimentar una degradación grave del rendimiento si está habilitado el controlador de errores de alineación del sistema y el proceso genera errores de alineación.</span><span class="sxs-lookup"><span data-stu-id="7405e-108">However, note that processes may experience severe performance degradation if the system alignment-fault handler is enabled and the process generates alignment faults.</span></span>

<span data-ttu-id="7405e-109">Si el depurador WinDbg se ha instalado como el depurador del sistema, WinDbg se iniciará automáticamente si algún proceso del sistema genera una excepción no controlada.</span><span class="sxs-lookup"><span data-stu-id="7405e-109">If the WinDbg debugger has been installed as the system debugger, WinDbg will automatically be launched if any process on the system generates an unhandled exception.</span></span> <span data-ttu-id="7405e-110">Si no tiene un depurador instalado como depurador del sistema, el sistema muestra un cuadro de diálogo que indica que la aplicación ha encontrado un error y proporciona la oportunidad de notificar el problema a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7405e-110">If you do not have a debugger installed as your system debugger, the system displays a dialog box stating that your application has encountered an error and providing the opportunity to report the problem to Microsoft.</span></span>

<span data-ttu-id="7405e-111">En los sistemas x64 y ARM64, cualquier error de alineación se controla mediante una combinación de hardware y software.</span><span class="sxs-lookup"><span data-stu-id="7405e-111">On x64 and ARM64 systems, any alignment faults are handled by a combination of hardware and software.</span></span> <span data-ttu-id="7405e-112">Para obtener el mejor rendimiento, todo el acceso a la memoria debe estar correctamente alineado.</span><span class="sxs-lookup"><span data-stu-id="7405e-112">For best performance, all access to memory should be properly aligned.</span></span> <span data-ttu-id="7405e-113">Además, el [acceso a la variable entrelazada](/windows/desktop/Sync/interlocked-variable-access) no alineada debe evitarse en ARM64, ya que estas operaciones no son seguras para atomicidad.</span><span class="sxs-lookup"><span data-stu-id="7405e-113">In addition, unaligned [interlocked variable access](/windows/desktop/Sync/interlocked-variable-access) should be avoided on ARM64, as these operations are not atomic-safe.</span></span>

 

 