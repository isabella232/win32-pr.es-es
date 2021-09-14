---
title: /align switch
description: El modificador /align es funcionalmente el mismo que la opción MIDL /Zp y lo reconoce el compilador de MIDL únicamente por compatibilidad con versiones anteriores con MkTypLib.
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
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159778"
---
# <a name="align-switch"></a>/align switch

El **modificador /align** es funcionalmente el mismo que la opción MIDL [**/Zp**](-zp.md) y lo reconoce el compilador de MIDL únicamente por compatibilidad con versiones anteriores con MkTypLib.

> [!Note]  
> La Mktyplib.exe está obsoleta. En su lugar, use el compilador MIDL.

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*Alineación* 
</dt> <dd>

Especifica la alineación de los tipos de la biblioteca. El *valor* de alineación puede ser 1, 2, 4 u 8. El valor 1 indica la alineación natural; *n* indica la alineación en el byte *n*. Si no especifica el modificador **/align,** el valor predeterminado es 8.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si va a generar un nuevo archivo Make, use el [**modificador /Zp.**](-zp.md)

El valor de alineación corresponde al valor de la opción [**/Zp**](-zp.md) utilizado por el compilador de Microsoft C/C++. Asegúrese de especificar la misma alineación al invocar el compilador de C que al invocar el compilador MIDL.

Para obtener más información, consulte la documentación de programación de Microsoft C/C++. Para obtener una explicación de los posibles riesgos en el uso de niveles de empaquetado no estándar, consulte el tema de ayuda [**/Zp.**](-zp.md)

## <a name="examples"></a>Ejemplos

**midl /align:4 filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




