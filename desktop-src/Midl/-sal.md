---
title: Modificador /sal
description: El modificador /sal dirige a MIDL para generar anotaciones SAL en los archivos de código auxiliar generados.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- /sal switch MIDL
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80097cbfbb7bebae3b84b65c9c228dd29992821a5bafa61830961f752c452950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067495"
---
# <a name="sal-switch"></a>Modificador /sal

El **modificador /sal** dirige a MIDL para generar anotaciones SAL en los archivos de código auxiliar generados.

``` syntax
midl /sal
```

## <a name="switch-options"></a>Opciones de cambio

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

MIDL marcará los parámetros de puntero y matriz con anotaciones que reflejen la descripción del parámetro en el archivo IDL tal y como lo aplican RPC y el motor de serialización de MULTIDIMENSIONAL. MIDL no crea anotaciones para parámetros en los métodos de interfaz marcados con el atributo [**\[ local \]**](local.md)a menos que [**/sal \_ local**](-sal-local.md) también esté presente en la línea de comandos. Para invalidar la anotación generada por MIDL, use el [**\[ atributo annotate. \]**](annotate.md)

Las anotaciones generadas por MIDL siempre tienen el prefijo RPC y requieren el uso del encabezado \_ \_ \_ **rpcsal.h** para traducir la anotación en anotaciones SAL estándar.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal \_ local**](-sal-local.md)
</dt> <dt>

[**\[Anotar\]**](annotate.md)
</dt> </dl>

 

 




