---
title: Wide-Character de datos
description: Rpc de Microsoft admite el tipo de carácter ancho wchar \_ t.
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eff57cf22e4836032acb59e1585da15285f55718b6c5b91733b1955ea85072a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010403"
---
# <a name="wide-character-types"></a>Wide-Character de datos

Rpc de Microsoft admite el tipo de caracteres [**anchos wchar \_ t**](/windows/desktop/Midl/wchar-t). El tipo de caracteres anchos usa 2 bytes para cada carácter. La definición del lenguaje C ANSI permite inicializar caracteres largos y cadenas largas como:

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 