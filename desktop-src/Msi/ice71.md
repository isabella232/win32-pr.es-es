---
description: ICE71 comprueba que la tabla Media contiene una entrada con DiskId igual a 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c6e136362caa13da2b6305e3d8c3ca9c3a5c7bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074551"
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

 

 



