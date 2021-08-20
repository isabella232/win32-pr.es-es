---
title: Modificador /use_epv
description: El modificador /use epv dirige al compilador midL a generar código auxiliar de servidor que llama a la rutina de aplicación de servidor a través de un vector de punto de entrada (epv), en lugar de \_ mediante una llamada estática. No se recomienda el uso de este atributo.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv switch MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 614abaf4c124aa0a6e1ca5f7da347ab4a9a2264e174c91734e6a75b188500a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014063"
---
# <a name="use_epv-switch"></a>Modificador /use \_ epv

El **modificador \_ /use epv** dirige al compilador midL a generar código auxiliar de servidor que llama a la rutina de aplicación de servidor a través de un vector de punto de entrada (epv), en lugar de mediante una llamada estática. No se recomienda el uso de este atributo.

``` syntax
midl /use_epv
```

## <a name="switch-options"></a>Opciones de cambio

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

Normalmente, las aplicaciones requieren vinculación estática a la rutina de aplicación de servidor. El compilador MIDL genera dicha llamada de forma predeterminada. Sin embargo, si una aplicación requiere que el código auxiliar del servidor llame a la rutina de aplicación de servidor mediante epv, se debe especificar el modificador **\_ /use epv.** Cuando se especifica el modificador **\_ /use epv,** el compilador MIDL genera un epv predeterminado. A continuación, se usa este epv predeterminado si la aplicación no registra otro epv a través de la [**llamada RpcServerRegisterIf.**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)

## <a name="examples"></a>Ejemplos

**midl /use \_ epv** *filename:.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/no \_ default \_ epv**](-no-default-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 