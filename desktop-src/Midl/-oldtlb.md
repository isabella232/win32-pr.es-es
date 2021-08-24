---
title: Modificador /oldtlb
description: El modificador /oldtlb dirige al compilador MIDL para generar una biblioteca de tipos de formato antiguo.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- /oldtlb switch MIDL
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b30a7bc905645523a81287eea2dfcdc408b8a4d172cc84282e0f1538e12cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895995"
---
# <a name="oldtlb-switch"></a>Modificador /oldtlb

El **modificador /oldtlb** dirige al compilador MIDL para generar una biblioteca de tipos de formato antiguo.

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a>Opciones de cambio

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

El modificador **/oldtlb** invalida el valor predeterminado y dirige al compilador MIDL a generar bibliotecas de tipos de formato antiguo incluso en las versiones actuales de Windows mediante [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) en lugar de [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).

## <a name="examples"></a>Ejemplos

**midl /oldtlb filename.idl**

**midl /oldtlb myoldodl.odl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/newtlb**](-newtlb.md)
</dt> </dl>

 

 