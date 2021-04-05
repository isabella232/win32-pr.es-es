---
title: modificador/Pack
description: El modificador/Pack es el mismo que el de la opción/ZP.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- /Pack modificador MIDL
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076868"
---
# <a name="pack-switch"></a>modificador/Pack

El modificador **/Pack** es el mismo que el de la opción [**/ZP**](-zp.md) .

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*nivel de empaquetado \_* 
</dt> <dd>

Especifica el nivel de empaquetado de las estructuras en el sistema de destino. El valor de nivel de empaquetado se puede establecer en 1, 2, 4 u 8.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El modificador **/Pack** designa el nivel de empaquetado de las estructuras en el sistema de destino. El valor de nivel de empaquetado corresponde al valor de la opción [**/ZP**](-zp.md) usado por el compilador de Microsoft C/C++ versión 7,0. Para obtener más información, vea la documentación de programación de Microsoft C/C++.

Especifique el mismo nivel de empaquetado al invocar el compilador de MIDL y el compilador de C. El nivel de empaquetado predeterminado que se usa cuando no se especifica el modificador [**/ZP**](-zp.md) ni **/Pack** es 8, en todos los entornos de compilación.

Para obtener una explicación de los posibles peligros en el uso de niveles de empaquetado no estándar, vea el tema de ayuda de [**/ZP**](-zp.md) .

## <a name="examples"></a>Ejemplos

**MIDL/Pack 2 nombrearchivo. idl**

**MIDL/Pack 8 bar. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ENV**](-env.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




