---
title: Modificador /no_format_opt
description: El modificador /no \_ format opt cambia la manera en que \_ MIDL optimiza los descriptores de tipos y procedimientos.
ms.assetid: 721ac828-7b47-4991-8bce-f9babf6c77a8
keywords:
- /no_format_opt switch MIDL
topic_type:
- apiref
api_name:
- /no_format_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93753d1aa73d378ff093cf2d315e144461f466a42910e1778060be05defb911a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014143"
---
# <a name="no_format_opt-switch"></a>Modificador /no \_ format \_ opt

El **modificador /no \_ format \_ opt** cambia la manera en que MIDL optimiza los descriptores de tipos y procedimientos.

``` syntax
midl /no_format_opt
```

## <a name="switch-options"></a>Opciones de cambio

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

De forma predeterminada, MIDL elimina los descriptores de tipo y procedimiento duplicados para reducir el tamaño del código auxiliar generado. El uso **del modificador /no \_ format \_ opt** desactiva este comportamiento de optimización.

## <a name="examples"></a>Ejemplos

**midl /no \_ format \_ opt mylean.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> </dl>

 

 




