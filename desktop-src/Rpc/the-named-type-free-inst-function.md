---
title: La función named_type_free_inst
description: El código auxiliar llama a \_ la \_ función inst Free de tipo con nombre \_ para liberar memoria asociada al tipo transmitido.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d3b5103572eb58e4311c65b0e1cff02e91f66f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774628"
---
# <a name="the-named_type_free_inst-function"></a>\_ \_ Función inst Free de tipo con nombre \_

El código auxiliar llama a la función **\_ \_ \_ inst Free de tipo con nombre** para liberar memoria asociada al tipo transmitido. La función se define como:

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

El parámetro apunta a la instancia del tipo transmitido. Este objeto no se debe liberar. Para obtener una explicación sobre cuándo llamar a la función, vea [el \_ atributo representated as](the-represent-as-attribute.md).

 

 




