---
title: _aulldiv rutina)
description: Divide dos enteros ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 2fce346ee9608f20667c76841a63a8a3fb9cfe21
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2020
ms.locfileid: "104487263"
---
# <a name="_aulldiv-routine"></a><span data-ttu-id="22d62-103">\_Rutina aulldiv</span><span class="sxs-lookup"><span data-stu-id="22d62-103">\_aulldiv Routine</span></span>

<span data-ttu-id="22d62-104">Divide dos enteros **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="22d62-104">Divides two **ULONGLONG** integers.</span></span>
<span data-ttu-id="22d62-105">Por ejemplo, para dividir dos valores UInt64, el compilador puede generar una llamada a la rutina **\_ aulldiv** .</span><span class="sxs-lookup"><span data-stu-id="22d62-105">For example, to divide two uint64 values the compiler might generate a call to the **\_aulldiv** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="22d62-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22d62-106">Remarks</span></span>

<span data-ttu-id="22d62-107">La rutina **\_ aulldiv** es una rutina auxiliar para el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="22d62-107">The **\_aulldiv** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="22d62-108">Si el compilador usa **\_ aulldiv** depende completamente del conjunto de optimización.</span><span class="sxs-lookup"><span data-stu-id="22d62-108">Whether the compiler uses **\_aulldiv** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="22d62-109">Esta función solo se usa en plataformas x86.</span><span class="sxs-lookup"><span data-stu-id="22d62-109">This function is used only on x86 platforms.</span></span>
