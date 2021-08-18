---
title: Modificador /notlb
description: El modificador /notlb impide que el compilador MIDL genere un archivo de biblioteca de tipos (TLB).
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- /notlb switch MIDL
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e309ed753d1549c31c9e3dea0a5c7aa87b32217aa12e5ee04934a183927adf87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067525"
---
# <a name="notlb-switch"></a>Modificador /notlb

El **modificador /notlb** impide que el compilador MIDL genere un archivo de biblioteca de tipos (TLB).

``` syntax
midl /notlb
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

De forma predeterminada, el compilador midl generará un archivo TLB cada vez que encuentre una [**instrucción LIBRARY.**](library.md) Este modificador invalida el comportamiento predeterminado.

Cuando se **especifica la opción /notlb,** todos los demás códigos auxiliares, encabezados, etc. se generan como de costumbre.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/tlb**](-tlb.md)
</dt> </dl>

 

 




