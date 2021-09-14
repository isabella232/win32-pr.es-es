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
ms.openlocfilehash: d4d6e54b963c9637c4f5a583fc9d8f44a0f2880e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159735"
---
# <a name="no_format_opt-switch"></a>Modificador /no \_ format \_ opt

El **modificador /no \_ format \_ opt** cambia la manera en que MIDL optimiza los descriptores de tipos y procedimientos.

``` syntax
midl /no_format_opt
```

## <a name="switch-options"></a>Opciones de cambio

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

De forma predeterminada, MIDL elimina los descriptores de tipo y procedimiento duplicados para reducir el tamaño del código auxiliar generado. El uso **del \_ modificador /no format \_ opt** desactiva este comportamiento de optimización.

## <a name="examples"></a>Ejemplos

**midl /no \_ format \_ opt mylean.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> </dl>

 

 




