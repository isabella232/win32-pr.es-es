---
title: _allmul rutina)
description: Multiplica dos enteros de LONGLONG o ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2020
ms.locfileid: "104077229"
---
# <a name="_allmul-routine"></a><span data-ttu-id="9197b-103">\_Rutina allmul</span><span class="sxs-lookup"><span data-stu-id="9197b-103">\_allmul Routine</span></span>

<span data-ttu-id="9197b-104">Multiplica dos enteros de **LONGLONG** o **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="9197b-104">Multiplies two **LONGLONG** or **ULONGLONG** integers.</span></span>
<span data-ttu-id="9197b-105">Por ejemplo, para multiplicar dos valores Int64, el compilador puede generar una llamada a la rutina **\_ allmul** .</span><span class="sxs-lookup"><span data-stu-id="9197b-105">For example, to multiply two int64 values the compiler might generate a call to the **\_allmul** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="9197b-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9197b-106">Remarks</span></span>

<span data-ttu-id="9197b-107">La rutina **\_ allmul** es una rutina auxiliar para el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="9197b-107">The **\_allmul** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="9197b-108">Si el compilador usa **\_ allmul** depende completamente del conjunto de optimización.</span><span class="sxs-lookup"><span data-stu-id="9197b-108">Whether the compiler uses **\_allmul** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="9197b-109">Esta rutina solo se usa en plataformas x86.</span><span class="sxs-lookup"><span data-stu-id="9197b-109">This routine is used only on x86 platforms.</span></span>
