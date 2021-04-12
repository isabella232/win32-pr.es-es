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
# <a name="wide-character-types"></a>Tipos de Wide-Character

Microsoft RPC admite el tipo de caracteres anchos [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t). El tipo de caracteres anchos usa 2 bytes para cada carácter. La definición del lenguaje C de ANSI permite inicializar caracteres largos y cadenas largas como:

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 