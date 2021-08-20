---
description: ICE71 comprueba que la tabla Media contiene una entrada con DiskId igual a 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1090eb8b1a36ed361ef763bfda3875a8fde052ed8643dceeb660c88ae954a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142519"
---
# <a name="ice71"></a>ICE71

ICE71 comprueba que la [tabla Media contiene](media-table.md) una entrada con DiskId igual a 1. (Windows instalador da por supuesto que el paquete .msi está en el disco 1).

## <a name="result"></a>Resultado

ICE71 devuelve un error si la tabla Media no contiene una entrada con DiskId igual a 1.

## <a name="example"></a>Ejemplo

ICE71 notifica el siguiente error para el ejemplo mostrado.

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

T0 corrija este error y cambie el valor de DiskId de la entrada donde se almacena el paquete a 1.

[Tabla multimedia](media-table.md) (parcial)



| DiskId |
|--------|
| 2      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



