---
title: Modificador /pack
description: El modificador /pack es el mismo que la opción /Zp.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- /pack switch MIDL
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159719"
---
# <a name="pack-switch"></a>Modificador /pack

El **modificador /pack** es el mismo que la [**opción /Zp.**](-zp.md)

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

*nivel de \_ empaquetado* 
</dt> <dd>

Especifica el nivel de empaquetado de las estructuras del sistema de destino. El valor de nivel de empaquetado se puede establecer en 1, 2, 4 u 8.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **modificador /pack** designa el nivel de empaquetado de las estructuras en el sistema de destino. El valor de nivel de empaquetado corresponde al valor de la opción [**/Zp**](-zp.md) utilizado por el compilador de Microsoft C/C++ versión 7.0. Para obtener más información, consulte la documentación de programación de Microsoft C/C++.

Especifique el mismo nivel de empaquetado al invocar el compilador MIDL y el compilador de C. El nivel de empaquetado predeterminado que se usa cuando no se especifica el modificador [**/Zp**](-zp.md) ni **/pack** es 8, en ambos entornos de compilación.

Para obtener una explicación de los posibles riesgos de usar niveles de empaquetado no estándar, consulte el tema de ayuda [**de /Zp.**](-zp.md)

## <a name="examples"></a>Ejemplos

**midl /pack 2 filename.idl**

**midl /pack 8 bar.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




