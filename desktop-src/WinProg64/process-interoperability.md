---
title: Interoperabilidad del proceso
description: Puede ejecutar aplicaciones basadas en Win32 en Windows de 64 bits con una capa de emulación. Windows 10 en ARM incluye una capa de emulación x86-on-ARM64. Para obtener más información, vea ejecutar aplicaciones de 32 bits.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- Programación de la interoperabilidad de Windows de 64 bits
- interoperabilidad de la programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023be0dafabfa8b17cf460542ae06467db517c11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704683"
---
# <a name="process-interoperability"></a><span data-ttu-id="7e665-107">Interoperabilidad del proceso</span><span class="sxs-lookup"><span data-stu-id="7e665-107">Process Interoperability</span></span>

<span data-ttu-id="7e665-108">Puede ejecutar aplicaciones basadas en Win32 en Windows de 64 bits con una capa de emulación.</span><span class="sxs-lookup"><span data-stu-id="7e665-108">You can run Win32-based applications on 64-bit Windows using an emulation layer.</span></span> <span data-ttu-id="7e665-109">Windows 10 en ARM incluye una capa de emulación x86-on-ARM64.</span><span class="sxs-lookup"><span data-stu-id="7e665-109">Windows 10 on ARM includes an x86-on-ARM64 emulation layer.</span></span> <span data-ttu-id="7e665-110">Para obtener más información, vea [ejecutar aplicaciones de 32 bits](running-32-bit-applications.md).</span><span class="sxs-lookup"><span data-stu-id="7e665-110">For more information, see [Running 32-bit Applications](running-32-bit-applications.md).</span></span>

<span data-ttu-id="7e665-111">En Windows de 64 bits, un proceso de 64 bits no puede cargar una biblioteca de vínculos dinámicos (DLL) de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7e665-111">On 64-bit Windows, a 64-bit process cannot load a 32-bit dynamic-link library (DLL).</span></span> <span data-ttu-id="7e665-112">Además, un proceso de 32 bits no puede cargar un archivo DLL de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7e665-112">Additionally, a 32-bit process cannot load a 64-bit DLL.</span></span> <span data-ttu-id="7e665-113">Sin embargo, Windows de 64 bits admite llamadas a procedimiento remoto (RPC) entre procesos de 64 bits y de 32 bits (tanto en el mismo equipo como en varios equipos).</span><span class="sxs-lookup"><span data-stu-id="7e665-113">However, 64-bit Windows supports remote procedure calls (RPC) between 64-bit and 32-bit processes (both on the same computer and across computers).</span></span> <span data-ttu-id="7e665-114">En Windows de 64 bits, un servidor COM fuera de proceso de 32 bits puede comunicarse con un cliente de 64 bits y un servidor COM de 64 bits fuera de proceso puede comunicarse con un cliente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7e665-114">On 64-bit Windows, an out-of-process 32-bit COM server can communicate with a 64-bit client, and an out-of-process 64-bit COM server can communicate with a 32-bit client.</span></span> <span data-ttu-id="7e665-115">Por lo tanto, si tiene una DLL de 32 bits que no es compatible con COM, puede encapsularla en un servidor COM fuera de proceso y utilizar COM para serializar las llamadas a y desde un proceso de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7e665-115">Therefore, if you have a 32-bit DLL that is not COM-aware, you can wrap it in an out-of-process COM server and use COM to marshal calls to and from a 64-bit process.</span></span>

<span data-ttu-id="7e665-116">Los servidores en proceso están registrados actualmente mediante la entrada del registro **InprocServer** .</span><span class="sxs-lookup"><span data-stu-id="7e665-116">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="7e665-117">En Windows de 64 bits, los servidores en proceso de 64 y 32 deben usar la entrada **InProcServer32** .</span><span class="sxs-lookup"><span data-stu-id="7e665-117">On 64-bit Windows, 64- and 32-bit in-process servers should use the **InprocServer32** entry.</span></span>

<span data-ttu-id="7e665-118">Para los identificadores de puerto, que por su naturaleza son locales para el equipo y que nunca se utilizarán en el límite de 32 bits a 64 bits, utilice el tipo **\_ ptr de identificador** en lugar del tipo de PTR **int \_** o **DWORD \_** .</span><span class="sxs-lookup"><span data-stu-id="7e665-118">To port handles, which by their nature are local to the computer and would never be used across the 32-bit to 64-bit boundary, use the **HANDLE\_PTR** type instead of the **INT\_PTR** or **DWORD\_PTR** type.</span></span> <span data-ttu-id="7e665-119">Esto incluye la migración de interfaces RPC que pasan tales identificadores como valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7e665-119">This includes porting RPC interfaces passing such handles as **DWORD** values.</span></span> <span data-ttu-id="7e665-120">El **identificador \_ PTR** de 64 bits es de 64 bits en la conexión (no truncado) y, por tanto, no necesita asignación.</span><span class="sxs-lookup"><span data-stu-id="7e665-120">The 64-bit **HANDLE\_PTR** is 64 bits on the wire (not truncated) and thus does not need mapping.</span></span> <span data-ttu-id="7e665-121">(El **\_ puntero de identificador** de 32 bits es de 32 bits en la conexión).</span><span class="sxs-lookup"><span data-stu-id="7e665-121">(The 32-bit **HANDLE\_PTR** is 32 bits on the wire.)</span></span>

<span data-ttu-id="7e665-122">Para obtener más información, vea [diseñar interfaces compatibles con 64 bits](designing-64-bit-compatible-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7e665-122">For more information, see [Designing 64-bit-Compatible Interfaces](designing-64-bit-compatible-interfaces.md).</span></span>

 

 




