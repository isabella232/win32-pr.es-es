---
title: Modificador /mktyplib203
description: El modificador /mktyplib203 fuerza al compilador MIDL a analizar el archivo de entrada.
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- /mktyplib203 switch MIDL
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc887560401986b9a7d5e0f0aa7c8b36d61874bf245a88ade7a149cd084f1ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014153"
---
# <a name="mktyplib203-switch"></a>Modificador /mktyplib203

El **modificador /mktyplib203** fuerza al compilador MIDL a analizar el archivo de entrada.

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

Para usar el modificador **/mktyplib203,** el archivo de entrada debe seguir exactamente la sintaxis de ODL, lo que significa que no se puede colocar ninguna instrucción fuera del bloque de biblioteca. Ejemplos

**midl /mktyplib203 myoldodl.odl**

**midl /mktyplib203 oldhabit.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




