---
description: ICE71 comprueba que la tabla de medios contiene una entrada con el valor de dipatine igual a 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c6e136362caa13da2b6305e3d8c3ca9c3a5c7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002696"
---
# <a name="ice71"></a>ICE71

ICE71 comprueba que la [tabla de medios](media-table.md) contiene una entrada con el valor de dipatine igual a 1. (Windows Installer supone que el paquete. msi se encuentra en el disco 1).

## <a name="result"></a>Resultado

ICE71 devuelve un error si la tabla de medios no contiene una entrada con el valor de dipatine igual a 1.

## <a name="example"></a>Ejemplo

ICE71 notifica el siguiente error para el ejemplo que se muestra.

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

T0 corrija este error, cambie el valor de la entrada en la que se almacena el paquete a 1.

[Tabla de medios](media-table.md) (parcial)



| Detectaron |
|--------|
| 2      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



