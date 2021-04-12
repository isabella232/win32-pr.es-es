---
description: Componentes de BLOB
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Componentes de BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277980"
---
# <a name="blob-components"></a>Componentes de BLOB

Un objeto binario grande (BLOB) incluye los siguientes componentes jerárquicos:

-   Propietarios
-   Categorías
-   Etiquetas
-   Valores

## <a name="textual-representation"></a>Representación textual

Para mayor comodidad, los blobs aparecen en el formato propietario: Categoría: etiqueta: valor en el que aparecen cuando se guardan en un archivo. La estructura interna del BLOB es opaca porque representa punteros y tablas. Por ejemplo, esta es una entrada de un BLOB que se puede usar para configurar un NPP:

``` syntax
NPP:Configure:BufferSize=32768
```

El propietario es NPP. La categoría es configure, la etiqueta es BufferSize y el valor es 32768.

 

 



