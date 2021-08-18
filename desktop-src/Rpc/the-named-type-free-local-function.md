---
title: La named_type_free_local función
description: Los códigos auxiliares llaman a la función local libre de tipos para liberar la memoria asignada por una llamada al tipo \_ con nombre a la rutina \_ \_ \_ \_ local.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123e0eb12a187ee6a5b7665ec126ba98153638e9d766015a0c9e7b1c7aec7dee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924085"
---
# <a name="the-named_type_free_local-function"></a>Función \_ local libre \_ de tipo con \_ nombre

Los códigos auxiliares llaman a **la \_ función \_ local** libre de tipos para liberar la memoria asignada por una llamada al tipo [con nombre a la rutina \_ \_ \_ local.](the-named-type-to-local-function.md) No libera la memoria asignada por el código auxiliar. El prototipo de función se define como:

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

El parámetro es un puntero a la memoria asignada por el **tipo con nombre al \_ \_ \_ local.**

 

 




