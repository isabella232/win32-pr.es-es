---
title: modificador/notlb
description: El modificador/notlb evita que el compilador de MIDL genere un archivo de biblioteca de tipos (TLB).
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- /notlb modificador MIDL
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487146"
---
# <a name="notlb-switch"></a>modificador/notlb

El modificador **/notlb** evita que el compilador de MIDL genere un archivo de biblioteca de tipos (TLB).

``` syntax
midl /notlb
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

De forma predeterminada, el compilador MIDL generará un archivo TLB siempre que encuentre una instrucción [**Library**](library.md) . Este modificador invalida el comportamiento predeterminado.

Cuando se especifica la opción **/notlb** , todos los demás códigos auxiliares, encabezados, etc. se generan como de costumbre.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/TLB**](-tlb.md)
</dt> </dl>

 

 




