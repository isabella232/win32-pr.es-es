---
title: Controladores (Guía de programación para Windows de 64 bits)
description: La versión de 64 bits de Windows está diseñada para que los desarrolladores puedan usar una única base de código fuente para las aplicaciones de 32 bits y 64 bits. En gran medida, esto también se aplica a los controladores de Windows de 32 y 64 bits.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- Controladores de 64 bits programación de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843a4efbb68652bf269c819c3a11ba102521318
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359640"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a><span data-ttu-id="6eb76-105">Controladores (Guía de programación para Windows de 64 bits)</span><span class="sxs-lookup"><span data-stu-id="6eb76-105">Drivers (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="6eb76-106">La versión de 64 bits de Windows está diseñada para que los desarrolladores puedan usar una única base de código fuente para las aplicaciones de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6eb76-106">The 64-bit version of Windows is designed to make it possible for developers to use a single source-code base for their 32-bit and 64-bit applications.</span></span> <span data-ttu-id="6eb76-107">En gran medida, esto también se aplica a los controladores de Windows de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6eb76-107">To a large extent, this is also true for 32-bit and 64-bit Windows drivers.</span></span>

<span data-ttu-id="6eb76-108">Sin embargo, los controladores de 32 bits no se pueden ejecutar en Windows de 64 bits y deben migrarse.</span><span class="sxs-lookup"><span data-stu-id="6eb76-108">However, 32-bit drivers cannot run on 64-bit Windows and must be ported.</span></span> <span data-ttu-id="6eb76-109">En el caso de las aplicaciones de modo de usuario, Windows de 64 bits incluye WOW64, que permite que las aplicaciones Windows de 32 bits se ejecuten (con cierta pérdida de rendimiento) en sistemas que ejecutan Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6eb76-109">For user-mode applications, 64-bit Windows includes WOW64, which enables 32-bit Windows applications to execute (with some loss of performance) on systems running 64-bit Windows.</span></span> <span data-ttu-id="6eb76-110">No existe ninguna capa de traducción equivalente para los controladores.</span><span class="sxs-lookup"><span data-stu-id="6eb76-110">No equivalent translation layer exists for drivers.</span></span>

<span data-ttu-id="6eb76-111">Para obtener información sobre cómo migrar controladores a Windows de 64 bits, consulte [problemas de 64](https://msdn.microsoft.com/library/aa489627.aspx) bits en el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="6eb76-111">For information about porting drivers to 64-bit Windows, see [64-Bit Issues](https://msdn.microsoft.com/library/aa489627.aspx) in the Windows Driver Kit (WDK).</span></span>

 

 




