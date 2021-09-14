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
ms.openlocfilehash: 84e8fd972355c2f6d37300c60f4bf74e76bf4396
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159741"
---
# <a name="mktyplib203-switch"></a>Modificador /mktyplib203

El **modificador /mktyplib203** fuerza al compilador MIDL a analizar el archivo de entrada.

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Para usar el modificador **/mktyplib203,** el archivo de entrada debe seguir exactamente la sintaxis de ODL, lo que significa que no se puede colocar ninguna instrucción fuera del bloque de biblioteca. Ejemplos

**midl /mktyplib203 myoldodl.odl**

**midl /mktyplib203 oldhabit.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




