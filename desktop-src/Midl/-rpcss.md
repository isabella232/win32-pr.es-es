---
title: modificador/RPCSS
description: El modificador/RPCSS, cuando se especifica, actúa como si \_ se hubiera especificado el atributo enable Allocate en todas las operaciones de la interfaz. No se recomienda el uso de este atributo.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- /RPCSS modificador MIDL
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dabdd6340005c4e56080dc91bdd372a858e0e7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076598"
---
# <a name="rpcss-switch"></a>modificador/RPCSS

El modificador **/RPCSS** , cuando se especifica, actúa como si se hubiera especificado el atributo [**enable \_ allocate**](enable-allocate.md) en todas las operaciones de la interfaz. No se recomienda el uso de este atributo.

``` syntax
midl /rpcss
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

En el modo predeterminado, el paquete RpcSs solo está habilitado si el procedimiento o la interfaz tiene el atributo [**habilitar \_ asignación**](enable-allocate.md) o el modificador **/RPCSS** se ha especificado en la línea de comandos. En el modo **/OSF** , el código auxiliar del lado servidor habilita el paquete de asignación RPCSS.

## <a name="examples"></a>Ejemplos

**MIDL/RPCSS nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**habilitar \_ asignación**](enable-allocate.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




