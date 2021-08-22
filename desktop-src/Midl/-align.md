---
title: Modificador /align
description: El modificador /align es funcionalmente el mismo que la opción MIDL /Zp y lo reconoce el compilador midl únicamente por compatibilidad con versiones anteriores con MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- /align switch MIDL
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187607b783678d3045224daec021eabf436fa8ba1884128789f44b06ac4365ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067655"
---
# <a name="align-switch"></a>Modificador /align

El **modificador /align** es funcionalmente el mismo que la opción MIDL [**/Zp**](-zp.md) y lo reconoce el compilador midl únicamente por compatibilidad con versiones anteriores con MkTypLib.

> [!Note]  
> La Mktyplib.exe está obsoleta. En su lugar, use el compilador MIDL.

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

*Alineación* 
</dt> <dd>

Especifica la alineación de los tipos de la biblioteca. El *valor* de alineación puede ser 1, 2, 4 u 8. El valor 1 indica la alineación natural; *n* indica la alineación en el byte *n*. Si no especifica el modificador **/align,** el valor predeterminado es 8.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si va a generar un nuevo archivo Make, use el [**modificador /Zp.**](-zp.md)

El valor de alineación corresponde al valor [**de la opción /Zp**](-zp.md) utilizado por el compilador de Microsoft C/C++. Asegúrese de especificar la misma alineación al invocar el compilador de C que al invocar el compilador MIDL.

Para más información, consulte la documentación de programación de Microsoft C/C++. Para obtener una explicación de los posibles riesgos de usar niveles de empaquetado no estándar, consulte el tema de ayuda [**de /Zp.**](-zp.md)

## <a name="examples"></a>Ejemplos

**midl /align:4 filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




