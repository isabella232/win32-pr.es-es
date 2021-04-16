---
title: modificador/use_epv
description: El \_ modificador/use EPV indica al compilador de MIDL que genere código de código auxiliar de servidor que llame a la rutina de aplicación de servidor a través de un vector de punto de entrada (EPV), en lugar de una llamada estática. No se recomienda el uso de este atributo.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv modificador MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685699"
---
# <a name="use_epv-switch"></a>/Use \_ modificador EPV

El modificador **/use \_ EPV** indica al compilador de MIDL que genere código de código auxiliar de servidor que llame a la rutina de aplicación de servidor a través de un vector de punto de entrada (EPV), en lugar de una llamada estática. No se recomienda el uso de este atributo.

``` syntax
midl /use_epv
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Normalmente, las aplicaciones requieren vinculación estática a la rutina de aplicación de servidor. El compilador MIDL genera este tipo de llamada de forma predeterminada. Sin embargo, si una aplicación requiere que el código auxiliar del servidor llame a la rutina de aplicación de servidor mediante EPV, se debe especificar el modificador **\_ EPV de/use** . Cuando se especifica el modificador **/use \_ EPV** , el compilador MIDL genera una EPV predeterminada. Este valor predeterminado de EPV se usa después si la aplicación no registra otro EPV a través de la llamada a [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .

## <a name="examples"></a>Ejemplos

**MIDL/use \_ EPV** *filename * * *. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/no \_ default \_ EPV**](-no-default-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 