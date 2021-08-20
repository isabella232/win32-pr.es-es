---
title: Modificador /no_default_epv
description: El modificador epv /no predeterminado dirige al compilador MIDL a no generar un vector de punto de entrada \_ \_ (epv) predeterminado. No se recomienda el uso de este atributo.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv switch MIDL
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69400ca5e3abfe73254648042e8b9f969f1ed9cf370407b38fdc42bcad5d4903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992190"
---
# <a name="no_default_epv-switch"></a>Modificador \_ \_ epv /no predeterminado

El **modificador \_ \_ epv /no** predeterminado dirige al compilador MIDL a no generar un vector de punto de entrada (epv) predeterminado. No se recomienda el uso de este atributo.

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a>Opciones de cambio

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

En este caso, la aplicación debe registrar un epv con la [**llamada RpcServerRegisterIf.**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) Compare este modificador con el [**modificador \_ /use epv.**](-use-epv.md)

## <a name="examples"></a>Ejemplos

**midl /no \_ default \_ epv filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/use \_ epv**](-use-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 