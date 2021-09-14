---
title: Wide-Character tipos
description: Microsoft RPC admite el tipo de caracteres anchos wchar \_ t.
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 821d69999a0ec7e175409120f223721defd6cd10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161030"
---
# <a name="wide-character-types"></a>Wide-Character tipos

Rpc de Microsoft admite el tipo de caracteres [**anchos wchar \_ t**](/windows/desktop/Midl/wchar-t). El tipo de caracteres anchos usa 2 bytes para cada carácter. La definición del lenguaje C ANSI permite inicializar caracteres largos y cadenas largas como:

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 