---
title: midl_pragma de advertencia
description: Use la opción midl pragma warning para invalidar temporalmente el comportamiento del mensaje de advertencia \_ de MIDL en tiempo de compilación.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma atributo de advertencia MIDL
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae8e902d1e58ff216f36ae8003dc8f3f553a32005136ef2a86201bd17279107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067095"
---
# <a name="midl_pragma-warning-attribute"></a>Midl \_ pragma warning attribute

Use la **opción midl \_ pragma warning** para invalidar temporalmente el comportamiento del mensaje de advertencia de MIDL en tiempo de compilación.

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*opción \_ warning* 
</dt> <dd>

La opción de advertencia puede ser una de las siguientes: disable, enable, default.

</dd> <dt>

*lista de \_ mensajes* 
</dt> <dd>

Lista de números de mensaje separados por espacios.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La pragma se puede usar como una pragma del compilador de C. Es decir, deshabilita, habilita o vuelve al comportamiento predeterminado para una advertencia MIDL determinada.

## <a name="examples"></a>Ejemplos

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




