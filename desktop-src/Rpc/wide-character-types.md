---
title: Tipos de Wide-Character
description: Microsoft RPC admite el tipo de caracteres anchos WCHAR \_ t.
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 821d69999a0ec7e175409120f223721defd6cd10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149468"
---
# <a name="wide-character-types"></a><span data-ttu-id="40fee-103">Tipos de Wide-Character</span><span class="sxs-lookup"><span data-stu-id="40fee-103">Wide-Character Types</span></span>

<span data-ttu-id="40fee-104">Microsoft RPC admite el tipo de caracteres anchos [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t).</span><span class="sxs-lookup"><span data-stu-id="40fee-104">Microsoft RPC supports the wide-character type [**wchar\_t**](/windows/desktop/Midl/wchar-t).</span></span> <span data-ttu-id="40fee-105">El tipo de caracteres anchos usa 2 bytes para cada carácter.</span><span class="sxs-lookup"><span data-stu-id="40fee-105">The wide-character type uses 2 bytes for each character.</span></span> <span data-ttu-id="40fee-106">La definición del lenguaje C de ANSI permite inicializar caracteres largos y cadenas largas como:</span><span class="sxs-lookup"><span data-stu-id="40fee-106">The ANSI C-language definition allows you to initialize long characters and long strings as:</span></span>

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 