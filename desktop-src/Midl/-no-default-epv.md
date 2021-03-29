---
title: modificador/no_default_epv
description: El \_ modificador de EPV predeterminado de/no \_ indica al compilador de MIDL que no genere un vector de punto de entrada predeterminado (EPV). No se recomienda el uso de este atributo.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv modificador MIDL
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995143"
---
# <a name="no_default_epv-switch"></a>/no \_ \_ modificador EPV predeterminado

El modificador de **\_ \_ EPV predeterminado de/no** indica al compilador de MIDL que no genere un vector de punto de entrada predeterminado (EPV). No se recomienda el uso de este atributo.

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

En este caso, la aplicación debe registrar un EPV con la llamada a [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) . Compare este modificador con el modificador [**\_ EPV de/use**](-use-epv.md) .

## <a name="examples"></a>Ejemplos

**MIDL/no \_ default \_ EPV nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/Use \_ EPV**](-use-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 