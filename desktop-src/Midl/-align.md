---
title: modificador/align
description: El modificador/Align es funcionalmente igual que la opción/ZP de MIDL y el compilador MIDL lo reconoce únicamente para mantener la compatibilidad con MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- modificador/align MIDL
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532721"
---
# <a name="align-switch"></a>modificador/align

El modificador **/align** es funcionalmente igual que la opción [**/ZP**](-zp.md) de MIDL y el compilador MIDL lo reconoce únicamente para mantener la compatibilidad con MkTypLib.

> [!Note]  
> La herramienta Mktyplib.exe está obsoleta. En su lugar, utilice el compilador de MIDL.

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*ecuación* 
</dt> <dd>

Especifica la alineación de los tipos de la biblioteca. El valor de *alineación* puede ser 1, 2, 4 u 8. El valor 1 indica la alineación natural; *n* indica la alineación en byte *n*. Cuando no se especifica el modificador **/align** , el valor predeterminado es 8.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si va a generar un nuevo archivo make, use el modificador [**/ZP**](-zp.md) .

El valor de alineación corresponde al valor de la opción [**/ZP**](-zp.md) usado por el compilador de C/C++ de Microsoft. Asegúrese de especificar la misma alineación al invocar al compilador de C como cuando se invoca el compilador de MIDL.

Para obtener más información, vea la documentación de programación de Microsoft C/C++. Para obtener una explicación de los posibles peligros en el uso de niveles de empaquetado no estándar, vea el tema de ayuda de [**/ZP**](-zp.md) .

## <a name="examples"></a>Ejemplos

**MIDL/align: 4 FILENAME. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




