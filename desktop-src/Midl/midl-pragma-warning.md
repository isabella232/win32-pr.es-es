---
title: midl_pragma atributo Warning
description: Use la \_ opción de advertencia pragma MIDL para invalidar temporalmente el comportamiento del mensaje de advertencia de MIDL en tiempo de compilación.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma el atributo de advertencia MIDL
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904014"
---
# <a name="midl_pragma-warning-attribute"></a>\_pragma MIDL Warning (atributo)

Use la opción de **\_ ADVERTENCIA pragma MIDL** para invalidar temporalmente el comportamiento del mensaje de advertencia de MIDL en tiempo de compilación.

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*opción de advertencia \_* 
</dt> <dd>

La opción de advertencia puede ser una de las siguientes: deshabilitar, habilitar, valor predeterminado.

</dd> <dt>

*lista de mensajes \_* 
</dt> <dd>

Una lista de números de mensaje separados por espacios.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La Directiva pragma se puede usar como una directiva pragma del compilador de C. Es decir, deshabilita, habilita o vuelve al comportamiento predeterminado de una advertencia de MIDL determinada.

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

 

 




