---
description: Lo llama el compilador cuando hay más de una página de variables locales en la función.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: _chkstk rutina)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a58b31836947dfb1816bea72a54f820354c792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998051"
---
# <a name="_chkstk-routine"></a><span data-ttu-id="46f81-103">\_Rutina chkstk</span><span class="sxs-lookup"><span data-stu-id="46f81-103">\_chkstk Routine</span></span>

<span data-ttu-id="46f81-104">Lo llama el compilador cuando hay más de una página de variables locales en la función.</span><span class="sxs-lookup"><span data-stu-id="46f81-104">Called by the compiler when you have more than one page of local variables in your function.</span></span>

## <a name="remarks"></a><span data-ttu-id="46f81-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46f81-105">Remarks</span></span>

<span data-ttu-id="46f81-106">\_chkstk rutina es una rutina auxiliar para el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="46f81-106">\_chkstk Routine is a helper routine for the C compiler.</span></span> <span data-ttu-id="46f81-107">En el caso de los compiladores x86, \_ se llama a la rutina chkstk cuando las variables locales superan los 4.000 bytes; para los compiladores x64, es de 8 KB.</span><span class="sxs-lookup"><span data-stu-id="46f81-107">For x86 compilers, \_chkstk Routine is called when the local variables exceed 4K bytes; for x64 compilers it is 8K.</span></span>

 

 



