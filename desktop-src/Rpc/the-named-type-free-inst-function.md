---
title: La named_type_free_inst función
description: Los códigos auxiliares llaman a la función inst libre de \_ tipo con nombre para liberar memoria asociada al tipo \_ \_ transmitido.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa55e896b89fccc513795a62634e805c2ad6e21b7bdecdd99a0b9cfe2d71cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016895"
---
# <a name="the-named_type_free_inst-function"></a>El tipo \_ con \_ nombre free \_ inst (Función)

Los códigos auxiliares llaman a **la función \_ \_ \_ inst** libre de tipo con nombre para liberar memoria asociada al tipo transmitido. La función se define como:

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

El parámetro apunta a la instancia del tipo transmitido. Este objeto no debe liberarse. Para obtener una explicación sobre cuándo llamar a la función, vea [Representación \_ como atributo](the-represent-as-attribute.md).

 

 




