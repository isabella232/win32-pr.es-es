---
title: Macros predefinidas
description: RC no admite las macros predefinidas de ANSI C \_ \_ \_ \_ (DATE, \_ \_ \_ \_ FILE, \_ \_ \_ \_ LINE, \_ \_ \_ \_ STDC, \_ \_ \_ \_ TIME, \_ \_ TIMESTAMP \_ \_ ). Por lo tanto, no puede incluir estas macros en los archivos de encabezado que incluirá en el script de recursos.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9e48b915fae430bf776b9eebab7ac795e7b69a3d79e06a7ce6422b6d6eab6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971954"
---
# <a name="predefined-macros"></a>Macros predefinidas

RC no admite las macros predefinidas de ANSI C **\_ \_ (DATE, \_ \_** **\_ \_ FILE, \_ \_** **\_ \_ LINE, \_ \_** **\_ \_ STDC, \_ \_** **\_ \_ TIME, \_ \_** **\_ \_ TIMESTAMP \_ \_**). Por lo tanto, no puede incluir estas macros en los archivos de encabezado que incluirá en el script de recursos.

RC define RC INVOKED, que permite compilar condicionalmente partes de los archivos de encabezado, en función de si el compilador es el compilador de C o \_ el compilador rc. Esto es importante porque el compilador RC solo admite un subconjunto de las instrucciones que admitiría un compilador de C.

Para compilar condicionalmente el código con el compilador RC, envuelve el código que RC no puede compilar con \# ifndef RC \_ INVOKED y **\# endif**.

El ejemplo siguiente se toma de los ejemplos del SDK. Muestra cómo crear un archivo de encabezado que se puede compilar condicionalmente.

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




