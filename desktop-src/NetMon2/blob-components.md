---
description: Componentes de BLOB
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Componentes de BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bd9ab8389cdd49a266855106891a91fcfbd0b4f69c7d22b5855143b34f376c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367487"
---
# <a name="blob-components"></a>Componentes de BLOB

Un objeto binario grande (BLOB) incluye los siguientes componentes jerárquicos:

-   Propietarios
-   Categorías
-   Etiquetas
-   Valores

## <a name="textual-representation"></a>Representación textual

Para mayor comodidad, los blobs aparecen en el formato Owner:Category:Tag:Value en el que aparecen cuando se guardan en un archivo. La estructura interna del BLOB es opaca porque representa punteros y tablas. Por ejemplo, esta es una entrada de un BLOB que se puede usar para configurar un NPP:

``` syntax
NPP:Configure:BufferSize=32768
```

El propietario es NPP. La categoría es Configurar, la etiqueta es BufferSize y el valor es 32768.

 

 



