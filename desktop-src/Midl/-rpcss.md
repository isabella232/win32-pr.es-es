---
title: Modificador /rpcss
description: El modificador /rpcss, cuando se especifica, actúa como si se especificara el atributo enable allocate en todas \_ las operaciones de la interfaz. No se recomienda el uso de este atributo.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- /rpcss switch MIDL
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0c3087f47bd12c852ef168b2684d5b094239cdac45933c8e7d831fc6461c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643745"
---
# <a name="rpcss-switch"></a>Modificador /rpcss

El **modificador /rpcss,** cuando se especifica, actúa como si se especificara el atributo [**enable \_ allocate**](enable-allocate.md) en todas las operaciones de la interfaz. No se recomienda el uso de este atributo.

``` syntax
midl /rpcss
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

En el modo predeterminado, el paquete RpcSs solo está habilitado si el procedimiento o la interfaz tienen el atributo [**enable \_ allocate**](enable-allocate.md) o se especifica el modificador **/rpcss** en la línea de comandos. En **el modo /osf,** el código auxiliar del lado servidor habilita el paquete de asignación RpcSs.

## <a name="examples"></a>Ejemplos

**midl /rpcss filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**habilitar \_ asignación**](enable-allocate.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




